# Detect COVID-19 from chest x-rays
# Introduction
This notebook is part of a coding bootcamp project called "chestX" hosted by TechLabs Berlin. ChestX is a webapp that detect COVID-19 from chest x-ray images (CXR) with the help of a computer vision model. For more information please refer to our GitHub: https://github.com/TechLabs-Berlin/st21-chestX

### Interpreting CXRs
- X-ray images are grayscale with values ranging from 0 (black) to 255 (white) 
- The values correlate to the density of the body's area:
    - black: air 
    - dark grey: subcutaneous tissues or fat
    - light grey: soft tissues like the heart and blood vessels 
    - off white: bones such as the ribs
    - bright white: metallic objects such as pacemakers or necklace 
- If something happens in the lungs, such as pneumonia, the air-dense lungs change into water-dense lungs. This causes the demarcation lines to fade since the pixel densities start closing in on the grayscale bar.
- About 20% of patients infected with COVID-19 develop pulmonary infiltrates and some develop very serious abnormalities. 

### Why CXRs?
- Portable chest X-rays are likely to be one of the most common modalities for the identification and follow-up of COVID-19 lung abnormalities.
- CT rooms are more difficult to decontaminate and they are not as available in different parts of the world as x-ray machines
- Deep Learning techniques have proven to be beneficial in both classifying abnormalities from lung x-ray images and aiding the radiologists to accurately predict COVID-19 cases in a reduced time frame.

Source: https://link.springer.com/article/10.1007/s42979-021-00496-w

### The dataset
The dataset used: https://www.kaggle.com/tawsifurrahman/covid19-radiography-database 

Which is a collection from the following resources:
- [1]https://bimcv.cipf.es/bimcv-projects/bimcv-covid19/#1590858128006-9e640421-6711
- [2]https://github.com/ml-workgroup/covid-19-image-repository/tree/master/png
- [3]https://sirm.org/category/senza-categoria/covid-19/
- [4]https://eurorad.org
- [5]https://github.com/ieee8023/covid-chestxray-dataset
- [6]https://figshare.com/articles/COVID-19_Chest_X-Ray_Image_Repository/12580328
- [7]https://github.com/armiro/COVID-CXNet
- [8]https://www.kaggle.com/c/rsna-pneumonia-detection-challenge/data
- [9] https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

### Data composition
The dataset contains 3616 COVID-19 positive cases, 10192 Normal, 6012 Lung Opacity (Non-COVID lung infection), and 1345 Viral Pneumonia images. In total, that makes 17549 COVID-19 negative and 3616 positive images and therefore a quite biased dataset (A positive to negative ratio of 20.61%.).
