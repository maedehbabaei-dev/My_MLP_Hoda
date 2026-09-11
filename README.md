# My_MLP_Hoda
Handwritten digit recognition using a custom NumPy MLP and Genetic Algorithm.

# Hoda0_9 Digit Classification (MLP + Genetic Algorithm)

This project focuses on recognizing digits from the Hoda0_9 dataset using two fully custom neural network implementations:

1. MLP (Gradient Descent) — a multi-layer perceptron built entirely from scratch using NumPy  
2. MLP with Genetic Algorithm (GA) — weight optimization using evolutionary search

Both models are implemented without any deep learning frameworks.

---

## Dataset: Hoda0_9

- Name: Hoda0_9  
- Format: Excel  
- Type: Persian handwritten digits (0–9)  
- Features: numeric pixel values  
- Target: digit label (0–9)

The dataset is large and cannot be uploaded to GitHub.  
It should be downloaded separately and placed inside the data/ directory as:

data/Hoda0_9.xlsx


The dataset is normalized, shuffled, and split into training and validation sets before training.

---

## Model Architectures

### MLP (Gradient Descent)
A fully custom neural network implemented using NumPy:
- Activation: Sigmoid  
- Loss: Mean Squared Error (MSE)  
- Optimization: Gradient Descent + Momentum  
- Batch-based training  
- Output plots (MSE & Accuracy) will be added later

### MLP with Genetic Algorithm (GA)
Neural network weights are flattened into a chromosome and optimized using GA:
- Selection: Tournament  
- Crossover: Uniform  
- Mutation: Gaussian noise  
- Fitness function: 1 / (1 + loss)  
- GA logs and comparison plots will be added later

---

## Project Structure
Hoda_project/ ├─ data/ │  └─ Hoda0_9.xlsx   ← (download separately) ├─ notebooks/ │  ├─ Hoda_MLP.ipynb │  └─ Hoda_GA.ipynb ├─ images/ │  ├─ hoda_mlp_mse.png │  ├─ hoda_mlp_acc.png │  ├─ hoda_ga_vs_gd.png │  └─ hoda_ga_log.png └─ README.md

---

## Author
Developed by Maedeh Babaei
