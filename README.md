# Computer Vision and Machine learning Internship Assignment 
I was assigned a task to train the DINO object detection model on a pedestrian dataset consisting of 200 images collected within the IIT Delhi campus. 
Dataset Link -> [Click Here](https://drive.google.com/drive/folders/1DCpmo919b7OrAng9clEbiMHjO3D0hyoa?usp=sharin)

## Data Visualization :
![Visualization](https://github.com/vinodpatil2002/CV-Intern-Assignment/blob/56ff3302b6f48b06ada53f86a781d7100098d377/visualisation.png)

## Task Instructions:
 - Dataset Preparation (done ✅)
 - Repository Setup : [Link](https://github.com/IDEA-Research/DINO) (done ✅)
 - GPU Access : This whole assignment was performed using Google Colab [link](https://github.com/vinodpatil2002/CV-Intern-Assignment/blob/56ff3302b6f48b06ada53f86a781d7100098d377/cv_intern_assignment.ipynb)
 - Download the pretrained model: [Link](https://drive.google.com/drive/folders/1qD5m1NmK0kjE5hh-G17XUX751WsEG-h_)
 - Validation : Run the pretrained model on the current dataset (done ✅) code provided in the notebook
 - Report and Visualtion : 
   
| Metric                                       | Value       |
|----------------------------------------------|-------------|
| Average Precision (AP) @ IoU=0.50:0.95       | 0.546       |
| Average Precision (AP) @ IoU=0.50            | 0.887       |
| Average Precision (AP) @ IoU=0.75            | 0.640       |
| Average Precision (AP) @ IoU=0.50:0.95 (small) | 0.457     |
| Average Precision (AP) @ IoU=0.50:0.95 (medium) | 0.628    |
| Average Precision (AP) @ IoU=0.50:0.95 (large)  | 0.602    |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=1) | 0.115 |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=10) | 0.585 |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=100) | 0.647 |
| Average Recall (AR) @ IoU=0.50:0.95 (small)  | 0.590       |
| Average Recall (AR) @ IoU=0.50:0.95 (medium) | 0.707       |
| Average Recall (AR) @ IoU=0.50:0.95 (large)  | 0.643       |


![Without Finetuning](https://github.com/vinodpatil2002/CV-Intern-Assignment/blob/36d632b52f688b1134d9d1a2a0fb9e4a7d0989b6/without_finetuning.png)


 - Finetuning : The model was finetuned by reducing the `num_classes` from 91 to 2 and `dn_labebook_size` also to 2 as mentioned in the official repo that `dn_labebook_size >= num_classes + 1`
 - Report and visualation :

| Metric                                       | Value       |
|----------------------------------------------|-------------|
| Average Precision (AP) @ IoU=0.50:0.95       | 0.583       |
| Average Precision (AP) @ IoU=0.50            | 0.882       |
| Average Precision (AP) @ IoU=0.75            | 0.665       |
| Average Precision (AP) @ IoU=0.50:0.95 (small) | 0.464     |
| Average Precision (AP) @ IoU=0.50:0.95 (medium) | 0.688    |
| Average Precision (AP) @ IoU=0.50:0.95 (large)  | 0.621    |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=1) | 0.123 |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=10) | 0.609 |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=100) | 0.717 |
| Average Recall (AR) @ IoU=0.50:0.95 (small)  | 0.648       |
| Average Recall (AR) @ IoU=0.50:0.95 (medium) | 0.793       |
| Average Recall (AR) @ IoU=0.50:0.95 (large)  | 0.657       |

![With Finetuning](https://github.com/vinodpatil2002/CV-Intern-Assignment/blob/425be2ff12918b3d991417fb9ea40490d0f8dfae/with_finetuning.png)

- Comparision:
   
| Metric                                       | With Fine-Tuning | Without Fine-Tuning |
|----------------------------------------------|------------------|---------------------|
| Average Precision (AP) @ IoU=0.50:0.95       | 0.583            | 0.546               |
| Average Precision (AP) @ IoU=0.50            | 0.882            | 0.887               |
| Average Precision (AP) @ IoU=0.75            | 0.665            | 0.640               |
| Average Precision (AP) @ IoU=0.50:0.95 (small) | 0.464          | 0.457               |
| Average Precision (AP) @ IoU=0.50:0.95 (medium) | 0.688         | 0.628               |
| Average Precision (AP) @ IoU=0.50:0.95 (large)  | 0.621         | 0.602               |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=1) | 0.123   | 0.115               |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=10) | 0.609  | 0.585               |
| Average Recall (AR) @ IoU=0.50:0.95 (all, maxDets=100) | 0.717  | 0.647               |
| Average Recall (AR) @ IoU=0.50:0.95 (small)  | 0.648            | 0.590               |
| Average Recall (AR) @ IoU=0.50:0.95 (medium) | 0.793            | 0.707               |
| Average Recall (AR) @ IoU=0.50:0.95 (large)  | 0.657            | 0.643               |

- Conclusion : The fine-tuned model outperforms the model without fine-tuning, showing higher precision and recall across most metrics, particularly for medium and large object sizes. Fine-tuning is generally beneficial for improved model performance.


The whole code base with all the modified changes can be viewed [here](https://drive.google.com/drive/folders/11C17qVnuSsADBc-aDXzxwYEXZEyqPtHF?usp=sharing) 

