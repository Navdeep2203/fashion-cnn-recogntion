# 🧠 Deep Learning Fashion Item Recognition  
### CNN-based Image Classification using PyTorch

This project implements a **Convolutional Neural Network (CNN)** using PyTorch to classify clothing items from the Fashion-MNIST dataset.  
The model is trained on **70,000 grayscale images across 10 clothing categories** and achieves **~91% test accuracy**.

The project demonstrates a complete **deep learning pipeline**, including data preprocessing, model training, evaluation, hyperparameter experimentation, and misclassification analysis.

---

# 📂 Dataset

The **Fashion-MNIST dataset** contains:

| Property | Value |
|--------|------|
Training Images | 60,000 |
Test Images | 10,000 |
Image Size | 28 × 28 |
Classes | 10 |

### Clothing Categories
0 → T-shirt/top
1 → Trouser
2 → Pullover
3 → Dress
4 → Coat
5 → Sandal
6 → Shirt
7 → Sneaker
8 → Bag
9 → Ankle Boot


---

# 🏗 Model Architecture

The classifier is a **Convolutional Neural Network** composed of:
Input Image (1 × 28 × 28)

Conv2D (1 → 32) + ReLU
MaxPooling

Conv2D (32 → 64) + ReLU
MaxPooling

Conv2D (64 → 128) + ReLU
MaxPooling

Flatten

Fully Connected Layer (128)
ReLU

Output Layer (10 classes)


This architecture enables the model to learn **hierarchical visual features** such as edges, shapes, and textures.

---

# ⚙️ Training Configuration

| Parameter | Value |
|----------|------|
Optimizer | Adam |
Loss Function | CrossEntropyLoss |
Batch Size | 64 |
Epochs | 5 |
Learning Rate | 0.001 |

The model was trained using the **Adam optimizer** to efficiently update network weights during backpropagation.

---

# 📊 Results

### Test Accuracy
~91%

The CNN performs well across most classes, particularly on visually distinct items such as:

- Trouser
- Bag
- Sneaker
- Sandal
- Ankle Boot

---

# 📉 Confusion Matrix

The confusion matrix was used to evaluate classification performance across all classes.


Example insights:

- **T-shirts and shirts** are occasionally confused due to similar visual patterns.
- **Pullovers and coats** sometimes overlap in predictions.
- Distinct categories like **bags and trousers** are classified with very high accuracy.

---

# 🔬 Hyperparameter Experimentation

Several hyperparameters were tested to improve model performance.

### Learning Rate Experiment

| Learning Rate | Accuracy |
|---------------|---------|
0.01 | ~85% |
0.001 | **~91%** |
0.0005 | ~89% |

Best performance was achieved with:
Learning Rate : 0.001

# 🔎 Misclassification Analysis

Misclassified samples were analyzed to understand model limitations.

Common misclassifications include:

- **Shirt → T-shirt**
- **Pullover → Coat**

These errors occur because upper-body clothing items share similar visual structures in grayscale images.


---

# 🛠 Technologies Used

- Python  
- PyTorch  
- NumPy  
- Matplotlib  
- Seaborn  
- OpenCV  

-

# 🚀 Future Improvements

Possible extensions for this project include:

- Real-time classification using webcam input with OpenCV  
- Training deeper CNN architectures  
- Applying data augmentation techniques  
- Deploying the model using a web application (Streamlit or Flask)

---

# 👤 Author

**Navdeep Singh**  
CSE Student — MIT Manipal  

GitHub:  


