# Capsule-Vision-2024-Solution-Team_Layer_Players


**Capsule Vision Challenge 2024** is all about multi-class abnormality classification of video capsule endoscopy. The task is to classify video capsule endoscopy frames into the following 10 classes : **Angioectasia**, **Bleeding**, **Erosion**, **Erythema**, **Foreign Body**,
**Lymphangiectasia**, **Polyp**, **Ulcer**, **Worms**, and **Normal**.

## Overview
Video capsule endoscopy (VCE) has become a vital tool for non-invasive visualization of
the gastrointestinal (GI) tract. However, the sheer volume of video data generated re-
quires automated solutions for abnormality detection to support clinical decision-making.
The Capsule Vision Challenge 2024 provides an opportunity to evaluate AI models that
can classify various abnormalities from VCE frames across ten categories. The purpose
of this challenge is to foster the development of vendor-neutral, generalized models for
clinical deployment. 

## Our solution to the Challenge
We have used a modified ResNet101 architecture with Squeeze and Excitation (SE)
blocks. Our approach involved augmenting
and balancing the dataset to address class imbalance, followed by training and evaluating
the model. The model achieved a **mean AUC** of **0.984**, **mean specificity** of **0.990**, **mean
average precision** of **0.839**, **mean sensitivity** of **0.759**, and a **balanced accuracy** of **0.780**.
These results demonstrate the potential of SE-ResNet101 for VCE abnormality detection,
with opportunities for further improvement in sensitivity and overall accuracy.

## Developed Pipeline
- The dataset consists of **37607** training images and **16132** validation images.
-  We have preprocessed the data and balanced it using augmentation methods. 
- The augmentation methods involved **image rescaling**, **image rotation**, **width and height shift**, **image flip**, and so on. 
- Additonally, the we balanced the dataset by fixing the sample size of each class to **5000**. 
- After preprocessing the training data, we have trained the **ResNet101 model** by incorporating **Squeeze and Excitation Blocks**.
- After training the model, validation was performed on the validation dataset. 

## Achieved results

Below given are the results achieved on the validation dataset.

| Model | Avg AUC | Avg Specificity | Avg Sensitivity | Avg F1-Score |Avg Precision | Balanced Accuracy |
| :------------ | ------ | ------ | ------ | ------ | ------ | ------ |
| ReNet101 with Squeeze-Excitation | 0.9843 | 0.9896 | 0.7593 | 0.7578 | 0.8388 | 0.7796 | 

## Conclusion
We presented an SE-ResNet101-based approach for VCE abnormality classification,
achieving high specificity and mean AUC, with competitive sensitivity and F1 scores.
Our approach demonstrates that an augmented and balanced dataset combined with SE
blocks in a deep learning model can support effective classification of VCE frames into
clinically relevant classes. This work contributes to the field by highlighting the feasibility
of vendor-independent AI-based models for VCE interpretation and offers insights for
further improvements toward clinical deployment.

## Acknowledgements

We extend our gratitude to the organizers of the Capsule Vision Challenge and all contributors to the dataset. We are grateful to the organisers for giving us a chance of participating in this competition and building a solution for this problem.

## Citations

- Challenge ArXiv
@article{handa2024capsule, title={Capsule Vision 2024 Challenge: Multi-Class Abnormality Classification for Video Capsule Endoscopy}, author={Handa, Palak and Mahbod, Amirreza and Schwarzhans, Florian and Woitek, Ramona and Goel, Nidhi and Chhabra, Deepti and Jha, Shreshtha and Dhir, Manas and Gunjan, Deepak and Kakarla, Jagadeesh and others}, journal={arXiv preprint arXiv:2408.04940}, year={2024}}

- Training and Validation Datasets
@article{Handa2024, author = "Palak Handa and Amirreza Mahbod and Florian Schwarzhans and Ramona Woitek and Nidhi Goel and Deepti Chhabra and Shreshtha Jha and Manas Dhir and Deepak Gunjan and Jagadeesh Kakarla and Balasubramanian Raman", title = "{Training and Validation Dataset of Capsule Vision 2024 Challenge}", year = "2024", month = "7", url = "https://figshare.com/articles/dataset/Training_and_Validation_Dataset_of_Capsule_Vision_2024_Challenge/26403469", doi = "10.6084/m9.figshare.26403469.v1", journal={Fishare}}

- Testing Datasets
@article{Handa2024, author = "Palak Handa and Amirreza Mahbod and Florian Schwarzhans and Ramona Woitek and Nidhi Goel and Deepti Chhabra and Shreshtha Jha and Manas Dhir and Pallavi Sharma and Dr. Deepak Gunjan and Jagadeesh Kakarla and Balasubramanian Ramanathan", title = "{Testing Dataset of Capsule Vision 2024 Challenge}", year = "2024", month = "10", url = "https://figshare.com/articles/dataset/Testing_Dataset_of_Capsule_Vision_2024_Challenge/27200664", doi = "10.6084/m9.figshare.27200664.v1" }
