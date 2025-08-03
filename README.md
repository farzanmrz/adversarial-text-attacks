# Adversarial Attacks on Text Classification Models

This repository contains the final project report for the **CS616 Robust Deep Learning** course. The project investigates the vulnerability of modern NLP models to adversarial attacks, specifically focusing on word-level perturbations against BERT for text classification tasks.

## 📝 Project Overview

Adversarial attacks in NLP aim to deceive models by making subtle changes to the input text that are often unnoticeable to humans but cause the model to misclassify the text. This project explores the effectiveness of **black-box, word-level adversarial attacks**, which offer a balance between effectiveness, readability, and ease of implementation.

The study focuses on the **BERT (Bidirectional Encoder Representations from Transformers)** model due to its prominence in NLP research and its widespread use in text classification applications.

## ⚔️ Attack Methodology

This project reproduces the **TEXTFOOLER** framework, a hybrid attack method that combines score-based and decision-based techniques to generate adversarial examples. The core components of this framework are:

1.  **Word Importance Identification**: The algorithm first identifies key words in a sentence that have the most significant impact on the model's prediction score.
2.  **Semantic Word Replacement**: It then substitutes these important words with their semantically similar synonyms to craft an adversarial example that preserves the original meaning and grammar.

## 📊 Key Findings

The experiment successfully reproduced the results of the original TEXTFOOLER study, highlighting BERT's vulnerability to such attacks. The key metrics from the experiment, averaged across five datasets (MR, IMDB, Yelp, AG, and Fake), are as follows:

* **Attack Success Rate**: 80.48%
* **Perturbation Rate**: 14.08% of words were altered
* **Semantic Similarity**: The perturbed text maintained a high similarity score of 0.72
* **Accuracy Drop**: The average accuracy of the BERT model dropped from **93.18%** on original text to **12.70%** on adversarial text.

These results demonstrate that hybrid attacks can create high-quality adversarial examples with minimal changes, posing a significant challenge for models used in security-sensitive applications.

## 📄 Report

For a detailed analysis, methodology, and discussion of the results, please see the full project report: `Final Project Report.pdf`.

## References

Jin, D., Jin, Z., Zhou, J. T., & Szolovits, P. (2020). Is BERT Really Robust? A Strong Baseline for Natural Language Attack on Text Classification and Entailment. *The Thirty-Fourth AAAI Conference on Artificial Intelligence (AAAI-20)*.
