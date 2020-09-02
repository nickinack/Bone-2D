# Bone-Extraction-UNet
Implementation of the paper , <a href="https://arxiv.org/pdf/2003.10839.pdf">Bone Structures Extraction and Enhancement in Chest Radiographs via CNN Trained on Synthetic Data</a> published on March 2020 by Ophir Gozes and Hayit Greenspan. The process involves converting a 3-D X-Ray (CXR) into  Digitally Reconstructed Radiographs (DRR) using Computer Vision. Previous works on this domain used FCNNs and L1 Loss for calculating the predicted DRR. This method proposes a new model: a trainable UNET and a non-trainable VGG19 network (in order to calculate perpetual loss using the conv3d outputs).

## Layout

The layout of the model is as follows:

- ### Model

<img src="https://github.com/nickinack/Bone-Extraction-U-Net/blob/master/train_process.png">

- ### UNet

<img src="https://github.com/nickinack/Bone-Extraction-U-Net/blob/master/unet.png">

- ### VGG19

<img src="https://github.com/nickinack/Bone-Extraction-U-Net/blob/master/vgg19.png">

## Loss

The loss function is given by the L1 Distance output of the convolutional block <i>block3.cov3d</i> layer.

## Contributors

- <a href="https://github.com/nickinack">Karthik Viswanathan</a>
