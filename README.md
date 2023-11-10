# **Dementia-Classification-FFNN**

[LINK TO JUPYTER NOTEBOOK](https://github.com/Gavin-Thomas/Dementia-Classification-FFNN/blob/main/DementiaFFNN.ipynb)

### **Problem Description**
Dementia represents a significant and growing public health concern with substantial costs expected to rise significantly. Traditional diagnostic methods have shown to be inadequate, leading to underdiagnosis. The aim was to address this by developing a more accurate diagnostic tool using deep learning.
### **Solution Design**
A deep learning model was chosen for its proficiency in handling classification problems like dementia diagnosis. The model was built using Python and PyTorch, due to their extensive libraries and support for machine learning tasks. The decision was influenced by the availability of Electronic Health Record (EHR) data in tabular format from over 1.2 million Albertans over the age of 55.
### **Software Design / Planning**
The software was planned with a focus on preprocessing the EHR data, which involved converting formats, handling missing values, encoding categorical variables, normalizing counts, and addressing data imbalance with Synthetic Minority Over-sampling Technique (SMOTE). Pseudocode and flow diagrams were used to outline this process before implementation.
### **Software Production**
The biggest challenge was computational limitations, which were mitigated by utilizing the Advanced Research Computing (ARC) facility. A key learning was implementing a feedforward neural network with batch normalization and dropout to prevent overfitting.
### **Testing**
Testing involved validating the model's performance with a holdout dataset and tuning based on loss and accuracy metrics. The model underwent rigorous testing, using strategies like confusion matrix analysis and Receiver Operating Characteristic (ROC) curve assessment to ensure robustness.
### **Output**
The code executes and produces a binary classification output to identify dementia cases. However, it currently has low precision, indicating a tendency to overdiagnose, which is an area for future improvement.
### **Code**
The code, which is included in the appendix, was developed with emphasis on readability and adhering to coding standards.
### **Challenges and Solutions**
While the program does not execute flawlessly, with a precision of 15%, the report details the challenges faced and solutions implemented, including future strategies to improve precision such as adjusting the decision threshold and exploring ensemble methods.
![image](https://github.com/Gavin-Thomas/Dementia-Classification-FFNN/assets/123608443/866a4f24-0108-40c3-8170-36798f4547bd)
