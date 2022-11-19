title:: $GGAL Bajando -1% Y Call... (highlights)
author:: [[@JohnGalt_is_www on Twitter]]
full-title:: "$GGAL Bajando -1% Y Call..."
category:: #tweets
url:: https://twitter.com/JohnGalt_is_www/status/1432800456745627654

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- $GGAL bajando -1% y calls de GGAL subiendo +20%
	  ¿están crazy Macaya o qué?
	  
	  No, no hay nadie crazy, es super racional y se explica con la sensibilidad a vega/delta, lo voy a intentar explicar sin formulas bien conceptual en un mini-hilo 🧵 
	  
	  ![](https://pbs.twimg.com/media/E-JMisUXsAMWj7m.jpg) ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800456745627654))
		- **Note**: Thread
	- El punto es que el precio de las opciones (CALLs y PUTs) depende de varios factores, en este caso nos concentramos en 2:
		- **Tags**: #[[favorite]]
	- El punto es que pasa cuando varía la volatilidad
	  
	  A más volatilidad más suben los calls
	  A  más volatilidad más suben los puts
	  
	  Sí, ambos suben con la volatilidad, y como se imaginarán la pregunta es ¿a que es mas sensible el precio al precio de $GGAL o a su volatilidad? ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800461426503685))
	- Bueno, no es tan sencillo responder esto porque son relaciones no lineales ambas y a su vez dependen de varias cosas como el tiempo para expiración y de que tan fuera de dinero esté la opción
	  
	  Ahí viene entonces la utilidad de las griegas ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800463783616513))
	- Justamente las griegas me permiten derivar parcialmente la función del precio contra una sola variable de todas las que inciden y con ello medir la sensibilidad a ESA variable puntual por separado
	  
	  Tranca, no voy a poner derivadas en un hilo de tw, lo importante es el concepto ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800465926885379))
	- Entonces, volviendo al gráfico, vemos 
	  vega: La sensibilidad del Call a la volatilidad de AAPL
	  delta: La sensibilidad del Call al precio de AAPL
	  
	  En función del strike (base del call ) 
	  y del TTM  (días para el vencimiento)
	  
	  Hice el graf con AAPL porque tiene mas liquidez 
	  
	  ![](https://pbs.twimg.com/media/E-JO0GjXEAMU-yN.jpg) ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800471161393154))
		- **Tags**: #[[trading]] #[[favorite]]
	- Sin hacer números ni fórmulas, lo importante es entender que hay zonas (bases y días al opex) donde pesa mas la variación de volatilidad y zonas donde pesa mas la variación del subyacente ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800473719902212))
	- La volatilidad viene subiendo (de 34% a 40%) hace unos días va gráfico de la volatilidad en 40 ruedas
	  
	  Cuando sube la volatilidad y sube GGAL se mezclan ambos factores y sube fuerte el precio del CALL
	  
	  Ahora que uno baja y el otro sube, pesa quien incide mas 
	  
	  ![](https://pbs.twimg.com/media/E-JTPgUX0AYkp4K.png) ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800478635700224))
	- Resumiendo en un ATM, o sea GGAL base 190 el aumento de volatilidad pesó mas que el 1% de baja del precio de GGAL para mover al call
	  
	  El primero lo sube el otro lo baja, resultado neto el call subió hoy un 10% con GGAL -1.5% ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800481399742467))
	- y obviamente no hay gráficos sin código python, así que ahí lo tienen
	  
	  https://t.co/pgzLfLSNBC ([View Tweet](https://twitter.com/JohnGalt_is_www/status/1432800484222504962))