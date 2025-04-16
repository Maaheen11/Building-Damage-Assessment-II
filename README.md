# Building-Damage-Assessment-Using-Satellite-Imagery

This project enhances the DAHiTrA (Damage Assessment using Hi-Resolution imagery and Transformer Architectures) model to improve the separation of adjacent buildings in post-disaster satellite imagery. The primary goal is to increase the accuracy of damage assessment by preserving fine-grained building boundaries using Edge-Aware Loss and SAM2 (Segment Anything Model).

## Introduction
Existing models like DAHiTrA tend to merge closely located buildings in post-disaster imagery and often miss small structures entirely. This limits their usability in high-stakes, real-world disaster response scenarios. This project addresses these limitations by extending DAHiTrA with prompt-based segmentation and edge-sensitive loss functions.

## Features
1. Edge Aware Loss Integration: Achieves more precise building boundary segmentation.
2. SAM2-based Boundary Refinement: Improves building separation and overall segmentation accuracy.

## Installation  

To clone this repo: 

```
git clone https://github.com/Maaheen11/Building-Damage-Assessment-II.git
cd DamageAssessment
```

Training/Evaluating the DAHiTrA model: 

1. Copy the xBD and LEVIR-CD dataset in the following directories 
  xBD -> data/xbd/train 
  LEVIR-CD -> data/LEVIR-CD

2. Execute the run_cd.sh file to train the model

3. Execute the eval.sh file to evaluate the model


Executing the SAM2 pipeline for Image Segmentation:

SAM2 is initialized using the sam2.1_hiera_small.pt and sam2.1_hiera_small.yaml file located in the sam2/configs/sam2.1 directory. Make sure these files exists. 

Execute the Sam2_finetuning.ipynb file to perform the enhanced image segmentation of damaged buildings. 


## Acknowledgment 
We thank https://github.com/nka77/DAHiTra.git for providing the project publicly. Our improvements were build on this project. 
