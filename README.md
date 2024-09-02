# Project Overview

This project involves working with a parallel corpus extracted from the EuroParl corpus, which includes translations of speeches delivered at the European Parliament in English, Dutch, and Italian. 
The goal is to preprocess the data, train character-level Statistical Language Models (SLMs), and evaluate their performance using perplexity.

# Files in the Repository

  - CL2024 Assignment.ipynb: The main Jupyter Notebook containing the code and analysis for the project.
  - parallel_sentences_en-nl-it.json: The parallel corpus file containing sentences in English (en), Dutch (nl), and Italian (it). Currently larger than 25 MB
  - .pkl files: These files contain the trained language models with attributes counts, vocab, and vocab_size.
  - .csv files: These files store the perplexity scores for each model on various test sets.

# Tasks Performed
1. Data Preprocessing

    Lowercasing: All text data is converted to lowercase.
    Digit Replacement: All digits are replaced with the letter "D".
    Character Filtering: Non-letter characters (excluding white spaces and accented letters) are removed.
    Data Splitting: The corpus is split into a training set (80%) and a test set (20%) using a random seed for reproducibility.

2. Training Language Models

    Bigram Model: A model predicting the current character based on the previous two characters.
    Tetragram Model: A model predicting the current character based on the previous four characters.
    Smoothing: Add-k smoothing (with k=0.01) is applied to the models.

3. Model Evaluation

    Perplexity Calculation: The perplexity of the models is evaluated on different test sets, including sentences in English, Dutch, and Italian.
    Analysis: Patterns in the models' performance are analyzed and discussed.

# Acknowledgments

This project is based on an assignment from the CL2024 course, focusing on the application of statistical language models to multilingual corpora.
