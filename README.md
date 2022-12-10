# Melanoma Identification with CNNs
** visual about skin cancers ** in folder

### Business Understanding

Skin cancer is the most common form of cancer in the United States. There are an estimated 9,500+ new diagnoses per day in the United States with an optimistic 99% cure rate. There are three types of skin cancer, Basal Cell Carcinomas (BCCs), Squamous Cell Carcinomas (SCCs) and Melanomas. Although all 3 must be surgically removed, BCCs and SCCs have slim to no chance of being fatal. Melanoma is the only form that has the capability to metastasize throughout the body and has a high probability of being lethal if not discovered early enough. 

*abcdes* in folder

While there are the basic ABCDE rules for identifying Melanoma, they do not encompass their complexity and diversity in presentation, and can even appear similar to a regullar mole. Dermatologists use Dermatoscopes for better clinical evaluation and advise patients with increased risk of Melanomas to go to MoleSafe, where a full-body 3D scan evaluates all lesions on your body and can be used as a clinical aide. MoleSafe has been an incredible advancement in the treatment of skin cancer as doctors do not have to solely rely on their own eyes to properly diagnose. Although, giving a Dermatologist similar capabilities in the exam room would only lead to improved patient outcomes.

Although MoleSafe has plenty of benefits, it is time-consuming and expensive (~$500) for a personal scan as insurance does not cover it. I set out to create a neural network that could do the same evaluation as MoleSafe, but to be used inside a Dermatoscope while the doctor is in the room with the patient. The doctor would then have a live version of MoleSafe to be used as a clinical aide in their diagnosis.

*dermatoscope* *molesafe* in folder

### Dataset

I used the ISIC 2019 Dataset from Kaggle which has 25,331 images of 8 different skin lesion types viewed through a dermatoscope. 
*all 8 lesions* in photos

I ultimately decided to narrow my image classification down to differentiating between Melanomas (4,577)  and benign moles (9,755). 
* 3 of mels and benign nevi * in photos

### Modeling

The images were scaled and reshaped and then split into a train (9,550, 66.7%), validation (1,382, 9.6%) and test (3,385, 23.6%) sets and classified via a Convolutional Neural Network.

Throughout the modeling process I was concerned with both accuracy and recall, with a priority on recall. Obviously we want to get the correct diagnoses from the image, but I also wanted to focus on minimizing missing any possible melanoma diagnoses.

A one layer CNN was used as a baseline for the model. From there, dropouts, regularizers, optimizers, different augmentations and overall architecture of the network were manipulated to improve results.

### Evaluation

The final model's results are displayed below.

  > Recall: 86.8%

  > Accuracy: 78.1%

* display model architecture, graphs of recall and accuracy * in folder

### Conclusion


### Next Steps

  - Be able to compound image evaluation with important factors like age, sex, body location and past skin cancer history

  - Only a subset of diagnoses analysed

  - Can only handle simple photos with one lesion in the area

* male female photo * in folder

