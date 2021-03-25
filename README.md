# Metis-Project-Four

## Metastatic Tumor Detection
This project used data consisting of images that showed lymph node tissues under a microscope. They were labelled with tumor or no tumor tissue present in the image. Tumor detection in lymph nodes is espcially important when determining the extent of metastatsis in a person's cancer diagnosis. This categorization will shape the treament and recovery of the patient depending on the analysis from a lymph node. The project deployed two separate convolutional neural networks (CNN)s. One was build and then iterated through to the final version and then compared to the second that used transfered learning (ResNet50). Overall, the project sought to aid physicians when determining which lymph's to biopsy for further anaylsis and detect pixel sized tumor tissue present in otherwise healthy images. 

## Files

### - Database Build and Analysis : 
- The data consists of 220,000 microscopic slide images of lymphnode tissue from the Netherlands in 2016. The dataset was rebalanced from the original to exclude duplicates reducing the original 300,000+ down to the 220,000 used for this analysis made available on Kaggle. The data has an imbalance between Cancerous and Non-cancerous slides of roughly 46% to 54% respectively. The project employed undersampling of 89,000 for each category setting the remaining images for testing against the models training and validation datasets. 

#### - Baseline & Final Iteration Convolutional Neural Networks: 
- Baseline model deployed three layers of convolutional Neural Networks with a binary class mode. This yieled decent accuracy results for the training set, but failed to improve the validation accuracy beyond the 50 ~ 53% range. The model overfit the data and could not be deployable beyond this experienment.
- The Final Iteration closed the gap between the validation accuracy and the training accuracy, but a small gap persisted. This indicated that despite improving the validation accuracy from 50 to 84 that the training data still overfit the model slightly. However when compared to the transfer learning example we see the model outperformed the ResNet50 pre-trained model by roughly 10 points. 
- ResNet50 is a Residual Neural Network that is pretrained on data externally. It relies on those images to build the CNN, by detecting curves, lines, patterns to build shapes and then identify the 
    
#### Conclusions

- The comparison between the Transfer Learning ResNet50 CNN and the Final Iteration of our model revealed that our model had a higher accuracy in both 
