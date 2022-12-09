# Melanoma Identification with CNNs

### Business Understanding
Skin cancer is the most common form of cancer in the United States. There are an estimated 9,500+ new diagnoses per day in the United States with an optimistic 99% cure rate. There are three types of skin cancer, Basal Cell Carcinomas (BCCs), Squamous Cell Carcinomas (SCCs) and Melanomas. Although all 3 must be surgically removed, BCCs and SCCs have slim to no chance of being fatal. Melanoma is the only form that has the capability to metastasize throughout the body and has a high probability of being lethal if not discovered early enough. 

While there are the basic ABCDE rules for identifying Melanoma, they do not encompass their complexity and diversity in presentation. Dermatologists use Dermatoscopes for better clinical evaluation and advise patients with increased risk of Melanomas to go to MoleSafe, where a full-body 3D scan evaluates all lesions on your body and can be used as a clinical aide. MoleSafe has been an incredible advancement in the treatment of skin cancer as doctors do not have to solely rely on their own eyes to properly diagnose. Although, giving a Dermatologist similar capabilities in the exam room should only lead to improved patient outcomes.

Although MoleSafe has plenty of benefits, it is time-consuming and expensive (~$500) for a personal scan as insurance does not cover it. I set out to create a neural network that could do the same evaluation as MoleSafe, but to be used inside a Dermatoscope while the doctor is in the room with the patient. The doctor would then have a live version of MoleSafe to be used as an aide in their diagnosis.

### Dataset
I used the ISIC 2019 Dataset from Kaggle which has 25,331 images of 8 different skin lesion types viewed through a dermatoscope. 

Data Analysis


### Modeling

The images were scaled and reshaped and then split into a train (70%, 18,829 photos), validation (10%, 2,553) and test (20%, 5,106 photos) sets and classified via a Convolutional Neural Network.

Throughout the modeling process I was primarily concerned with both accuracy and recall, with a priority on recall. Obviously we want to get the correct diagnoses from the image, but I also wanted to focus on minimizing missing skin cancer diagnoses.

A one layer CNN was used as a baseline for the model. From there, dropouts, regularizers, optimizers, augmentations and overall architecture of the network were manipulated to improve results.

### Evaluation

Recall: 86.8%

Accuracy: 78.1%

### Next Steps

Be able to include important factors like age, body location and past skin cancer history

Only a subset of diagnoses analysed

