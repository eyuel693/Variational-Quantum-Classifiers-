
# **Variational Quantum Classifier (VQC) for Medical Risk Prediction**

This project implements a **Variational Quantum Classifier (VQC)** to classify patient risk using a hybrid classical–quantum learning pipeline. The model combines classical preprocessing (PCA) with a trainable quantum circuit built using **PennyLane**, optimized through **PyTorch**.

---

## ** Project Overview**

The goal is to classify patient data into **low-risk** and **high-risk** categories using a quantum-enhanced model.
The workflow includes:

* Classical preprocessing
* Quantum feature encoding
* Variational quantum circuit training
* Hybrid optimization
* Performance visualization (loss, accuracy, decision boundary, entanglement analysis)

---

## ** Key Components**

### **1. Data Preprocessing**

* PCA reduces the dataset to **4 components** → mapped to **4 qubits**.
* Encodes classical values into rotation angles.

### **2. Quantum Circuit Design**

* **Feature Map:** 
* **Ansatz Layers:**

### **3. Entanglement**

* CNOT gates create correlations between qubits.
* Without entanglement, the model becomes linear; with it, the VQC learns non-linear boundaries.

### **4. Forward Pass**

1. Encode PCA features into qubits
2. Apply trainable ansatz
3. Measure ⟨Z⟩ on qubit 0
4. Convert to probability → used for loss & optimization

### **5. Optimization**

* Gradients computed using **Parameter-Shift Rule**:
* Optimizer: **Adam**

---

## ** Results Summary**

* **Loss decreases quickly** → effective optimization
* **Validation accuracy stabilizes around 83–84%**
* **No overfitting** (training & validation loss close)
* **Decision boundary** shows clear nonlinear separation in PCA space
* **Entanglement analysis** confirms useful quantum correlations

---

## ** Visualizations**

* Loss & accuracy curves
* Decision boundary heatmap
* Single-qubit entanglement entropies
* Qiskit circuit diagrams

---

## ** Technologies Used**

* **PennyLane**
* **PyTorch**
* **Qiskit**
* **NumPy / SciPy**
* **Matplotlib**


