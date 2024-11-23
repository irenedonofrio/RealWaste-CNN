# RealWaste Image Multiclass Classification

## **Overview**
This project focuses on building a deep learning model for **multiclass image classification** of waste materials using the **RealWaste** dataset, which was sourced from waste received at the Whyte's Gully Waste and Resource Recovery facility in Wollongong, NSW, Australia.
The project explores both Deep CNNs and Transfer Learning techniques. Models are trained on the training dataset and evaluated on the validation set. The best-performing model, DenseNet121-FT, is further tested on the test set.
Transfer learning is implemented using two approaches: feature extraction and fine-tuning to optimize performance.

---

## **Dataset**

The dataset comprises 4,752 labeled images of waste, with each image sized at **524x524 pixels**. The dataset is publicly available from the **UC Irvine Machine Learning Repository**.
It is a comprehensive dataset that covers various classes of landfilled waste for sustainable waste management: 

| Label               | Image Count |
|---------------------|-------------|
| Cardboard           | 461         |
| Food Organics       | 411         |
| Glass               | 420         |
| Metal               | 790         |
| Miscellaneous Trash | 495         |
| Paper               | 500         |
| Plastic             | 921         |
| Textile Trash       | 318         |
| Vegetation          | 436         |

- **Publication Reference**:  
  Single, S.; Iranmanesh, S.; Raad, R. *RealWaste: A Novel Real-Life Data Set for Landfill Waste Classification Using Deep Learning.* Information 2023, 14, 633.  
  [DOI: 10.3390/info14120633](https://doi.org/10.3390/info14120633)

- **Dataset Source**:  
  [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/)

---

## **Project Highlights**

1. **Dataset Exploration - Tackling dataset imbalanceness**
   
  The RealWaste dataset is explored ,providing insights into the distribution and characteristics of the data. Given the **imbalanceness** of the dataset the ``class_weight`` is implemented to     force the model to pay more/less attention to the classes based on their frequency. 

2. **Data Augmentation**
   
  Data augmentation is a technique used to artificially increase the size of a training dataset by applying various transformations to the existing data. It usually adopted to ensure the           **robustness** and **generalization** of the model.

  In this specific case I will apply the following transformations: 
    * Horizontal flip 
    * Rotate 
    * Shear

2. **Different models tried**
   
   Different type of models are implemented, trained and evaluated.
     * **Convolutional Neural Networks**:
         * **Base-DeepCNN**: A simple architecture with three feature extraction blocks (convolution + pooling + batch normalization) followed by a classifier.
         * **Deep-CNN with Residual Connections and Depthwise Separable Convolutions**: Incorporates residual connections to mitigate vanishing gradient issues and depthwise separable                       convolutions for a smaller, faster-converging, and less overfitting-prone model.
    
    * **Transfer learning**:
      Transfer learning consists in reusing a model which has been already trained on a large dataset (and thus it is a generic model) for our purposes. I adopted the two pre-trained models that       performed the best in the original paper:
        * **InceptionV3**
        * **DenseNet121**
          
## **Project Highlights**
Packages and version are in ``conda.yaml``
---
