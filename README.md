

# Sahih-El-Bukhari-chat-with-Langchain-RAG

This project aims to leverage the power of LangChain and Retrieval Augmented Generation (RAG) to build a question-answering system based on the Hadiths, specifically utilizing the Sahih Bukhari dataset. The system embeds Hadith texts using sentence transformers, stores these embeddings with FAISS, and then performs similarity searches to find relevant Hadiths to answer user queries. The answers are generated through a pipeline that combines the RAG approach with a large language model, specifically meta-llama/Llama-2-7b-chat-hf, fine-tuned for causal language modeling tasks.

## Features

- **Document Embedding and Storage**: Utilizes HuggingFace's Sentence Transformers for embedding Hadith texts and FAISS for efficient storage and retrieval.
- **Question Answering**: Leverages LangChain for crafting a retrieval-based QA chain that integrates the RAG technique for generating informative, contextually relevant answers.
- **Multilingual Support**: Designed to handle queries in Arabic, showcasing deep understanding and response generation based on Islamic texts.

## Installation

This project requires Python 3.7 or later. Clone this repository and install the dependencies as follows:

```bash
git clone <this-repository>
cd <repository-folder>
pip install -r requirements.txt
```

### Dependencies

- `transformers`
- `torch`
- `langchain`
- `langchain_community`
- `chainlit`
- `sentence_transformers`
- `faiss-gpu`
- `bitsandbytes`
- `accelerate`

You can install all required packages with the following command:

```bash
pip install transformers torch langchain langchain_community chainlit sentence_transformers faiss-gpu bitsandbytes accelerate --quiet
```

## Usage

To use this project, follow these steps:

1. **Prepare your dataset**: Place your Hadith dataset in CSV format under `/content/`.
2. **Run the script**: Execute `hadith.py` to start the question-answering system.
3. **Query the system**: Input your questions in Arabic to receive answers based on the Sahih Bukhari Hadiths.

### Example Query

```python
query = "ما هي نسبة الزكاة من المال"
response = final_result(query)
print(response)
```

This will output the relevant Hadith or information from the dataset, along with the generated response from the model.

## Contributing

Contributions to this project are welcome. Please fork the repository, make your changes, and submit a pull request.



This project is licensed under the MIT License - see the LICENSE file for details.

---

Make sure to add any additional sections you think are necessary, such as **Acknowledgments**, **Project Structure**, or **Future Work**. This template should give you a solid foundation for presenting your project on GitHub.
