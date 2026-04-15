# 🍎 Fruits‑360 CNN Classification

A custom convolutional neural network (CNN) built to classify fruit images from the Fruits‑360 dataset into 257 classes. This project demonstrates an end‑to‑end deep learning workflow: data loading, preprocessing, model design, training, evaluation, error analysis, and single‑image inference.

### 📌 Project Overview
This project trains a CNN from scratch to recognize fruits based on color, shape, and texture. With 257 categories and over 180,000 images, the dataset challenges the model to distinguish between visually similar fruits (e.g., Apple Red 1 vs. Apple Red 2).

**Final Model Performance**

- **94.3% accuracy** on the full 257‑class test set

- Strong generalization across fruit types

- Clear misclassification patterns between visually similar fruits

### 🧠 Model Architecture

#### A custom CNN built with TensorFlow/Keras:

- 3× convolution + max‑pooling blocks

- Flatten → Dense(256) → Dense(128) → Dense(64)

- Dropout for regularization

- Softmax output layer with 257 units

- Adam optimizer (learning rate = 0.0001)

- EarlyStopping to prevent overfitting

### 📂 Dataset

**Fruits‑360 (Kaggle)**

- 257 fruit classes

- 135,071 training images

- 45,008 test images

- All images resized to 150×150 and normalized to 0–1

### 🚀 Training

**Training pipeline:**

- ImageDataGenerator for loading and preprocessing

- Batch size: 16

- Input size: 150×150×3

- EarlyStopping with restore_best_weights=True

- Accuracy and loss curves plotted for both train and validation sets

### 📊 Evaluation

**The model achieved:**

- Test Accuracy: 94.3%

- Test Loss: 0.53

A confusion‑matrix‑based analysis identified the Top 10 most confused class pairs, highlighting where the model struggles (mostly between visually similar fruits).

### 🔍 Single Image Prediction

A single image from the Test set was passed through the model.

**The model correctly predicted:**

- Apple Red 1

This confirms the end‑to‑end inference pipeline works as expected.

### 💾 Saved Model

**The trained model is saved as:**

- fruit_cnn_model.keras

This allows for future inference, fine‑tuning, or deployment.

### 🧭 Next Steps

**Potential improvements:**

- Transfer learning (MobileNet, EfficientNet)

- Increase input resolution to 224×224

- Stronger augmentation

- Class‑balanced sampling

- Deploy as a simple web app or API

### 📝 Files in This Repository

[Fruits-360 CNN.ipynb](./Fruits-360%20CNN.ipynb) — full training notebook

[fruit_cnn_model.keras](./fruit_cnn_model.keras) — saved trained model

[README.md](./README.md) — project overview (this file)
