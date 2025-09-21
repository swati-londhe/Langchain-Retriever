# LangChain Retriever Strategies

## Overview

This notebook (`langchain_retrievers.ipynb`) explores various **retriever strategies** in **LangChain** for efficient information retrieval. It demonstrates the following:

- Using `WikipediaRetriever` for direct web-based search
- Building vectorstores with `FAISS` or `Chroma` combined with `OpenAIEmbeddings`
- Implementing different retriever types:
  - Similarity-based retriever
  - Maximum Marginal Relevance (MMR) retriever
  - `MultiQueryRetriever`
- Integrating `ChatOpenAI` with `MultiQueryRetriever` and `ContextualCompressionRetriever`

## Requirements

To run the notebook, install the required Python packages using the following command:

```bash
pip install langchain chromadb faiss-cpu openai tiktoken wikipedia langchain_openai langchain-community python-dotenv
```

## Setup

1. **Create a `.env` file** in the same directory as the notebook with your OpenAI API key:

   ```
   OPENAI_API_KEY=sk-xxxx
   ```

   Replace `sk-xxxx` with your actual OpenAI API key.

2. **Start Jupyter Notebook**:

   ```bash
   jupyter notebook
   ```

3. Open the `langchain_retrievers.ipynb` notebook in the Jupyter interface.

4. Run the cells in the notebook sequentially to execute the code.

## Expected Output

- The `WikipediaRetriever` will return short, relevant passages from Wikipedia.
- Vectorstore-based retrievers (`FAISS` or `Chroma`) will return relevant documents using similarity search or MMR.
- The `MultiQueryRetriever` will generate multiple query variations using a language model (LLM) to improve retrieval.
- The `ContextualCompressionRetriever` will return compressed, relevant context using `ChatOpenAI`.

## Notes

- A valid OpenAI API key is required for `OpenAIEmbeddings` and `ChatOpenAI`.
- Ensure an active internet connection for API calls and Wikipedia access.
- The notebook assumes familiarity with LangChain's retriever concepts.