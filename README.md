# Large Language Models’ Factuality Depends on the Language of Inquiry

This repo contains the code for our Benchmark.

## Directory Structure
- `generations` folder contains the generations for the models we mentioned in the paper on our dataset.
- `results` folder contains LLM evaluation results for all the models.
- `src` folder contains the scripts for generations and evaluations on our dataset.

## Setup and Usage Instructions for our Benchmark

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AggarwalTushar/multilingual_benchmark.git
   cd multilingual_benchmark

2. **Install dependencies:**
   
    Use env.yml to create a conda environment:
   ```bash
   conda env create -f environment.yml
   conda activate eval
   
3. **Run your model on the benchmark**
   Add your model path in the eval.sh file. Use the following command to run the file:
   ```bash
   bash eval.sh

## Model Performance Results

| Model | Associative | Unassociative | t-stat | p-value | FRS | KTS | X-FAKT |
|-------|-------------|---------------|---------|---------|-----|-----|---------|
| Meta-Llama-3-70B-Instruct | 2.36 ± 5.12 | 9.85 ± 10.54 | 2.52 | 0.01 | 0.076 | 0.118 | 0.092 |
| Gemma-27B | 4.23 ± 8.49 | 16.46 ± 17.07 | 2.54 | 0.01 | 0.046 | 0.076 | 0.057 |
| Phi-4 | 12.87 ± 16.51 | 30.15 ± 25.92 | 2.35 | 0.02 | 0.023 | 0.055 | 0.032 |
| Phi-3-medium-128k-Inst | 25.09 ± 29.84 | 55.57 ± 36.24 | 2.93 | <0.01 | 0.012 | 0.032 | 0.018 |
| Gemma-9B | 4.98 ± 6.09 | 22.32 ± 21.37 | 2.90 | <0.01 | 0.035 | 0.055 | 0.043 |
| Meta-Llama-3-8B-Instruct | 4.60 ± 7.54 | 25.77 ± 19.61 | 3.85 | <0.01 | 0.032 | 0.045 | 0.037 |
| Orca-2-7B | 31.95 ± 31.65 | 56.77 ± 32.99 | 2.60 | 0.01 | 0.011 | 0.039 | 0.017 |
| DeepSeek-7B-Chat | 31.49 ± 30.68 | 63.73 ± 36.29 | 3.09 | <0.01 | 0.010 | 0.030 | 0.015 |
| Mistral-7B-Instruct-v0.2 | 16.96 ± 15.65 | 45.25 ± 29.34 | 3.42 | <0.01 | 0.016 | 0.034 | 0.022 |
| Phi-3.5-mini-Inst | 41.85 ± 31.62 | 69.87 ± 31.23 | 3.09 | <0.01 | 0.009 | 0.034 | 0.014 |
| Phi-3-mini-128k-Inst | 42.45 ± 30.99 | 77.95 ± 33.72 | 3.65 | <0.01 | 0.008 | 0.027 | 0.013 |
| Llama-3.2-3B-Instruct | 24.10 ± 17.80 | 47.48 ± 26.80 | 3.07 | <0.01 | 0.014 | 0.041 | 0.021 |
| Gemma-2B | 9.97 ± 14.78 | 45.77 ± 31.30 | 4.06 | <0.01 | 0.018 | 0.027 | 0.021 |
| Llama-3.2-1B-Instruct | 34.74 ± 22.32 | 65.96 ± 26.98 | 4.03 | <0.01 | 0.010 | 0.031 | 0.015 |

Results show model performance based on:
- Associative and Unassociative errors (mean ± standard deviation)
- Factual Recall Score (FRS)
- Knowledge Transferability Score (KTS)
- Cross-Lingual Factual Knowledge Transferability Score (X-FAKT)

The values represent the percentage of incorrect samples average across all languages.
