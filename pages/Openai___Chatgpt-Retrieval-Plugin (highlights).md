title:: Openai/Chatgpt-Retrieval-Plugin (highlights)
author:: [[openai]]
full-title:: "Openai/Chatgpt-Retrieval-Plugin"
category:: #articles
url:: https://github.com/openai/chatgpt-retrieval-plugin

- Highlights first synced by [[Readwise]] [[Mar 25th, 2023]]
	- The ChatGPT Retrieval Plugin repository provides a flexible solution for semantic search and retrieval of personal or organizational documents using natural language queries. ([View Highlight](https://read.readwise.io/read/01gwbe1yt8k6m96rd92x8a1dr1))
	- Memory Feature
	  
	  A notable feature of the Retrieval Plugin is its capacity to provide ChatGPT with memory. By utilizing the plugin's upsert endpoint, ChatGPT can save snippets from the conversation to the vector database for later reference (only when prompted to do so by the user). This functionality contributes to a more context-aware chat experience by allowing ChatGPT to remember and retrieve information from previous conversations. Learn how to configure the Retrieval Plugin with memory [here](https://github.com/openai/chatgpt-retrieval-plugin/blob/main/examples/memory). ([View Highlight](https://read.readwise.io/read/01gwbe3bygx7snzr1hwqfdk5g3))
- New highlights added [[Mar 28th, 2023]] at 12:34 PM
	- Webhooks
	  
	  To keep the documents stored in the vector database up-to-date, consider using tools like [Zapier](https://zapier.com) or [Make](https://www.make.com) to configure incoming webhooks to your plugin's API based on events or schedules. For example, this could allow you to sync new information as you update your notes or receive emails. You can also use a [Zapier Transfer](https://zapier.com/blog/zapier-transfer-guide/) to batch process a collection of existing documents and upload them to the vector database. ([View Highlight](https://read.readwise.io/read/01gwgqtshz2ghsxd0r4mmcbjk9))
	- Future Directions
	  
	  The ChatGPT Retrieval Plugin provides a flexible solution for semantic search and retrieval, but there is always potential for further development. We encourage users to contribute to the project by submitting pull requests for new features or enhancements. Notable contributions may be acknowledged with OpenAI credits.
	  
	  Some ideas for future directions include:
	  
	  •   **More vector database providers**: If you are interested in integrating another vector database provider with the ChatGPT Retrieval Plugin, feel free to submit an implementation.
	  •   **Additional scripts**: Expanding the range of scripts available for processing and uploading documents from various data sources would make the plugin even more versatile.
	  •   **User Interface**: Developing a user interface for managing documents and interacting with the plugin could improve the user experience.
	  •   **Hybrid search / TF-IDF option**: Enhancing the [datastore's upsert function](https://github.com/openai/chatgpt-retrieval-plugin/blob/main/datastore/datastore.py#L18) with an option to use hybrid search or TF-IDF indexing could improve the plugin's performance for keyword-based queries.
	  •   **Advanced chunking strategies and embeddings calculations**: Implementing more sophisticated chunking strategies and embeddings calculations, such as embedding document titles and summaries, performing weighted averaging of document chunks and summaries, or calculating the average embedding for a document, could lead to better search results.
	  •   **Custom metadata**: Allowing users to add custom metadata to document chunks, such as titles or other relevant information, might improve the retrieved results in some use cases.
	  •   **Additional optional services**: Integrating more optional services, such as summarizing documents or pre-processing documents before embedding them, could enhance the plugin's functionality and quality of retrieved results. These services could be implemented using language models and integrated directly into the plugin, rather than just being available in the scripts.
	  
	  We welcome contributions from the community to help improve the ChatGPT Retrieval Plugin and expand its capabilities. If you have an idea or feature you'd like to contribute, please submit a pull request to the repository. ([View Highlight](https://read.readwise.io/read/01gwgqvah0kb2f6340pn1mycpy))