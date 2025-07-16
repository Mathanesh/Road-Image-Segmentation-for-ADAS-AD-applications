# Road Image Segmentation for ADAS/AD applications
Accurate road segmentation is essential for autonomous driving and ADAS, enabling effective navigation in complex environments. This study examines how model architecture and dataset choice affect segmentation by training a modified VGG-16 on the Comma10k dataset and a modified U-Net on the KITTI Road dataset. Both models achieved high accuracy, with cross-dataset testing showing VGG-16 outperforming U-Net, despite U-Net being trained for more epochs. We analyze model performance using metrics such as F1-score, mIoU, and precision, discussing how architecture and dataset impact results.


## Introduction:
Road image segmentation plays a crucial role in applications such as autonomous driving (AD), advanced driver assistance systems (ADAS), traffic monitoring, and smart city development. It enables a deeper understanding of the driving environment, supporting safer and more efficient decision-making. This is particularly valuable for tasks like lane detection, obstacle avoidance, and path planning in self-driving vehicles. This report focuses on training two models on separate datasets, then performing cross-validation by evaluating one model with the other dataset it has not been trained on. For this, we trained a modified VGG-16 model with the Comma10k dataset and a modified U-Net model on the KITTI Road dataset. We will also investigate what went wrong with the under-performing model, and how to improve model training moving forward.

![seg_intro](https://github.com/user-attachments/assets/6f5407d8-052c-4777-a713-94533b6f19e0)

## Model Architecture:
### UNET
<img width="1555" height="1036" alt="unet_structure" src="https://github.com/user-attachments/assets/d093c7c9-93f1-4314-a4c3-151b94bedc26" />

### VGG16
<img width="601" height="611" alt="vgg_structure" src="https://github.com/user-attachments/assets/0ad50aa2-02ed-4c23-bd53-c9a9dc8a299f" />

## Dataset Information:
<img width="2171" height="529" alt="dataset" src="https://github.com/user-attachments/assets/e64fe6eb-2a31-485f-9263-a9b478fd75b7" />

### Training on KITTI Dataset
<img width="1823" height="1215" alt="kitti_training" src="https://github.com/user-attachments/assets/a02472cd-1254-457c-9476-4bc2b7af4666" />

### Training on comma10k Dataset
<img width="1489" height="990" alt="comma_training" src="https://github.com/user-attachments/assets/73bb563c-d2b1-46ed-9a1b-305a1e21d756" />

### Data Augmentation
<img width="1368" height="901" alt="data_aug" src="https://github.com/user-attachments/assets/b7b9d831-b21d-43cb-98ab-25af8a4744b2" />

## Results:
### Evaluation
<img width="2409" height="424" alt="eval" src="https://github.com/user-attachments/assets/9be04868-d1de-476a-88a6-f763bb287138" />

### Cross-validation
<img width="2409" height="345" alt="cross_val" src="https://github.com/user-attachments/assets/c4aa20d5-19b7-400d-8620-89e1249b2cb8" />


## Conclusion:
This project demonstrates that the choice of dataset and model characteristics greatly affect the ability of a model to classify unseen data, as the datasets used for testing may have discrepancies that other datasets may not have, such as the presence of very dark tree shadows in the case of the KITTI dataset. Data augmentation techniques and transfer learning can be implemented to overcome the effects of said discrepancies. All in all, one should always explore and utilize different datasets to seek what is best for the project at hand, and seek datasets with a wide variation of data to reduce overfitting and improve generalization performance.

<img width="1451" height="941" alt="conclusion" src="https://github.com/user-attachments/assets/120dcc48-01b7-4d2b-9407-80d45daf04da" />
