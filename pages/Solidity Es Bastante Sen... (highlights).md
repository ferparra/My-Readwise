title:: Solidity Es Bastante Sen... (highlights)
author:: [[@patriciomolina on Twitter]]
full-title:: "Solidity Es Bastante Sen..."
category:: #tweets
url:: https://twitter.com/patriciomolina/status/1494039063774515208

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Solidity es bastante sencillo como lenguaje de programación, pero es bastante difícil programar *bien* en ese lenguaje, especialmente si venís con algunas "malas prácticas" de otros lenguajes.
	  
	  Dejo algunas conclusiones por haber hecho el challenge de @exactly_finance.
	  
	  1/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039063774515208))
		- **Note**: Thread
	- "Just for fun" hice el challenge de @exactly_finance (lo pueden encontrar en https://t.co/5NiLJCiwuS). Es un smart contract que recibe depósitos y distribuye rewards entre el pool de miembros.
	  
	  Quería saber si era capaz de hacerlo con lo poco que sé de Solidity.
	  
	  2/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039065825529859))
	- Lo primero que hice fue armar un prototipo básico en Python (mi lenguaje de cabecera) para probar algunas hipótesis. Salió rápido. Me hizo ahorrar bastante tiempo pero también me hizo cometer varios errores que voy a explicar en un par de tuits 🙂
	  
	  3/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039067998269450))
	- El setup del challenge se hace súper fácil con @HardhatHQ. Basta con seguir el tutorial que está en https://t.co/hZ99mDHzs8 y en un toque ya estás programando el smart contract. Sugiero primero escribir los tests y después desarrollar las funciones. So far, so good.
	  
	  4/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039070271488003))
	- Después de unas horas me encuentro con el primer gran roadblock: Solidity no soporta operaciones nativas de punto flotante 🤦‍♂️ Por ejemplo, si hacés 3/2 te da 1.
	  
	  En otras palabras: sólo maneja enteros (lo cual tiene sentido porque la EVM corre en hardware muy heterogéneo)
	  
	  5/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039072838459397))
	- Googleando encontré la forma de sortear el problema y salí andando, ¿pero vieron que les dije que Python me hizo cometer errores? Bueno, el error fundamental fue recorrer listas.
	  
	  6/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039075443126276))
	- En Solidity es carísimo (en gas) hacer loops (e.g.: recorrer un array). Usarlos indiscriminadamente es una mala práctica. En mi script de prueba usé diccionarios y listas para distribuir los rewards, y eso ya era un problema. La v1 del contrato cumplía, pero a qué costo...
	  
	  7/12 
	  
	  ![](https://pbs.twimg.com/media/FLvdXNiXIAUaggy.jpg) ([View Tweet](https://twitter.com/patriciomolina/status/1494039081361285127))
	- El genio de @lucaslain generosamente revisó mi código y me levantó el punto: se puede hacer O(1). Volví al código y creí haber encontrado una solución sin loops, pero la v2 hacía mal los pagos de los rewards ante un escenario de test que se me había escapado 😨
	  
	  8/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039083718529025))
	- Mis tests corrían, y si mi contrato hubiera llegado a mainnet ese bug hubiera sido explotado y dejado al contrato (y a sus miembros) sin un mango (o "sin un wei" 😂)
	  
	  Baño de humildad. Solidity 2 - Pato 0.
	  
	  9/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039085803085829))
	- Finalmente llegué a una solución O(1), lo implementé y salió andando, pero lo más importante no fue haber llegado a una solución eficiente sino a la siguiente conclusión: en Solidity estás obligado a pensar en términos de eficiencia o "sos pollo" 🍗
	  
	  10/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039088021839879))
	- En Python y otros lenguajes sabés que tu código puede ser +/- eficiente en términos de uso de CPU y memoria, pero va a terminar su ejecución. En Solidity el gas limit de la tx te pone una patada que te podría dejar sin poder acceder a los fondos del contrato para siempre.
	  
	  11/12 
	  
	  ![](https://pbs.twimg.com/media/FLvg0VwWQAkaLvd.png) ([View Tweet](https://twitter.com/patriciomolina/status/1494039092568469508))
	- Así que ya saben: a Solidity se lo respeta (?)
	  
	  Aprendí muchísimo haciendo este challenge. Si te gusta programar te recomiendo que lo hagas (y de paso a lo mejor pegás un laburito copado en @exactly_finance 😉)
	  
	  12/12 ([View Tweet](https://twitter.com/patriciomolina/status/1494039094904729604))