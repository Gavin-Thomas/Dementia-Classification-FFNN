# **Dementia-Classification-FFNN**

<img src="https://github.com/Gavin-Thomas/Dementia-Classification-FFNN/blob/main/misc/DallE-Neuron.png?raw=true" width="300">

[LINK TO JUPYTER NOTEBOOK](https://github.com/Gavin-Thomas/Dementia-Classification-FFNN/blob/main/DementiaFFNN.ipynb)

### 1. Problem Description
Recent studies indicate a significant underdiagnosis of dementia using traditional diagnostic methods, such as cognitive evaluations and neurological tests, which often lack precision and efficiency [1, 3]. The emergence of artificial intelligence (AI), particularly Machine Learning (ML) and its subset Deep Learning (DL), offers promising avenues for enhancing diagnostic accuracy [4]. DL, with its capability to model complex neural structures, has shown potential for superior predictive abilities compared to traditional methods [4].

This project is driven by the need to develop a more accurate diagnostic tool for dementia, leveraging deep learning techniques. Given the rising prevalence and associated costs of dementia, there is a pressing need for more efficient and precise diagnostic methods.

### 2. Solution Design & Rationale
The project utilizes a deep learning model, specifically designed for classification tasks such as dementia diagnosis. Python and PyTorch were selected for their extensive libraries and strong support in machine learning, complemented by the availability of past Electronic Health Record (EHR) data of over 1.2 million Albertans aged 55 and above, formatted in tables.

This project serves as a precursor to my thesis, which will focus on a multi-class classification problem of dementia type and severity using multimodal data. This includes both structured tabular data, similar to what was used in this project (though not the same dataset), and unstructured free text data from clinical patient notes. To build a foundation for this more complex thesis project, I started with a simpler unimodal binary dementia classifier using deep learning, aiming to grasp the basics and ensure the model's code is functional.

### 3. Software Design / Planning
The project began with converting a dataset from SAS file format to CSV, utilizing pandas for data manipulation and SAS7BDAT for reading SAS files. A function was created to convert SAS files to CSV, ensuring proper file management and converting the data into a pandas DataFrame, which was then saved as a CSV file without row indices.

The dataset underwent refinement, with irrelevant columns being dropped to streamline the data. Data types of each column were checked for consistency, and missing values were addressed. The 'GENDER' column was processed using one-hot encoding to convert categorical data into a format more suitable for statistical models. This processed data was then concatenated with the original DataFrame, replacing the initial 'GENDER' column. The cleaned data was saved as a new CSV file for further use. For my Master’s project, I will use a more recent dataset that includes considerations for sex/gender, incorporating pronouns, gender identity, and biological sex, including intersex.

Prior to model training, the class distribution in the training and test sets was examined to ensure a balanced dataset, crucial for unbiased predictions. The data preparation for machine learning included normalizing specific columns, addressing class imbalance with SMOTE (Synthetic Minority Over-sampling Technique), and splitting the dataset into training and test sets, which were then converted into PyTorch tensors.

The core phase involved training a feedforward neural network, setting up a loss function and optimizer, and implementing data batching, loss calculation, accuracy tracking, learning rate adjustments, and model saving. Batch normalization and dropout techniques were incorporated to enhance performance and prevent overfitting.

The model's performance was evaluated using ROC curves and confusion matrices to assess its class differentiation ability and overall predictive accuracy.

### 4. Software Production
The project faced computational limitations, which were overcome by using the Advanced Research Computing (ARC) facility. A persistent challenge is the model's lack of precision, or high type 1 error, leading to overdiagnosis in some cases.

Key learning points included implementing a feedforward neural network with batch normalization and dropout layers, using SMOTE for class imbalance, and applying one-hot encoding for birth-sex data.

### 5. Testing
Routine checks were performed on dataset headers, column titles, and datatypes during data preprocessing. The model's performance was validated using holdout data (80% training, 20% validation) and tuned based on loss and accuracy metrics. Testing strategies included confusion matrix analysis and Receiver Operating Characteristic (ROC) curve assessment, using Visual Studio Code and Jupyter notebooks for error detection and code breakdown.

### 6. Output
The code successfully executes, providing a binary classification output for potential dementia cases. However, the current version exhibits a high type 1 error, indicating a tendency towards overdiagnosis, which will be a focus for improvement in my Master’s project.

### 7. Challenges and Solutions
Challenges included class imbalance (addressed with SMOTE), beginner-level machine learning skills (mitigated through practice), computational limits (overcome with NVIDIA v100 GPU on ARC cluster), lack of precision (ongoing issue), uncertainty in optimizer and loss function choice (seeking expert advice), handling sensitive data (resolved by anonymizing data), and preventing overfitting (addressed with batch normalization and dropout).

### Appendix
Due to data privacy, only the Jupyter notebook and the preprocessed CSV file are available on Github.

### References
- [1] Shao Y, et al. BMC Med Inform Decis Mak 2019;19:128.
- [2] Arvanitakis Z, et al. JAMA 2019;322:1589.
- [3] Woodford HJ, George J. QJM 2007;100:469–84.
- [4] Janiesch C, et al. Electron Mark 2021;31:685–95.

