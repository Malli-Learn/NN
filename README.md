# NN
# Project Name
Lending Loan Case Study Assignment 

### Problem Statement
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

#### Data Set Details
    The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:
- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion
## Solution : 
Images size is at  
    img_height = 180
    img_width = 180
   
   <b>standardize</b>
    RGB is a not a not ideal for a neural network.it is good to standardize values to be in the [0, 1]
    layers.experimental.preprocessing.Rescaling to normalize pixel values between (0,1).   

### Model 1 - With initail Data
  - Constructed using 8 layers
  - Total params: 1,172,265
  - Used loss funcation <b> SparseCategoricalCrossentropy </b> as it is Suitable for multi-class classification problems
  
 #### Finding
  - Model is OverFit, By seeing the graphs
  - where we can observe difference between Training and Validation loss is increasing
  - Training Accuracy went up to 80-90% but when it comes to validation it is around 45-50% only

  ### Model 2 With Agumented Data
  - Created with agumented data 
  - Same model is created for learning
  - Total params: 1,172,265
  - Used loss funcation <b> SparseCategoricalCrossentropy </b> as it is Suitable for multi-class classification problems
  
 #### Finding
  - where we can observe Over fitting was resolved, seems both Training and validation accurace and Losss at same level
  - But overall accuracy got dropped from 90% to 55%

 ### Model 3 With Augmentor - 500 Generated images
  - Created 500 additional images  using Augmentor with paratments flip_left_right, Rotate, Zoom and scale 
  - Same model is created for learning
  - Total params: 1,172,265
  - total images - 6739 
  - Used loss funcation <b> SparseCategoricalCrossentropy </b> as it is Suitable for multi-class classification problems
  
 #### Finding
  - With help of Augmentor generated data, Overall Accuracy increased very well
      * Training Acuracy - around 95%
      * Validation Accruracu - around 65%

  - Overall Loss
    * Training Loss - less than .25
    * Validation Loss - between 2.0 to 2.5

  Still Model is seems overfitting a bit, will can be fine tuned by modifying hyper parameters
  

## Technologies Used
- Python 3,o
- Pandas
- matplotlib
- Pathlib
- tensorflow.keras
- tensorflow.keras.models
- Agumentor 
  


## Contact
Created by @Malli-Learn - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
