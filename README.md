# CodeAlpha_HandwrittenCharacterRecognition

## 📌 Objective
Recognize handwritten digits (0-9) from grayscale images using a Convolutional Neural Network (CNN). This project is submitted as **Task 3: Handwritten Character Recognition** for the CodeAlpha Machine Learning Internship.

## 📊 Dataset
- **Source:** MNIST (built into `tensorflow.keras.datasets`, no manual download needed)
- **Size:** 60,000 training images + 10,000 test images
- **Image format:** 28x28 pixel grayscale
- **Classes:** 10 (digits 0-9)

## ⚙️ Approach
1. **Data Loading** — loaded MNIST directly via Keras' built-in dataset loader.
2. **Preprocessing** — normalized pixel values to the 0-1 range, reshaped images to include a channel dimension, one-hot encoded the 10 digit labels.
3. **Model Architecture** — built a CNN with:
   - 3 convolutional layers (32, 64, 64 filters) with ReLU activation
   - 2 max-pooling layers for downsampling
   - A dense layer (64 units) with dropout (0.5) to reduce overfitting
   - A softmax output layer for 10-class classification
4. **Training** — trained for 10 epochs with a 90/10 train/validation split, batch size 128, Adam optimizer.
5. **Evaluation** — measured test accuracy, precision, recall, F1-score (per class) and visualized a confusion matrix.
6. **Visualization** — sample digit images, training accuracy/loss curves, confusion matrix, and sample predictions.

## 🏆 Results
- **Test Accuracy:** XX.XX%
- High precision and recall across all 10 digit classes
- The confusion matrix shows that most misclassifications occur between visually similar digits

## 📁 Files in this repo
- `handwritten_digit_recognition.py` — full training & evaluation script
- `sample_digits.png` — example digits from the training set
- `training_history.png` — accuracy/loss curves over training epochs
- `confusion_matrix.png` — confusion matrix on test data
- `sample_predictions.png` — sample correct/incorrect predictions
- `handwritten_digit_cnn_model.keras` — saved trained model

## ▶️ How to Run
```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
python handwritten_digit_recognition.py
```

## 🔧 Tools & Libraries
Python, TensorFlow/Keras, NumPy, Scikit-learn, Matplotlib, Seaborn

## 🎓 Internship
This project was completed as part of the **CodeAlpha Machine Learning Internship**.
🔗 [www.codealpha.tech](https://www.codealpha.tech)
