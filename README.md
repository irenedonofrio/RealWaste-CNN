# RealWaste Image Multiclass Classification

## **Overview**
This project focuses on building a deep learning model for **multiclass image classification** of waste materials using the **RealWaste** dataset, which was sourced from waste received at the Whyte's Gully Waste and Resource Recovery facility in Wollongong, NSW, Australia.
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

---

## **Dataset**

The dataset comprises 4,752 labeled images of waste, with each image sized at **524x524 pixels**. The dataset is publicly available from the **UC Irvine Machine Learning Repository**.

- **Publication Reference**:  
  Single, S.; Iranmanesh, S.; Raad, R. *RealWaste: A Novel Real-Life Data Set for Landfill Waste Classification Using Deep Learning.* Information 2023, 14, 633.  
  [DOI: 10.3390/info14120633](https://doi.org/10.3390/info14120633)

- **Dataset Source**:  
  [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/)

---

## **Project Highlights**

1. **Dataset Exploration**
The RealWaste dataset is explored ,providing insights into the distribution and characteristics of the data. Given the **imbalanceness** of the dataset the ``class_weight`` is implemented to force the model to pay more/less attention to the classes based on their frequency. 

---
