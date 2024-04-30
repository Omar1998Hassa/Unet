# U-Net for Biomedical Image Segmentation

## Overview
This repository contains an implementation of the U-Net architecture for biomedical image segmentation. The U-Net architecture is widely used for tasks such as labeling neurons in electron microscopy images. This implementation includes the necessary components to build and train a U-Net model from scratch.

## Requirements
- Python 3.x
- PyTorch
- torchvision
- tqdm
- matplotlib
- scikit-image

## Usage
1. Clone this repository:
   ```
   git clone https://github.com/yourusername/unet-biomedical-segmentation.git
   cd unet-biomedical-segmentation
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Download the dataset (provide instructions or a link to the dataset).

4. Train the U-Net model:
   ```
   python train.py
   ```

5. Evaluate the trained model (if applicable):
   ```
   python evaluate.py
   ```

## Components
### 1. Contracting Block
This block performs two convolutions followed by a max pool operation, reducing the spatial dimensions while increasing the number of channels.

### 2. Expanding Block
This block performs an upsampling operation followed by a convolution, concatenation with the corresponding cropped feature map from the contracting path, and two additional convolutions.

### 3. Feature Map Block
The final layer of the U-Net architecture, which maps each pixel to the correct number of output channels using a 1x1 convolution.

### 4. U-Net Model
The overall U-Net model consists of four contracting blocks followed by four expanding blocks, with an upfeature layer
