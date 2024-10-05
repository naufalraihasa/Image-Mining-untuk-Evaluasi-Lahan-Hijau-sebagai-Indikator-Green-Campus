---

# Action - Image Mining for Green Campus Evaluation

### Overview

This project was developed as part of the **Academic Competition of Data Science (ACTION)**, hosted by **UNESA**. The goal of this project is to utilize image mining techniques with deep learning, specifically convolutional neural networks (CNN), to evaluate green areas as indicators of a green campus. Using **Google Earth** satellite imagery, the project aims to classify green areas and estimate the total green space on campus, which is critical for sustainable campus development.

### Objectives
1. **Develop a CNN-based model** for identifying green campus areas from satellite images.
2. **Evaluate the model’s performance** in classifying green vs non-green areas.
3. **Provide insights** on the proportion of green space in Universitas Airlangga using Google Earth imagery, supporting the campus’s sustainability initiatives.

### Dataset
The dataset consists of satellite images from **Google Earth**, specifically focused on the campus of **Universitas Airlangga**. Images were preprocessed and categorized into green and non-green areas. Preprocessing steps included image resizing, normalization, and segmentation into smaller patches.

- **Image dimensions**: 1280x720 pixels (chopped into 128x128 pixels)
- **Classes**: Green area, Non-green area
- **Format**: `.jpg` and `.png` images
- **Source**: Google Earth

### Methodology

#### 1. **Model Architecture**  
Several models were used in the competition:

- **Basic CNN**: A custom CNN with three convolutional layers followed by max-pooling and dropout layers to prevent overfitting.
- **Transfer Learning Models**:
  - **ResNet50**
  - **InceptionV3**
  - **MobileNetV2**
  
  These models were pre-trained on ImageNet and used with their top layers removed. Custom classification layers were added on top.

#### 2. **Training and Evaluation**  
The training process was done using **Google Colab**, with GPUs to speed up the process. The models were trained for 25 epochs with a batch size of 64 images. The dataset was split into **80% training** and **20% testing**.

- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy (since it’s a binary classification problem)
- **Metrics**: Accuracy

#### 3. **Preprocessing**  
Each image from Google Earth was preprocessed before being fed into the model. This included:

...

### Results

....

### Files

- `Makalah Data Mining Action (DanDADan).pdf`: The official research paper submitted for the competition.
- `Action_Unesa_Code.ipynb`: Jupyter Notebook containing the code for data loading, model training, and evaluation.
