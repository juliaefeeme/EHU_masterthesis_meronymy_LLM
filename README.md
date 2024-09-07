# Commonsense Knowledge Bases: Meronymic Relationships Acquisition and their Verification with Large Language Models
![tail2](https://github.com/user-attachments/assets/225614dc-c890-476b-b932-7896e00dc809)

> For humans, the tail of a bird is not the same as the tail of an airplane. Is it the same for an AI?

## Introduction
In the rapidly growing field of AI, especially in Natural Language Processing (NLP), adding commonsense knowledge (CSK) is important to improve large language models (LLMs). While these models are good at generating text, they often struggle with understanding basic semantic relationships. 

This study aims to enhance WordNet, a popular lexical database, by gathering part-whole relationships (like "bird-tail") from various CSK databases and validating them using LLMs. 

The research focuses on automating the whole process and showing how AI can improve linguistic databases and commonsense understanding.

## Methodology
1. Eight CSKBs: AristoTupleKB, Ascent++, ConceptNet, HasPartKB, Quasimodo, TransOMCS, Uncommonsense, VisualGenome
  - Extraction of *PartOf*, *MemberOf*, *SubstanceOf* and *Has* relationships
  - Random sample for manual evaluation
      - Are the samples actually relations?
2. Prompting LLMs (GPT4, LLaMA3.1, Phi3)
  - Testing the language models to observe if they can be used as a tool to validate meronymic relations

## Results
**CSKBs**

- 435,791 examples of meronymic pairs
- Random sample of 150 examples: 
    - 106 valid
    - 44 invalid

**LLMs**
| Metrics    | GPT-4 | LLaMA-3.1 | Phi-3 |
|------------|-------|-----------|-------|
| Precision  | **0.95**  | **0.95**      | 0.93  |
| Recall     | **0.94**  | 0.89      | 0.77  |
| F1-score   | **0.95**  | 0.92      | 0.85  |
| Accuracy   | **0.93**  | 0.89      | 0.80  |

## Conclusions
The study confirms that LLMs, especially GPT-4, can accurately validate these relationships, achieving over 95% accuracy. 

Smaller models like LLaMA-3.1 and Phi-3 perform less effectively but remain reliable. 

It is needed to address biases in CSKBs, such as homophobic and sexist content, and it is important to refine LLMs to avoid validating such biases.
