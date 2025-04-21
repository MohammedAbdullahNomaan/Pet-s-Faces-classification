# Pet-s-Faces-classification
# 🐾 Pet Breed Classification using ResNet50

This project implements a pet breed image classification model using TensorFlow and transfer learning with ResNet50. It classifies images of different dog and cat breeds.

---

## 📁 Dataset

The dataset is expected to be placed inside the `./images/` directory.

- Image Format: `.jpg`
- Naming Convention: `<breed_name>_<index>.jpg`
  - Example: `beagle_1.jpg`, `Bombay_2.jpg`

---

## 🧠 Model Summary

- ✅ **Base Model**: ResNet50 (pre-trained on ImageNet, top layers removed)
- 🔄 **Augmentation**: Random flip and rotation
- 🔢 **Encoding**: Manual label encoding using a mapping
- 🧮 **Classifier**: Dense layer with softmax activation (15 classes)
- ⚙️ **Loss Function**: Categorical Crossentropy
- 🚀 **Optimizer**: Adam
- 📊 **Metrics**: Accuracy

---

## 🏗️ Architecture

1. Images resized to (224x224) and padded.
2. Augmentation using `RandomFlip` and `RandomRotation`.
3. Feature extraction via frozen ResNet50 base.
4. Output layer: Dense layer with 15 softmax outputs.

---

## 🔧 How to Run

### 1. Clone this repository
```bash
git clone https://github.com/yourusername/pet-breed-classification.git
cd pet-breed-classification

2. Install dependencies

pip install -r requirements.txt
3. Add images
Place your .jpg images in the images folder.

4. Train the model
python train_model.py
📈 Training Progress
The model is trained for 10 epochs. Training and validation accuracy/loss are plotted.

📉 Loss Curve

📈 Accuracy Curve

These graphs are displayed using matplotlib.

🧪 Evaluation
Test accuracy is calculated using:

python
model.evaluate(X_test, y_test)
Predictions on test data:

python
y_pred = model.predict(X_test)
🏷️ Label Mapping

Class	Breed
0	Abyssinian
1	american pit bull terrier
2	american bulldog
3	basset hound
4	beagle
5	Bengal
6	Bombay
7	British Shorthair
8	Egyptian Mau
9	boxer
10	chihuahua
11	english cocker spaniel
12	english setter
13	german shorthaired
14	great pyreness
15	Birman

📝 Notes
The label_encode function should ideally use a dictionary for better maintainability.

Ensure all labels in the image filenames are correctly spelled.

ResNet50 is used with frozen weights to prevent retraining the base model.

📦 Requirements
Create a requirements.txt with the following:

tensorflow
numpy
pandas
matplotlib
scikit-learn
Install with:


pip install -r requirements.txt

📬 Contact
For issues, suggestions, or improvements, feel free to open an issue or create a pull request on GitHub.
