## MRI_Image_Segmentation

<div align="center">
  <img src="https://github.com/HassanKhalil321/MRI_Image_Segmentation/blob/main/assets/model%20show.jpg" width="800" hight="400"/>
</div>


## Introduction

This project features a U-Net based deep learning model for MRI image segmentation. Using a single MRI image, it accurately segments a specific tissue type, enhancing medical image analysis to assist radiologists in diagnosis and treatment planning.

## Dataset

The Brain MRI segmentation dataset from Kaggle is a comprehensive collection of MRI scans specifically designed for the task of segmenting brain tissues. This dataset includes a variety of images with annotated labels, providing ground truth for different tissue types. It serves as an essential resource for training and evaluating machine learning models in medical image segmentation. The high-quality annotations and diversity of the scans make it ideal for developing robust and accurate segmentation algorithms.

## Model Overview

 ## Model Architecture

The U-Net architecture is composed of two main parts:

### Encoder (Contraction Path)
The encoder consists of several convolutional layers (Conv2D) followed by max-pooling layers (MaxPooling2D). Each convolutional block contains:
- **Conv2D**: Applies convolution operations to the input image to extract features.
- **MaxPooling2D**: Reduces the spatial dimensions of the feature maps, keeping the most important information.

### Decoder (Expansion Path)
The decoder is responsible for upsampling the encoded feature maps back to the original image size. Each block in the decoder path contains:
- **Conv2DTranspose**: Performs the reverse operation of convolution, increasing the spatial dimensions.
- **Concatenate**: Merges corresponding feature maps from the encoder path to retain high-resolution features.
- **Conv2D**: Refines the upsampled features to produce the final segmented output.

## Workflow

1. **Input Image**: An MRI scan of the brain is fed into the model.
2. **Encoder**: The image passes through the encoder, where convolutional layers extract features and pooling layers reduce dimensionality.
3. **Bottleneck**: The compressed feature maps are further processed in the bottleneck layer.
4. **Decoder**: The decoder upsamples the feature maps and concatenates them with the corresponding encoder outputs to restore the spatial dimensions.
5. **Output**: The final output is a segmented image highlighting the tumor regions.

## Loss
<div align="center">
  <img src="https://github.com/HassanKhalil321/MRI_Image_Segmentation/blob/main/assets/CCE.jpg" width="400"/>
</div>

## Results
<div align="center">
  <img src="https://github.com/HassanKhalil321/MRI_Image_Segmentation/blob/main/assets/testttt.png" alt="Gesture Recognition" width="500"/>
</div>
