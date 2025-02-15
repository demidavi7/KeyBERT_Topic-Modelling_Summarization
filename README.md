# KeyBERT for Dynamic Topic Modeling and Summarization 
## Overview
This repository provides two distinct studies:

**First Extension** - Dynamic Topic Modeling

A pipeline designed for keyword extraction, semantic clustering, and tracking topic evolution over time.
Uses KeyBERT for extracting representative keywords and applies topic modeling techniques to analyze trends.
[more details](https://github.com/demidavi7/KeyBERT_Topic-Modelling_Summarization/tree/main/First_Extension ) 

**Second Extension**- Text Summarization using Keywords enrichment

A separate study on text summarization that integrates the extractive capabilities of KeyBERT with the abstractive approach of DistilBART, aiming to enhance summary coherence and informativeness.
[more details](https://github.com/demidavi7/KeyBERT_Topic-Modelling_Summarization/tree/main/Summarization_second_extension) 

Additionally we have also added a lightweight library containing the inference pipeline for summary generation. 
It allows for djusting text enrichment parameters to fine-tune keyword representation and Choosing between two different models for summarization.[more details](https://github.com/demidavi7/KeyBERT_Topic-Modelling_Summarization/tree/main/summarizer_pipeline)

## Repository structure 
```
KeyBERT_Topic-Modelling_Summarization/
├── First_Extension/                       # First extension (Advanced Topic Modeling)
│   ├── KeyBERT_Extension_1.ipynb          # Notebook for keyword extraction & topic modeling
│   ├── README.md                          # Documentation for the first extension
│   ├── topic_evaluation_chart.png         # Topic evaluation visualization
│   ├── wordcloud_example.png              # Sample word cloud visualization
│   └── workflow_diagram.png               # Workflow representation of the extension
├── Summarization_second_extension/        # Second extension (Summarization)
│   ├── data-pre-processing.ipynb          # Notebook for text preprocessing
│   ├── summarization_results_base.csv     # Base summarization results
│   ├── summarization_results_top_list.csv # Summarization results (list model)
│   ├── summarization_results_top_single.csv # Summarization results (single model)
│   ├── test_cnn.csv                        # CNN test data 
│   └── training_models_and_testing.ipynb   # Notebook for training and testing summarization models
├── summarizer_pipeline/                   # Summarization library package
│   ├── build/lib/keyword_summarizer/      # Compiled summarization library
│   ├── keyword_summarizer/                # Main summarization library code
│   ├── keyword_summarizer.egg-info/       # Package metadata for the summarization library
│   ├── README.md                          # Documentation for summarization pipeline
│   └── setup.py                           # Setup file for installing the summarization library
└── README.md                              # Project documentation
```
## References

## Team
- Annalisa Belloni
- Davide Elio Stefano Demicheli
- Valeria Petrianni
- Valerio Xefteris
