# NER-based-Smart-Medical-Question-Answering


**🩺 Medical Question Answering System**
A robust Medical Question Answering System leveraging advanced Natural Language Processing (NLP) models such as BioBERT, Sentence Transformers, FAISS, and Abbreviation Expansion to retrieve, understand, and summarize precise medical information from a structured dataset.

**📌 Project Overview**
This project aims to bridge the information gap in the healthcare domain by providing an intelligent question-answering system trained on a medical QA dataset. Users can input natural language medical questions, and the system returns concise, medically accurate answers using state-of-the-art NLP techniques.

**Key features:**

i. Named Entity Recognition (NER) with BioBERT

ii. Semantic search using FAISS Indexing

iii. Abbreviation expansion for domain-specific terms

iv. Answer summarization using BART

v. Fuzzy matching to enhance answer confidence

💡 **How It Works**
**Dataset Loading:** Medical QA pairs are loaded and cleaned from a CSV file.

**NER Extraction:** Entities in the question are recognized using BioBERT.

**Semantic Embedding:** Questions are converted to vectors using all-MiniLM-L6-v2.

**Indexing:** A FAISS HNSW index is built for efficient semantic search.

**Answer Retrieval:** Top-k similar questions are retrieved and ranked.

**Abbreviation Expansion:** Short forms are expanded using a medical dictionary.

**Summarization:** Retrieved answers are summarized using BART for clarity.

**Confidence Scoring:** Answers are ranked using fuzzy logic based similarity.

**📂 Dataset**
The system uses a custom-preprocessed version of the MedQuAD (Medical Question Answering Dataset) which includes real-world QA pairs from trusted medical sources.

**🧠 Technologies Used**
Transformers by HuggingFace (BioBERT, BART)

Sentence-Transformers for embeddings

FAISS for fast similarity search

FuzzyWuzzy for ranking responses

NLTK for stopword handling

Pandas and NumPy for data wrangling

**🚀 Installation**
git clone https://github.com/your-username/medical-question-answering.git
cd medical-question-answering
pip install -r requirements.txt
**Dependencies (inferred from notebook):**
pip install sentence_transformers faiss-cpu fuzzywuzzy python-Levenshtein pandas numpy transformers nltk


**⚙️ Usage**
You can run the notebook directly:

**jupyter notebook Medical_Question_Answering.ipynb**
Or integrate the models into an API interface for deployment.

**📈 Results**
Fast response time using FAISS HNSW indexing

High relevance and clarity in answers

Successfully handles abbreviations and complex questions

**Example Input:**
"What is the treatment for DVT?"

**Example Output:**
"Treatment for Deep Vein Thrombosis (DVT) often includes anticoagulant medications, compression stockings, and in some cases, surgical interventions."

