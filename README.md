# CASCRNet: An Atrous Spatial Pyramid Pooling and Shared Channel Residual based Network for Capsule Endoscopy

### Team Name: Code Cortex

### Team Members: M Manvith Prabhu, K V Srinanda, Dr.Shyam Lal

### This repository houses the code and resources associated with our work on on the Capsule Vision Challenge 2024 by MISAHUB.

## Introduction

As proposed by the authors of this challenge, the task in hand invites contestants to create a model capable of automatically classifying abnormalities captured in video capsule en-
doscopy (VCE) video frames. To address this multi-class disease classification task, which is challenging due to the complexity and imbalance in the Capsule Vision challenge dataset, we propose CASCRNet (Capsule endoscopy-Aspp-SCR-Network), a parameter-efficient and
novel model that uses Shared channel residual (SCR) blocks and Atrous Spatial Pyramid
Pooling (ASPP) blocks. Further, the performance of the proposed model is compared
with other well-known approaches. The experimental results yield that proposed model
provides better disease classification results. The proposed model was successful in classifying diseases with a F1 Score of 78.5% and a Mean AUC of 98.3% on the validation data, which is promising given its compact architecture.

## Technologies Used

![Tech Used](https://go-skill-icons.vercel.app/api/icons?i=python,tensorflow,scikitlearn,numpy,matplotlib)

## Dataset

The dataset contains 37607 training images and 16132 validation images belonging to 10 classes each viz. Angioectasia, Bleeding, Erosion, Erythema, Foreign Body, Lymphangiectasia, Normal, Polyp, Ulcer and Worms. The testing set consists of 4385 images. The training and validation sets are highly imbalanced with Normal class forming the large chunk of the data.

## Proposed Approach
The AI pipeline developed by our team for this challenge is depicted in Figure 1.

![AI pipeline](image.png)
<p align="center">Figure 1: AI Pipeline</p>

The proposed model, CASCRNet, leverages the shared channel residual block concept depicted in Figure 2. An Atrous Spatial Pyramid Pooling block was incorporated to further enhance the model's ability to understand images. The LeakyReLU activation function with an alpha value of 0.01 was utilized. In addition to this, the Adam optimizer was used, whose learning rate started with a value of 0.001 and was halved each time it reached a plateau. Dilated convolutions were applied within the residual blocks. Additionally, focal loss was implemented to improve performance. The architecture of CASCRNet is illustrated in Figure 3.

![SCR Block](image-1.png)
<p align="center">Figure 2: Shared Channel Residual Block</p>

![alt text](image-2.png)
<p align="center">Figure 3: Architecture of the proposed CASCRNet</p>


## Results and Discussions

A comparison of the performance metrics of the submitted models and baseline models on
the validation dataset is provided in Table 1. The proposed model CASCRNet clearly outperforms all other
models and baselines across every evaluation metric.

![Comparision Table](image-3.png)

Figure 4 shows the performance of CASCRNet on the validation data in the form of ROC Curve and normalized confusion matrix. Remarkably, CASCRNet achieves
these metrics while processing full-sized input images (224x224), even in the presence of a highly
imbalanced training dataset. Despite its good performance, it is essential to note that the
model is not intended as a replacement for a medical professional.

![Metrics](image-4.png)
<p align="center">Figure 4: Performance of CASCRNet on Validation Data</p>

## Conclusion and Future Scope

The proposed model, being both compact and parameter-efficient, is well-suited for deployment on edge devices and mobile platforms, making it an ideal tool to assist doctors and medical personnel. Moreover, the model can be extended for real-time monitoring in
video capsule endoscopy, offering valuable clinical support. While the CASCRNet outperformed others in the comparative study, there remains
room for improvement. Exploring architectures like Vision Transformers (ViTs) and Vision-Language Models (VLMs) may lead to better-balanced accuracy. VLMs, in
particular, could provide deeper insights and explain the rationale behind the model’s decisions, further enhancing its utility in medical applications.
