# Breast Cancer Detection - Deep Learning

## Project Overview
Breast cancer is a significant health issue, with early detection being crucial for improving survival rates. This project focuses on developing a deep learning algorithm to support radiologists in analyzing mammographic images, reducing false negatives, and enhancing diagnostic accuracy. The primary goal is to assist in distinguishing between pathological and non-pathological cases, thereby improving the effectiveness of mammography as a screening tool. The project used the DDSM (Digital Database for Screening Mammography) dataset, which includes labeled images of calcifications and masses, categorized into benign, malignant, and non-pathological findings.

## Model Architecture 
The best-performing model was a customized version of the __VGG16 architecture__, pre-trained on the ImageNet dataset. The model's design included:
- __13 Convolutional Layers:__ Using 3x3 filters for feature extraction.
- __Max-Pooling Layers:__ Integrated for down-sampling and dimensionality reduction.
- __Modified Dense Layers:__ Adjusted to a smaller output size with a single node for binary classification, using a sigmoid activation function for distinguishing between pathological and non-pathological cases.
- __Regularization Techniques:__ Employed data augmentation and pre-training to improve model robustness.
- __Training Strategy:__ Utilized early stopping to prevent overfitting, with hyperparameter tuning for optimal performance.

## Conclusions 
- __🔍 Model Performance:__ The customized VGG16 model achieved an accuracy of 87% on the test set and an AUC (Area Under the Curve) of 0.933, surpassing benchmarks and demonstrating reliable diagnostic capabilities.
- __🩺 Clinical Relevance:__ Sensitivity was prioritized over specificity to minimize false negatives, which is critical in breast cancer detection. The chosen threshold maximized clinical benefits, increasing true positive rates at the cost of a controlled increase in false positives.
- __💡 Model Strengths:__ This project balanced model development and clinical analysis effectively, identifying a robust model while considering real-world medical application needs.

## Future Improvements
- __Categorical Classification:__ Extend the model to predict BI-RADS scores, providing more detailed classifications beyond binary outputs. This could include adding an explanatory component that highlights why a specific score was assigned, increasing transparency and trust among radiologists.
- __Enhanced Features:__ Integrate additional patient data such as breast tissue density, which plays a crucial role in breast cancer assessment. Including such features could significantly boost the model’s accuracy.
