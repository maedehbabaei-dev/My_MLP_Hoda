Hoda 0-9 Digit Classification using MLP and Genetic Algorithm

📌 Overview

This project implements a Multi-Layer Perceptron (MLP) Neural Network optimized using a Genetic Algorithm (GA) for handwritten digit classification using the Hoda dataset.

The images are converted into numerical feature vectors and classified using a neural network. Instead of using gradient-based optimization, the neural network weights are optimized using a Genetic Algorithm.

«Important: Although the original dataset is known as Hoda 0-9, the dataset subset used in this experiment contains images from only four classes (0, 1, 2, and 3). Therefore, the results reported here represent a 4-class classification experiment, not the complete 10-class Hoda 0-9 dataset.»

---

🧠 Model Architecture

The project uses a Multi-Layer Perceptron with the following architecture:

Input Layer:      100 neurons
        ↓
Hidden Layer 1:    32 neurons
        ↓
Hidden Layer 2:    16 neurons
        ↓
Output Layer:      10 neurons

The input images are resized to 10 × 10 pixels, resulting in:

10 × 10 = 100 input features

The output layer uses Softmax for classification.

«Note: The network architecture contains 10 output neurons, but the current dataset subset used in this experiment contains only classes 0–3.»

---

🧬 Genetic Algorithm

A Genetic Algorithm is used to optimize the neural network weights.

GA Configuration

Parameter| Value
Population Size| 100
Maximum Generations| 600
Tournament Size| 3
Elite Fraction| 0.1
Mutation Rate| 0.1
Mutation Scale| 0.3
Crossover| Uniform Crossover
Early Stopping Patience| 30

Chromosome Representation

All neural network weights are flattened into a single chromosome.

The chromosome length is:

(100 × 32) + (32 × 16) + (16 × 10)

= 3200 + 512 + 160

= 3872

Therefore, each individual in the genetic algorithm represents 3,872 neural network weights.

---

📊 Dataset

The Hoda handwritten digit dataset is used for image classification.

Preprocessing

The images are processed using the following steps:

1. Load grayscale BMP images.
2. Resize each image to 10 × 10 pixels.
3. Flatten each image into a vector of 100 features.
4. Normalize pixel values to the range "[0, 1]".
5. Shuffle the dataset.
6. Split the data into training and validation sets.

Dataset Statistics

Total images:       544
Training images:    380
Validation images:  164

Input shape:
544 × 100

The current experiment contains four classes:

0, 1, 2, 3

---

📈 Training Results

The Genetic Algorithm was configured to run for a maximum of 600 generations.

However, early stopping was triggered at generation 72 because the validation accuracy did not improve for 30 consecutive generations.

Best Result

Best Validation Accuracy: 81.71%

The best validation accuracy was approximately 81.71%.

The training and validation accuracy curves show the improvement of the model during the genetic optimization process.

---

📋 Classification Report

The final validation results were:

Class| Precision| Recall| F1-score| Support
0| 0.91| 0.88| 0.90| 49
1| 0.84| 0.82| 0.83| 57
2| 0.72| 0.92| 0.81| 48
3| 0.00| 0.00| 0.00| 10
Accuracy| | | 0.82| 164
Macro Avg| 0.62| 0.65| 0.63| 164
Weighted Avg| 0.78| 0.82| 0.79| 164

The model performed best on class 0, while class 3 was not correctly predicted in the final validation set.

The zero precision and recall for class 3 occur because the model did not predict any validation samples as class 3.

---

📉 Confusion Matrix

The confusion matrix is used to analyze the predictions for each class and identify which digits are being confused with one another.

The results show that most of the classification errors are related to confusion between classes 1 and 2, while class 3 was particularly difficult for the model.

---

🛠️ Technologies

- Python
- NumPy
- Pandas
- OpenCV
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Genetic Algorithm
- Neural Networks / MLP

---

📁 Project Structure

Hoda-0-9-GA/
│
├── MyMLP_Hoda_GA.ipynb
├── mlp_hoda_ga_weights.npz
└── README.md

---

🚀 How to Run

1. Open the Notebook

Open:

MyMLP_Hoda_GA.ipynb

in Google Colab or Jupyter Notebook.

2. Prepare the Dataset

Place the Hoda images in the expected Google Drive directory:

/content/drive/MyDrive/Hoda 0-9/

3. Run the Notebook

Run the cells sequentially.

The notebook will:

Load images
    ↓
Preprocess images
    ↓
Create training/validation sets
    ↓
Build the MLP
    ↓
Initialize Genetic Algorithm
    ↓
Optimize neural network weights
    ↓
Evaluate validation performance
    ↓
Generate accuracy curves
    ↓
Generate confusion matrix
    ↓
Generate classification report

---

🎯 Project Goal

The main goal of this project is to explore the use of a Genetic Algorithm as an optimization method for neural network weights.

Instead of relying on traditional gradient descent, the Genetic Algorithm searches for neural network weight combinations that minimize the classification loss.

This project demonstrates the combination of:

Neural Networks
        +
Genetic Algorithms
        ↓
Image Classification

---

⚠️ Limitations

The current experiment has several limitations:

- Only 544 images were used.
- The available subset contains only four classes (0–3).
- The neural network has 10 output neurons, but the current experiment does not contain classes 4–9.
- Class 3 was not correctly predicted in the final validation results.
- The validation accuracy reached 81.71%, but the performance is not uniform across all classes.

A future version can use the complete Hoda 0-9 dataset to perform true 10-class digit classification.

---

🔮 Future Improvements

Possible improvements include:

- Using the complete Hoda 0-9 dataset.
- Including all ten digit classes (0–9).
- Increasing the image resolution.
- Tuning Genetic Algorithm parameters.
- Using a larger neural network.
- Comparing GA optimization with Gradient Descent.
- Testing different mutation and crossover strategies.
- Increasing the population diversity.

---

👩‍💻 Author

Developed by Maedeh Babaei

