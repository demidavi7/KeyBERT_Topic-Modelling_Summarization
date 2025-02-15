# Overview

This extension explores a hybrid text summarization approach, combining:

    Extractive summarization using KeyBERT to highlight the most relevant keywords.
    Abstractive summarization utilizing DistilBART, a transformer-based model, for generating more coherent summaries.

The study focuses on fine-tuning models on news article datasets and evaluating different summarization techniques using benchmarking metrics.
Pipeline Overview

The summarization process consists of three main stages:
## 1. Data Preprocessing

  The dataset is a sub-sample of the CNN/DailyMail news dataset (train.csv), containing 50,000 samples (~200MB).
  ([https://huggingface.co/VexPoli])
  Two different keyword positioning strategies:
        Keywords added at the end of the text.
        Keywords added at the beginning of the text.
        Creation of a dataset with a unique special token for keyword lists.
   
  Notebook: data-pre-processing.ipynb
    Techniques Used:
        tokenization, and augmentation
        Integration with Hugging Face datasets 
        Keyword extraction using KeyBERT

## 2. Model Training & Fine-Tuning
  [Pretrained DistilBART model](https://huggingface.co/sshleifer/distilbart-xsum-6-6) is fine-tuned on the processed dataset.
  Hugging Face Transformers library is used for loading and training.
  

 Implementation:

  Notebook: training_models_and_testing.ipynb
  Models Trained:
      BASE : DistilBART fine-tuned on standard news summarization dataset [https://huggingface.co/VexPoli/distilbart-summarization-base]
      LIST : DistilBART fine-tuned on keywords enriched news summarization dataset (list model) [https://huggingface.co/VexPoli/distilbart-summarization-top-list]
      SINGLE : DistilBART fine-tuned on keywords enriched news summarization dataset (single model) [https://huggingface.co/VexPoli/distilbart-summarization-top-single]
  Dataset & Preprocessing:
      Tokenization and text segmentation
      Special token handling for keyword-based learning

## 3. Evaluation & Testing

    The summarization model is tested on benchmark datasets, including:
        test_cnn.csv - A sample test set from the CNN/DailyMail dataset.
    Evaluation Metrics:
        ROUGE Score (Recall-Oriented Understudy for Gisting Evaluation)
        F1 Score for summary precision
        Human evaluation 

📌 Results Files:

    summarization_results_base.csv - Baseline model evaluation
    summarization_results_top_list.csv - Results for top-ranked summarization approaches
    summarization_results_top_single.csv - Best individual summary performance
