# Bone-Fracture-Detection
MI - CS302 - Project   

Dataset -   
  https://www.kaggle.com/datasets/andradaolteanu/rsna-fracture-detection  
  https://www.kaggle.com/competitions/rsna-2022-cervical-spine-fracture-detection/

## Abstract and Scope
The skeletal system of the human body comprising of over 200 bones is a very essential component. Bones allow for movement, provide protection and structure to the human body. Bone fractures occur due to trauma, overuse or other diseases. Bone fractures are painful to endure and patients suffering from such a condition benefit from quick and accurate diagnosis which will enable them to access the right treatment. Doctors use X-Ray images to identify the fractured bone. The manual detection is often time-consuming and there is also a high chance of error. Hence, this project aims to automate the process and help doctors identify fractures quicker which will enable patients to get the right treatment faster.

## Feasibility Study
Doctors rely on X-ray images to identify fractures. Manual inspection of multiple X-rays can be time-consuming and often a tedious process. Radiologists may sometimes overlook or fail to notice certain details due to high pressure and workloads. This project aims to assist doctors and radiologists, to prevent this from happening and provide the right diagnosis as soon as possible. 
  
  
## Dataset Description  
The dataset is split into multiple folders with different data. The first folder - zip_png_images contains different folders, each containing the CT scan images of a unique study instance pertaining to a particular patient scan. The images are in png format.  
Train.csv contains informatation on each study instance. It consists of multiple rows including study instance id, patient overall, total fractures and c1 through c7.  
    - Patient overall indicates if there is a broken bone or not.  1 for fracture and 0 for no fracture  
    - Total fractures indicates number of broken vertebrae  
    - c[1-7] tells if a given vertebrae for given study instance id is fractured or not  
    
    
## Model  
## Accuracy and Loss Metrics  
