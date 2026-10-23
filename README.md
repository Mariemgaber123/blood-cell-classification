# Blood Cell Classification using Deep Learning

## Overview

This project focuses on classifying blood cell images into eight different classes using deep learning. It was developed as part of the **FCDS-AU Fall'26 Deep Learning Assignment**.

The project explores Convolutional Neural Networks (CNNs) and several training strategies to improve classification performance and generalization.

## Dataset

The dataset contains small RGB images of blood cells and is organized into training and test sets.

- **Training samples:** 13,673
- **Test samples:** 3,419
- **Image dimensions:** 28 × 28 pixels
- **Image channels:** RGB
- **Number of classes:** 8

The dataset includes `train.csv`, `sample_submission.csv`, a `train/` directory, and a `test/` directory.

> The competition dataset is not included in this repository. Please obtain it through the original competition source.

## Project Workflow

The project follows a typical deep learning workflow:

1. **Data Loading and Exploration** — Loading the dataset, examining labels, and understanding the image structure.
2. **Preprocessing** — Preparing image data and labels for model training.
3. **Model Development** — Building CNN-based architectures for multiclass image classification.
4. **Training and Validation** — Training models and evaluating their performance on validation data.
5. **Experimentation** — Testing different strategies to improve model performance.
6. **Inference and Submission** — Generating predictions for the test set and preparing a competition submission file.

## Experiments & Model Improvements

Several experiments were conducted to investigate how different training strategies affect classification performance.

### 1. Baseline Model

A baseline CNN was trained to establish a reference point for evaluating subsequent improvements.

### 2. Class Weighting

Class weights were introduced into the loss function to give different importance to classes during training and investigate their effect on classification performance.

### 3. Data Augmentation

Image augmentation was explored to expose the model to variations in the training images and help improve generalization.

### 4. Combined Improvements and Learning-Rate Adjustments

Class weighting and data augmentation were evaluated together, alongside learning-rate adjustments, to investigate whether combining these strategies could improve validation performance.

### 5. Label Smoothing

Label smoothing was explored as a modification to the classification loss function to reduce overconfident predictions and potentially improve generalization.

### 6. Test-Time Augmentation (TTA)

Test-Time Augmentation was used to combine predictions from multiple versions of an image, including the original image and horizontally and vertically flipped versions.

The softmax probabilities from these versions were averaged to produce the final predictions.

### 7. Model Architecture Experiments

Different CNN configurations were evaluated, including a deeper CNN architecture, to examine the relationship between model architecture and classification performance.

Experiments were compared using **validation accuracy** and **Macro F1-score**, with the goal of improving overall classification performance.

## Results

The strongest recorded validation results from the experiments were:

| Metric | Best Recorded Result |
|---|---:|
| Validation Accuracy | 97.70% |
| Validation Macro F1-score | 97.62% |

These results were obtained using Test-Time Augmentation with the evaluated model.

**Note:** These are validation results, not confirmed competition leaderboard scores. The final competition score may differ.

## Technologies Used

- Python
- PyTorch
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- PIL / image-processing utilities

## Repository Structure

```text
Blood-Cell-Classification/
│
├── README.md
├── blood_cell_classification.ipynb
└── .gitignore
```

The notebook filename above is illustrative; replace it with the actual filename in the repository.

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Mariemgaber123/Blood-Cell-Classification.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Blood-Cell-Classification
   ```

3. Install the required libraries:

   ```bash
   pip install torch torchvision numpy pandas matplotlib scikit-learn pillow
   ```

4. Download the competition dataset from its original source and place the files in the directory structure expected by the notebook.

5. Open the notebook in Jupyter Notebook, JupyterLab, or Google Colab and update the dataset path to match your environment.

6. Run the notebook cells to reproduce the experiments and generate predictions.

## Key Takeaways

- Built and evaluated CNN models for multiclass image classification.
- Explored class weighting and data augmentation as training strategies.
- Investigated learning-rate adjustments and label smoothing.
- Evaluated a deeper CNN architecture.
- Applied Test-Time Augmentation to combine predictions from transformed images.
- Compared models using validation accuracy and Macro F1-score.

## Author

**Mariem Gaber**

- **GitHub:** https://github.com/Mariemgaber123
- **LinkedIn:** https://www.linkedin.com/in/mariem-gaber-b380bb375

---

*Developed as part of the FCDS-AU Fall'26 Deep Learning Assignment.*