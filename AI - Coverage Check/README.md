# Automated Coverage Check using AI Techniques

## Overview

This project addresses the challenge of automating the coverage check process in the POC (Proof of Concept) phase at IDD. Due to discrepancies in the naming of financial products between client references and internal naming conventions, this process has traditionally been manual. The project leverages NLP (Natural Language Processing) and ML (Machine Learning) techniques to match client-referenced financial products with their corresponding IDD products, aiming for high accuracy and confidence levels.

## Creating the Knowledge Base

A comprehensive knowledge base is established from three primary sources:

- **Internal Naming Conventions**: The foundational dataset reflecting IDD's product naming schema.
- **Past POCs**: Historical mappings of client references to IDD products, serving as a valuable learning resource.
- **Market Data Analyst Input**: Additional insights, such as expanded acronyms and naming nuances, further enrich the knowledge base.

## Data Preprocessing

Data preprocessing involves cleaning references, removing noise, and distinguishing between similar but conceptually different terms. Techniques include:

- Eliminating irrelevant words and characters.
- Creating artificial distance between words with similar spellings but opposite meanings.
- Transforming cleaned text references into numeric vectors using TF-IDF vectorization, facilitating machine learning model training and prediction.

## Model Training and Prediction

The project utilizes a K-nearest neighbors (KNN) model to find the best match for a given client reference within the knowledge base. A distance threshold is carefully selected to balance the trade-off between prediction accuracy and coverage.

## Cross-validation and Threshold Tuning

Extensive cross-validation ensures model robustness, while threshold tuning optimizes the balance between precision and recall. The project achieves an accuracy of up to 84.7% for predicted matches, with a significant portion of matches derived from historical POC data.

## Future Directions

Efforts to enhance the project's effectiveness include expanding the training dataset, enriching the knowledge base with more analyst insights, developing a user interface for POC team use, and exploring open-source LLM models for potentially improved performance.

