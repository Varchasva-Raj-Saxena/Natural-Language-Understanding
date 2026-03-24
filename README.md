# Assignment 2

This repository contains solutions for two NLP tasks:

- **Problem 1:** Learning word embeddings from IIT Jodhpur text using Word2Vec-style models.
- **Problem 2:** Character-level Indian name generation using recurrent neural network variants.

The notebooks are:

- [B23Cm1062_prob1.ipynb](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23Cm1062_prob1.ipynb)
- [B23Cm1062_prob2.ipynb](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23Cm1062_prob2.ipynb)

## Project Structure

- [B23Cm1062_prob1.ipynb](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23Cm1062_prob1.ipynb): Problem 1 notebook
- [B23Cm1062_prob2.ipynb](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23Cm1062_prob2.ipynb): Problem 2 notebook
- [B23CM1062-A2/corpus.txt](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23CM1062-A2/corpus.txt): saved IITJ corpus for Problem 1
- [TrainingNames.txt](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/TrainingNames.txt): training names file for Problem 2
- [iitj_pdfs](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/iitj_pdfs): PDF sources used for corpus creation

## Requirements

Install the Python libraries used in the notebooks before running:

```bash
pip install numpy matplotlib scikit-learn requests beautifulsoup4 PyPDF2 wordcloud nltk torch
```

You may also need to download NLTK resources inside the notebook. The Problem 1 notebook already includes those download commands.

## How To Run Problem 1

Problem 1 trains and analyzes CBOW and Skip-Gram style word embeddings on IIT Jodhpur text.

1. Open [B23Cm1062_prob1.ipynb](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23Cm1062_prob1.ipynb).
2. Make sure the corpus file exists at [B23CM1062-A2/corpus.txt](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23CM1062-A2/corpus.txt).
3. If you want to reuse the saved corpus, keep the corpus-loading path unchanged in the notebook.
4. Run the notebook from top to bottom.
5. The notebook will:
   - load and preprocess the corpus
   - report top-frequency words
   - train CBOW and Skip-Gram models
   - print sample embeddings
   - show nearest neighbors, analogies, and PCA plots

## How To Run Problem 2

Problem 2 trains recurrent models for character-level name generation.

1. Open [B23Cm1062_prob2.ipynb](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/B23Cm1062_prob2.ipynb).
2. Make sure [TrainingNames.txt](c:/Users/varchasva/OneDrive/Documents/Lab_Assignments/NLU_Assignmnet/Assignment%202/TrainingNames.txt) is present in the root folder.
3. Run the notebook from top to bottom.
4. The notebook will:
   - load and encode the name dataset
   - build the character vocabulary
   - train the vanilla RNN, BLSTM, and Attention+RNN models
   - generate sample names
   - compare models using novelty and diversity

## Notes

- Problem 1 can take longer if corpus scraping and PDF extraction are triggered instead of loading the saved corpus.
- Problem 2 uses the local names file directly, so changing `TrainingNames.txt` changes the training set.
- If plots or outputs look stale, restart the notebook kernel and rerun all cells.
