# Brain MRI Segmentation 🧠 ![license](https://img.shields.io/github/license/Pegah-Ardehkhani/Brain-MRI-Segmentation.svg) ![releases](https://img.shields.io/github/release/Pegah-Ardehkhani/Brain-MRI-Segmentation.svg) <a href="https://colab.research.google.com/github/Pegah-Ardehkhani/Brain-MRI-Segmentation/blob/main/Brain%20MRI%20Segmentation.ipynb" target="_parent\"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> [![nbviewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](http://nbviewer.org/github/Pegah-Ardehkhani/Brain-MRI-Segmentation/blob/main/Brain%20MRI%20Segmentation.ipynb)

<p align="center">
  <img width="500" height="300" src="https://mateuszbuda.github.io/images/brainseg/CS_6668.gif">
</p>

## Dataset 📔

[Kaggle link: Brain Tumor Data](https://www.kaggle.com/mateuszbuda/lgg-mri-segmentation)

The dataset used for development was obtained from The Cancer Imaging Archive (TCIA) and involved 110 cases of lower-grade glioma patients. Registers brain MR images with manual FLAIR abnormality segmentation masks are published as a Kaggle Dataset lgg-mri-segmentation.

## Project Overview 

**U-net:**

U-net from scratch has been written.

Key aspects of U-Net:

1. Convolution Layers: Convolution operation are used to learn information from images which then can be used as features for machine learning problems.

2. Down Sampling: Sequence of convolution combined with max pooling results in down sampling. In down sampling, size of the image is reduced which means we can observe larger portion of image in a single convolution operation. Down sampling is a good approach for identifying what is present in the image but for identifying where the object is we need to use upsampling.

3. Up Sampling: It is just opposite of down sampling. We go from low resolution to high resolution. For up sampling U-Net uses transposed covolution which is achieved by taking transpose of filter kernels and reversing the process of convolution.

Following picture gives a clear picture of What a U-Net is.

<p align="center">
  <img width="1000" height="500" src="https://theaisummer.com/static/3995761ad87f8909f5dec5925d182e80/4ff83/The-3D-Unet-model.png">
</p>

**Reustls:**

<p align="center">
  <img width="800" height="400" src="https://github.com/Pegah-Ardehkhani/Brain-MRI-Segmentation/blob/main/model%20history.PNG">
</p>

Dice Score on the test data: 0.9027

<p align="center">
  <img width="1000" height="300" src="https://github.com/Pegah-Ardehkhani/Brain-MRI-Segmentation/blob/main/original%20and%20pred.PNG">
</p>
