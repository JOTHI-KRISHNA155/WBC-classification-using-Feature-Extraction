# WBC-classification-using-Feature-Extraction
📌 Methodology

This project combines Deep Learning and Machine Learning techniques to build a robust system for White Blood Cell (WBC) Classification.

🔹 Preprocessing & Segmentation

Image Preprocessing

Convert images into grayscale.

Apply Gaussian Blur to smooth the image.

Use OTSU’s thresholding to separate foreground (cells) from background.

Perform morphological operations to reduce noise.

Segmentation

The Watershed algorithm is applied for cell segmentation.

Extracted WBC cells are used for further feature processing.

🔹 Feature Extraction

The model employs a dual-feature strategy:

Deep Learning Features

Pre-trained VGG16 is used to extract high-level spatial features from WBC images.

Handcrafted Features

Shape-based and geometric features are extracted to improve robustness:

Area

Perimeter

Solidity

Aspect Ratio

Extent

🔹 Handling Class Imbalance

To counter class imbalance, SMOTE (Synthetic Minority Oversampling Technique) is applied during training.

This ensures balanced representation of all WBC types.

🔹 Classification

The extracted features (deep + handcrafted) are combined.

A LightGBM Gradient Boosting Classifier is trained on the balanced dataset.

This hybrid approach leverages both deep learned representations and domain-specific handcrafted features for improved accuracy.

🔹 Evaluation

The final model is evaluated using:

Accuracy Score

Classification Report (Precision, Recall, F1-Score)
Dataset Link: https://www.kaggle.com/datasets/masoudnickparvar/white-blood-cells-dataset
