Title:
Question Answering System Using Dense Retrieval + BERT

Project Description:
This notebook implements a Question and Answering System using BERT-based models. It uses a pre-trained BERT model for text encoding and fine-tuned BERT (bert-large-uncased-whole-word-masking-finetuned-squad) for question answering tasks. FAISS is employed for efficient similarity searches, making this system capable of answering questions from a corpus of text.

Approach:
Environment Setup:

Installs required libraries such as transformers, faiss-cpu, and torch.
Model Loading:

Loads bert-base-uncased for text encoding and bert-large-uncased-whole-word-masking-finetuned-squad for question answering.
Text Encoding:

Implements a function to encode input texts into dense vectors using BERT, applying mean pooling over token embeddings.
FAISS Indexing:

Utilizes FAISS for efficient retrieval by creating an index of the encoded document vectors.
Question Answering:

Likely uses the fine-tuned BERT model for extracting answers to user queries based on retrieved documents.
Metrics:

Exact Match (EM): Measures the percentage of predictions that match the ground truth answers exactly.
F1 Score: Evaluates the overlap between the predicted and actual answers.
Retrieval Accuracy: Assesses how often the relevant document is correctly retrieved.