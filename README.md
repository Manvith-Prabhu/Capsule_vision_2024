# CASCRNet: An Atrous Spatial Pyramid Pooling and Shared Channel Residual based Network for Capsule Endoscopy

### Team Name: Code Cortex

### Team Members: M Manvith Prabhu, K V Srinanda, Dr. Shyam Lal

### This repository houses the code and resources associated with our work on on the Capsule Vision Challenge 2024 by MISAHUB.

## Introduction

As proposed by the authors of this challenge, the task in hand invites contestants to create a model capable of automatically classifying abnormalities captured in video capsule en-
doscopy (VCE) video frames. To address this multi-class disease classification task, which is challenging due to the complexity and imbalance in the Capsule Vision challenge dataset, we propose CASCRNet (Capsule endoscopy-Aspp-SCR-Network), a parameter-efficient and
novel model that uses Shared channel residual (SCR) blocks and Atrous Spatial Pyramid
Pooling (ASPP) blocks. Further, the performance of the proposed model is compared
with other well-known approaches. The experimental results yield that proposed model
provides better disease classification results. The proposed model was successful in classifying diseases with a F1 Score of 78.5% and a Mean AUC of 98.3% on the validation data, which is promising given its compact architecture. This approach was ranked 15 in the competition

## Technologies Used

![Tech Used](https://go-skill-icons.vercel.app/api/icons?i=python,tensorflow,scikitlearn,numpy,matplotlib)

## Dataset

The dataset contains 37607 training images and 16132 validation images belonging to 10 classes each viz. Angioectasia, Bleeding, Erosion, Erythema, Foreign Body, Lymphangiectasia, Normal, Polyp, Ulcer and Worms. The testing set consists of 4385 images. The training and validation sets are highly imbalanced with Normal class forming the large chunk of the data.

The training and validation datasets can be found [here](https://figshare.com/articles/dataset/Training_and_Validation_Dataset_of_Capsule_Vision_2024_Challenge/26403469?file=48018562).\
The testing dataset can be found [here](https://figshare.com/articles/dataset/Testing_Dataset_of_Capsule_Vision_2024_Challenge/27200664?file=49717386).

## Models used
1) [ResNet50](https://keras.io/2.16/api/applications/resnet/)
2) [DenseNet121](https://keras.io/2.16/api/applications/densenet/)
3) [RCCGNet](https://github.com/shyamfec/RCCGNet)
4) Proposed CASCRNet (this repository)

## Getting Started

### Prerequisites
Before starting, ensure you have:
- Downloaded the datasets from the above links
- A Kaggle account to run the notebooks OR
- Google Colab to run the notebooks

### Installation and Setup
1. **Clone the repository:**
```bash
git clone https://github.com/Manvith-Prabhu/CASCRNet.git
```
2. **Access the Capsule Vision 2024 dataset:** Upload the downloaded dataset to Kaggle or Colab

### Running the Models: 
1. **Open the notebooks on Kaggle or Google Colab:** Import the cloned notebooks into Kaggle or Google Colab to utilise their computational resources and pre-installed libraries.
2. **Run the notebooks:** Follow the step-by-step instructions within each notebook to train and evaluate the models. The notebooks are self-contained and include comments to guide you through the process.


## Proposed CASCRNet
 Figure 1 shows the architecture of Shared Channel Residual Block
<div align="center">
  <img src="https://github.com/user-attachments/assets/f72c36a4-5356-43c9-b497-20c34f483b4e" alt="Figure 2: Shared Channel Residual Block"/>
  <p><strong>Figure 1: Shared Channel Residual Block</strong></p>
</div>
 Figure 2 shows the model architecture of CASCRNet which uses SCR blocks followed by ASPP blocks.
<div align="center">
  <img src="https://github.com/user-attachments/assets/3ed5ee52-4759-424b-885b-0571479a6286" alt="Figure 3: Architecture of the proposed CASCRNet"/>
  <p><strong>Figure 2: Architecture of the proposed CASCRNet</strong></p>
</div>


## Results and Discussions

A comparison of the performance metrics of the submitted models and baseline models on
the validation dataset is provided in Table 1. The proposed model CASCRNet clearly outperforms all other
models and baselines across every evaluation metric.

<div align="center">
  <img src="https://github.com/user-attachments/assets/48c3a6a3-ab4e-4987-8764-71ebebcb25d6" alt="Figure 5: Your Caption Here"/>
</div>

We were ranked #2 on validation set and #15 on test set performance.


## Extra Files 
- **Metrics Report**: Each folder contatins a metric report Json file corresponding to predictions of the model on validation set
- **ROC Curve**: ROC curve for predictions of each model on validation set
- **Validation and Test predictions**: XLSX file of predictions of each model on validation and test set respectively (Test predictions is provided only for the proposed model)

## BibTex

```
@misc{srinanda2024cascrnetatrousspatialpyramid,
      title={CASCRNet: An Atrous Spatial Pyramid Pooling and Shared Channel Residual based Network for Capsule Endoscopy}, 
      author={K V Srinanda and M Manvith Prabhu and Shyam Lal},
      year={2024},
      eprint={2410.17863},
      archivePrefix={arXiv},
      primaryClass={eess.IV},
      url={https://arxiv.org/abs/2410.17863}, 
}
```
