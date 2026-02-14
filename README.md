# RecipeQA NLP System

## Overview:
This project is an end-to-end Natural Language Processing system designed to tackle the RecipeQA dataset , which contains questions about cooking recipes. It demonstrates advanced NLP techniques including multiple-choice question answering, retrieval-based reasoning, and generative text modeling. The system is built to showcase skills in data preprocessing, transformer models, embeddings, and performance evaluation—key competencies for a Data Science program.

## Project Description:
The RecipeQA NLP system answers questions about recipes by combining:

 - BERT-based multiple-choice classification for structured question-answering.

 - T5-based generative modeling as a fallback for ambiguous or complex questions.

 - Sentence-BERT and FAISS for context retrieval from a large set of recipes.

The pipeline ensures that the model can understand recipe instructions, relate them to questions, and generate accurate answers even for questions that require reasoning beyond simple classification.

## Key Features:

 - Data preprocessing: Extracts textual samples from JSON dataset, handles missing questions, concatenates recipe steps into a single context, calculates context statistics.

 - Multiple-choice modeling: Uses BERT to classify questions into correct answer choices.

 - Generative fallback: Uses T5-small to generate answers when BERT confidence is low.

 - Context retrieval: Embeds recipes with Sentence-BERT and retrieves relevant contexts with FAISS.

 - Evaluation: Computes overall accuracy on validation data, supports confidence thresholding.

## Data:

- Source: RecipeQA dataset on Kaggle

- Splits: Training, validation, testing

- Preprocessing: Missing questions handled, context concatenated, tokenized for transformer inputs

## Results:

 - Achieved overall system accuracy: ~40% on validation set.

 - Correctly answers questions requiring textual reasoning, temporal ordering, step identification, and ingredient matching.

 - Efficient retrieval of relevant context using FAISS enables robust performance even on long recipes.

## Future Work:

1. Fine-tune BERT and T5 on larger recipe datasets for higher accuracy.

2. Deploy the system as an interactive web app for recipe QA.

3. Incorporate additional transformer architectures (eg, RoBERTa, GPT-style models) for comparison.

## Technologies & Libraries:

Python, PyTorch, Hugging Face Transformers, Sentence-BERT, FAISS, pandas, tqdm

Models: bert-base-uncased, t5-small,all-MiniLM-L6-v2

## Author / Contact:
Ramin Safdar Tourehei
Email: Rsafdart@gmail.com
