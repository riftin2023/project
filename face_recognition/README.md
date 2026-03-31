# 🧠 Face Recognition using SVM and PCA

## 📌 Project Overview

This project implements a **Face Recognition System** using **Support Vector Machine (SVM)** along with **Principal Component Analysis (PCA)** for dimensionality reduction.

The model is trained on the **Labeled Faces in the Wild (LFW)** dataset and is capable of identifying individuals from facial images with optimized hyperparameters using Grid Search.

---

## 🚀 Features

* Face recognition using **SVM (RBF kernel)**
* Dimensionality reduction using **PCA (Eigenfaces)**
* Hyperparameter tuning with **GridSearchCV**
* Visualization of predictions with correctness indication
* Clean pipeline using `make_pipeline`

---

## 🛠️ Technologies Used

* Python
* Scikit-learn
* NumPy
* Matplotlib
* Seaborn
* Pandas

---

## 📂 Dataset

* **LFW (Labeled Faces in the Wild)**
* Automatically fetched using `fetch_lfw_people`
* Filtered with:

  * `min_faces_per_person = 60`

---

## ⚙️ How It Works

### 1. Load Dataset

* Load face images and labels
* Display sample images

### 2. Preprocessing

* Flatten images into feature vectors
* Split into training and testing sets

### 3. Feature Extraction

* Use **PCA** to reduce dimensionality
* Convert images into **Eigenfaces**

### 4. Model Training

* Use **SVM with RBF kernel**
* Handle class imbalance using `class_weight='balanced'`

### 5. Hyperparameter Tuning

* Optimize:

  * `C` (regularization)
  * `gamma` (kernel coefficient)
* Use **GridSearchCV** to find best parameters

### 6. Prediction

* Predict labels for test images

### 7. Visualization

* Display predictions
* Correct predictions → **Black**
* Incorrect predictions → **Red**

---

## 📊 Model Pipeline

```
Input Image
     ↓
PCA (Dimensionality Reduction)
     ↓
SVM (Classification)
     ↓
Predicted Person
```

---

## 📈 Example Output

* Displays a grid of test images
* Each image labeled with predicted name
* Incorrect predictions highlighted in **red**

---

## 🧪 How to Run

### 1. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### 2. Run the script

```bash
python your_script_name.py
```

---

## 📌 Key Concepts Used

* Support Vector Machines (SVM)
* Principal Component Analysis (PCA)
* Eigenfaces
* Hyperparameter Tuning
* Machine Learning Pipelines

---

## 👨‍💻 Author

* Developed as a Machine Learning project for face recognition

---

## ⭐ Acknowledgements

* Scikit-learn documentation
* LFW dataset contributors

---

## 📬 Feedback

Feel free to open issues or contribute to improve this project!
