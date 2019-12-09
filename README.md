# DeepLearning: Understanding Clouds from Satellite Images By MaskRCNN and Unet
Authors: Jiaqi Tang, Jingjing Lin, Xinyi Ye, Yeqing Liu

## Objectives

Climate change has been a serious topic in recent years and even influenced political decision making.
A better physical understanding of clouds can help build better climate models as shallow clouds play a huge role in determining the Earth's climate. Although human eyes are pretty good at detecting features of different clouds, it is  challenging to build traditional rule-based algorithms to separate cloud features. Our work introduces a model for to classify cloud organization patterns from satellite images with MaskRCNN.


## Data

[Dataset click here](https://www.kaggle.com/c/understanding_cloud_organization/data)

The dataset includes 22184 satellite images of 1400 x 2100 px that contain certain cloud formations, with label names: Fish, Flower, Gravel, Sugar from NASA Worldview. Each image has at least one cloud formation, and can possibly contain up to all all four. The labels were created in a crowd-sourcing activity at the Max-Planck-Institite for Meteorology in Hamburg, Germany, and the Laboratoire de météorologie dynamique in Paris, France.

## Write-up

[documentName](document link)

## Method
Mask R-CNN models replace the RoI pooling layer with an RoI alignment layer. This allows the use of bilinear interpolation to retain spatial information on feature maps, making Mask R-CNN better suited for pixel-level predictions.
Mask R-CNN not only predicts the categories and bounding boxes of RoIs, but also allows us to use an additional fully convolutional network to predict the pixel-level positions of objects.

Unlike Mask RCNN,  UNet can produce only one mask. Unet contains two paths. First path is the contraction path (also called as the encoder) which is used to capture the context in the image. The encoder is stack of convolutional and max pooling layers. The second path is decoder)which is used to enable precise localization using transposed convolutions.


## Challenge and Solution
Challenge:
Our challenge in this project is to detect the where the cloud is, and then to classify the type of cloud.
Clouds are sparse and it is hard to determine the bound of clouds.

Solution:
Instant segmentation on COCO dataset (COCO is a large-scale object detection, segmentation, and captioning dataset.)


