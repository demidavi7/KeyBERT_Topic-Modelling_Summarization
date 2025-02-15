# KeyBERT for Dynamic Topic Modeling and Summarization 

## Table of contents



Overview

This repository provides a powerful end-to-end pipeline for keyword extraction, topic modelling, and text summarization. Using KeyBERT, we extract meaningful keywords from text data and apply semantic clustering to group them into relevant topics. Additionally, we analyze topic evolution over time to uncover trends in textual datasets.
Workflow Overview

The pipeline follows these steps:

    Input Dataset:
    A dataset containing time-based textual data (e.g., news headlines) is provided.

    Grouping by Time Period:
    Text data is grouped by year and month to analyze topic trends.

    Keyword Extraction:
    We utilize KeyBERT to extract meaningful keywords from the dataset.

    Semantic Clustering:
    Extracted keywords are clustered based on their semantic similarity to form coherent topics.

    Topic Labeling:
    Each cluster is manually or algorithmically assigned a label that best represents the underlying topic.

    Topic Evolution Analysis:
        A matrix of topics over time is created to track topic frequency for each time period.
        Visualizations are generated to highlight the emergence, peaks, and decline of different topics over time.

<p align="center"> <img src="./workflow_diagram.png" alt="Workflow Diagram" width="80%"> </p>
Example Outputs
1. Word Cloud Representation

To better understand each topic, we generate word clouds that showcase the most frequent words associated with a given topic.
<p align="center"> <img src="./wordcloud_example.png" alt="Word Cloud for Topic coronavirus covid" width="30%"> </p>
2. Topic Evolution Over Time

A key aspect of this project is analyzing how topics emerge, evolve, and disappear over time. The visualization below displays the normalized frequency of the top spiking topics across multiple years.
<p align="center"> <img src="./topic_evaluation_chart.png" alt="Topic Evolution Over Time" width="90%"> </p>

This pipeline can be used for news trend analysis, research trend discovery, and other time-based textual insights.

## References

## Team
- Annalisa Belloni
- Davide Elio Stefano Demicheli
- Valeria Petrianni
- Valerio Xefteris
