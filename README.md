# Zero-Shot-Text-Generation

# Overview

The primary goal is to evaluate how efficiently different open-source LLMs process Assamese News text. The repository provides specific datasets for different news categories and individual scripts to measure the **latency** (inference time) for each model without prior fine-tuning (Zero-Shot).

# Datasets

The repository includes Assamese news articles categorized into the following five domains:

* **Crime, Law & Justice**
* **Entertainment**
* **Health**
* **Politics**
* **Sports**

These datasets are formatted for direct ingestion into the evaluation scripts.

# Models Evaluated

The following Large Language Models (LLMs) are benchmarked for performance:

1.  **Llama 3**
2.  **Qwen2.5-7B**
3.  **Mistral**
4.  **Aya-23**

# Methodology

* **Zero-Shot Inference:** The models are tasked with classifying or processing the news articles without any training examples.
* **Latency Calculation:** Each script feeds the specific dataset to the models and calculates the time taken for inference. This helps in understanding the real-time performance of these models on low-resource languages like Assamese.

# Repository Structure

The code is organized by domain to allow for modular evaluation:

```text
├── datasets/
│   ├── crime_law_justice.csv
│   ├── entertainment.csv
│   ├── health.csv
│   ├── politics.csv
│   └── sports.csv
├── benchmarks/
│   ├── benchmark_crime.py        # Latency test for Crime dataset
│   ├── benchmark_entertainment.py # Latency test for Entertainment dataset
│   ├── benchmark_health.py       # Latency test for Health dataset
│   ├── benchmark_politics.py     # Latency test for Politics dataset
│   └── benchmark_sports.py       # Latency test for Sports dataset
└── README.md
## cite as:
P. J. Baruah, A. Paul, V. S. Snehal, and T. Borah, "AND-2500: A Novel Assamese News Corpus and Comparative Benchmarking of Language Models," Computación y Sistemas, vol. 30, no. 3, pp. 1955–1966, 2026, doi: 10.13053/CyS-30-3-6206.
