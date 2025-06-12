# Subjectivity Classification in News Articles

This repository contains the code, models, and predictions for our project on **subjectivity classification**, where we classify sentences from news articles as either **subjective (SUBJ)** or **objective (OBJ)**. The work is based on fine-tuning and evaluating several transformer-based models across multiple languages, and implementing ensemble strategies to improve classification performance.

## Models Used

We fine-tuned and evaluated the following multilingual transformer models:
- [DistilBERT](https://huggingface.co/distilbert-base-multilingual-cased)
- [InfoXLM](https://huggingface.co/microsoft/infoxlm-base)
- [mBERT](https://huggingface.co/bert-base-multilingual-cased)
- [MiniLM](https://huggingface.co/nreimers/mMiniLMv2-L12-H384-distilled-from-XLMR-Large)
- [XLM-RoBERTa](https://huggingface.co/xlm-roberta-base)

## Repository Structure

- `data/`  
  Contains the datasets for each language in dedicated subfolders (e.g., `english/`, `italian/`, `multilingual/`, etc.).

- `models/`  
  Should contain folders with the fine-tuned versions of each transformer model:
  - DistilBERT
  - InfoXLM
  - mBERT
  - MiniLM
  - XLM-RoBERTa
    
  However, GitHub does not allow to upload these folders because they exceed the size limit.

- `predictions/`  
  Contains subfolders for each model and for the ensemble methods. Each subfolder includes model predictions for all test settings.
  - `distilmbert_predictions/`
  - `infoxlm_predictions/`
  - `mbert_predictions/`
  - `minilm_predictions/`
  - `xlm_roberta_predictions/`
  - `ensemble_predictions/`

- `scorer/`  
  Official evaluation script provided by the task organizers.

- `data_analysis.ipynb`  
  Exploratory notebook with dataset statistics and label distribution analysis.

- `distilmbert.ipynb`  
  Fine-tuning, evaluation, and error analysis for DistilBERT.

- `infoxlm.ipynb`  
  Fine-tuning, evaluation, and error analysis for InfoXLM.

- `mbert.ipynb`  
  Fine-tuning, evaluation, and error analysis for mBERT.

- `minilm.ipynb`  
  Fine-tuning, evaluation, and error analysis for MiniLM.

- `xlmroberta.ipynb`  
  Fine-tuning, evaluation, and error analysis for XLM-RoBERTa.

- `ensamble.ipynb`  
  Implementation and evaluation of ensemble strategies: Majority Voting, Probability Averaging, and Stacking

