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

