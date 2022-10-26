# Bone-Fracture-Detection
MI - CS302 - Project   

Dataset - https://www.kaggle.com/datasets/andradaolteanu/rsna-fracture-detection

Stuff to do:
- Split dataset into test and train data   
- Calculate accuracy and loss  
- Build better model after learning more about CNN layers    




- Bounding data csv from competition data for EDA and to show fractures?   
  
  
## Dataset Description  
The dataset is split into multiple folders with different data. The first folder - zip_png_images contains different folders, each containing the scan images of a unique study instance pertaining to a particular patient scan. The images are in png format.  
Train.csv contains informatation on each study instance. It consists of multiple rows including study instance id, patient overall, total fractures and c1 through c7.  
    - Patient overall indicates if there is a broken bone or not.  1 for fracture and 0 for no fracture  
    - Total fractures indicates number of broken vertebrae  
    - c[1-7] tells if a given vertebrae for given study instance id is fractured or not  
    
    
## Model  
## Accuracy and Loss Metrics  


  
    
      
        
          
            
            

https://www.kaggle.com/competitions/rsna-2022-cervical-spine-fracture-detection/
