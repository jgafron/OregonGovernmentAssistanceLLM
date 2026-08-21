# AI Government Assistance Advisor

> An AI-powered recommendation system that fine-tuned OpenAI language models to recommend Oregon government assistance programs using synthetically generated training data.

## Overview

This repository holds the datasets, fine-tuning artifacts, and supporting materials from a university machine learning project focused on building a domain-specific AI assistant that recommends Oregon government assistance programs.

Rather than hand-writing hundreds of training examples, I started by researching Oregon's assistance programs and documenting their eligibility requirements, factors like household size, monthly income, age, pregnancy status, disability, residency, veteran status, and other program-specific qualifications.

To keep the training data consistent and high-quality, I built a Python-based synthetic data generator that created applicant profiles by varying demographic attributes, then determined which assistance programs each synthetic applicant actually qualified for based on the documented eligibility rules. That gave us a large, internally consistent training dataset without the manual effort of writing every example by hand.

The generated examples were converted into OpenAI's JSONL fine-tuning format and used to fine-tune multiple OpenAI language models. We ran and compared several training runs to improve recommendation consistency and overall response quality.

The finished model was integrated into a university prototype where users could describe their situation in plain language and get back personalized government assistance recommendations.

## Project Workflow

1. Research Oregon government assistance programs and document eligibility requirements.
2. Encode eligibility criteria into structured training data.
3. Generate synthetic applicant profiles using a custom Python data generation tool.
4. Automatically determine applicant eligibility based on program rules.
5. Convert generated examples into OpenAI JSONL fine-tuning datasets.
6. Fine-tune multiple OpenAI language models.
7. Evaluate model performance and iterate on training data quality.

## Repository Structure

**`training_data/`**
The primary datasets used to train the model: the final OpenAI chat-format training dataset, program-specific eligible/ineligible examples, and earlier dataset iterations.

**`pet_data/`**
Additional datasets showing the same synthetic data generation approach extended to pet assistance programs.

**`metrics/`**
Training metrics and fine-tuning results.

**`presentation/`**
The university presentation covering the overall system and architecture.

## Technologies

Python, OpenAI Fine-Tuning, JSON/JSONL, Prompt Engineering, Synthetic Data Generation

## Note

This repository preserves the datasets and fine-tuning artifacts from the original university project. The deployed application and portions of the original generation pipeline were built as part of a team project and aren't included here.
