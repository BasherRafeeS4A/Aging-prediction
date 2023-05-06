# Only a Matter of Style: Age Transformation Using a Style-Based Regression Model (SIGGRAPH 2021)

> The  task of age transformation illustrates the change of an individual's appearance over time. Accurately modeling this complex transformation over an input facial image is extremely challenging as it requires making convincing and possibly large changes to facial features and head shape, while still preserving the input identity. In this work, we present an image-to-image translation method that learns to directly encode real facial images into the latent space of a pre-trained unconditional GAN (e.g., StyleGAN) subject to a given aging shift. We employ a pre-trained age regression network used to explicitly guide the encoder to generate the latent codes corresponding to the desired age. In this formulation, our method approaches the continuous aging process as a regression task between the input age and desired target age, providing fine-grained control on the generated image. Moreover, unlike other approaches that operate solely in the latent space using a prior on the path controlling age, our method learns a more disentangled, non-linear path. We demonstrate that the end-to-end nature of our approach, coupled with the rich semantic latent space of StyleGAN, allows for further editing of the generated images. Qualitative and quantitative evaluations show the advantages of our method compared to state-of-the-art approaches.

<a href="https://arxiv.org/abs/2102.02754"><img src="https://img.shields.io/badge/arXiv-2008.00951-b31b1b.svg" height=22.5></a>
<a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" height=22.5></a>

<a href="https://www.youtube.com/watch?v=zDTUbtmUbG8"><img src="https://img.shields.io/static/v1?label=Two Minute Papers&message=SAM Video&color=red" height=22.5></a>  
<a href="https://youtu.be/X_pYC_LtBFw"><img src="https://img.shields.io/static/v1?label=SIGGRAPH 2021 &message=5 Minute Video&color=red" height=22.5></a>  
<a href="https://replicate.ai/yuval-alaluf/sam"><img src="https://img.shields.io/static/v1?label=Replicate&message=Demo and Docker Image&color=darkgreen" height=22.5></a>


Inference Notebook: &nbsp;<a href="http://colab.research.google.com/github/yuval-alaluf/SAM/blob/master/notebooks/inference_playground.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" height=22.5></a>  
Animation Notebook: <a href="http://colab.research.google.com/github/yuval-alaluf/SAM/blob/master/notebooks/animation_inference_playground.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" height=22.5></a>


<p align="center">
<img src="docs/teaser.jpeg" width="800px"/>
</p>

## Description   
Official Implementation of our Style-based Age Manipulation (SAM) paper for both training and evaluation. SAM 
allows modeling fine-grained age transformation using a single input facial image

<p align="center">
<img src="docs/2195.jpg" width="800px"/>
<img src="docs/1936.jpg" width="800px"/>
</p>



## Repository structure
| Path | Description <img width=200>
| :--- | :---
| SAM | Repository root folder
| &boxvr;&nbsp; configs | Folder containing configs defining model/data paths and data transforms
| &boxvr;&nbsp; criteria | Folder containing various loss criterias for training
| &boxvr;&nbsp; datasets | Folder with various dataset objects and augmentations
| &boxvr;&nbsp; docs | Folder containing images displayed in the README
| &boxvr;&nbsp; environment | Folder containing Anaconda environment used in our experiments
| &boxvr; models | Folder containing all the models and training objects
| &boxv;&nbsp; &boxvr;&nbsp; encoders | Folder containing various architecture implementations
| &boxv;&nbsp; &boxvr;&nbsp; stylegan2 | StyleGAN2 model from [rosinality](https://github.com/rosinality/stylegan2-pytorch)
| &boxv;&nbsp; &boxvr;&nbsp; psp.py | Implementation of pSp encoder
| &boxv;&nbsp; &boxur;&nbsp; dex_vgg.py | Implementation of DEX VGG classifier used in computation of aging loss
| &boxvr;&nbsp; notebook | Folder with jupyter notebook containing SAM inference playground
| &boxvr;&nbsp; options | Folder with training and test command-line options
| &boxvr;&nbsp; scripts | Folder with running scripts for training and inference
| &boxvr;&nbsp; training | Folder with main training logic and Ranger implementation from [lessw2020](https://github.com/lessw2020/Ranger-Deep-Learning-Optimizer)
| &boxvr;&nbsp; utils | Folder with various utility functions
| <img width=300> | <img>



