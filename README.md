# TOPSIS-Based Model Evaluation for Text Classification

## Overview
This project evaluates different pre-trained transformer-based models for text classification using a small IMDb review dataset. The evaluation is based on **accuracy, F1-score, and inference time**. The final ranking is determined using the **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** method.

## Features
- Evaluates models from the **Hugging Face Transformers** library.
- Computes **Accuracy, F1-score, and Inference Time**.
- Uses **TOPSIS** for multi-criteria decision making.
- Saves results as a **CSV file** (`topsis_results.csv`).
- Generates a **bar chart** (`topsis_ranking.png`) ranking models based on their TOPSIS scores.

## Models Evaluated
- `distilbert-base-uncased-finetuned-sst-2-english`
- `roberta-base`
- `bert-base-uncased`

## Dependencies
Ensure you have the following installed:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn transformers
```

## Running the Script
Run the Python script to evaluate the models:

```bash
python model_evaluation.py
```

### Expected Output
- A CSV file (`topsis_results.csv`) containing model performance metrics.
- A bar chart (`topsis_ranking.png`) visualizing model rankings.
- Console output explaining the best model and its strengths.

## Explanation of Metrics
- **Accuracy**: Measures how many predictions are correct.
- **F1-score**: Balances precision and recall.
- **Inference Time**: Measures how fast a model processes text.
- **TOPSIS Score**: Determines the best model by considering all metrics.

## Example Results
| Model | Accuracy | F1-score | Inference Time (sec) | TOPSIS Score |
|--------|----------|----------|-----------------|--------------|
| `distilbert-base` | 0.90 | 0.89 | 0.05 | 0.82 |
| `roberta-base` | 0.88 | 0.87 | 0.07 | 0.79 |
| `bert-base` | 0.86 | 0.85 | 0.09 | 0.75 |

**Conclusion**: The best model is selected based on the highest **TOPSIS Score**.

## Author
Developed by **Aarushi Gupta (Roll nNo. 102216107)**

