# EquiInsight💰📈🔍  

EquiInsight is a specialised user-friendly platform made for investors, analysts, and financial professionals who specialise in equity markets. It is intended to make information retrieval simple. To get pertinent insights from the stock market and financial sphere, users can ask queries and input the URLs of articles.

![EquiInsight](https://github.com/harshd23/EquiInsight/blob/main/equiinsight.png)

## Technologies Used:-

- Langchain + LLM(Mistral) & Groq(Inference Engine)
- Streamlit: UI
- Huggingface embeddings: Text embeddings
- FAISS: Vector databse

## Features:-

- To retrieve article material, load URLs or upload text files containing URLs.
- Utilise the UnstructuredURL Loader provided by LangChain to process article content.
- Create an embedding vector with HuggingFaceBge embeddings and utilise FAISS, a strong similarity search library, to facilitate the efficient and quick retrieval of pertinent data.
- Use the Groq Inference Engine to communicate with the LLMs (Mistral) by submitting queries and getting answers along with source URLs.

## Why we can't directly use ChatGPT:-

- Problem 1: Pasting and copying articles in ChatGPT takes a lot of time and effort.
- Problem 2: We require a comprehensive knowledge base that allows the solution to potentially be found in three or four articles.
- Problem 3: The size of tokens in ChatGPT free tier accounts is restricted. Large news articles might not be the best option because we provide a lot of text and will be charged for it.

## Project Structure:-

- app.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- faiss_store_openai.pkl: A pickle file to store the FAISS index.
- .env: Configuration file for storing your HuggingFace Token and Groq API key.

## Steps to run the project:-

1.Clone this repository to your local machine using:

```bash
  git clone https://github.com/harshd23/EquiInsight.git
```

2.Install the required dependencies using pip:

```bash
  pip install -r requirements.txt
```

3.Set up your Groq API key and HuggingFace Tokens by creating a .env file in the project root and adding your API

```bash
  HF_TOKEN = your_huggingface_token
  GROQ_API_KEY = your_api_key_here
```

## Usage of the project:-

1.Run the Streamlit app by executing:

```bash
streamlit run app.py
```

2.The web app will open in your browser.

- On the sidebar, you can input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those news articles
- I have used following news articles:
  - <https://www.moneycontrol.com/news/business/markets/bombay-hc-orders-sebi-to-disclose-icici-securities-exemption-letter-12792721.html>
  - <https://www.moneycontrol.com/news/business/amazon-partners-with-45-govt-emporiums-ngos-trade-bodies-to-empower-local-artisans-12789470.html>
  - <https://www.moneycontrol.com/news/business/state-bank-of-india-deploys-2000-bankers-to-woo-the-wealthy-12787918.html>
