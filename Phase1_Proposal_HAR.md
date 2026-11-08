# Phase 1 Project Proposal — Software-only Track

**Course:** ML 402331  
**Student:** Essam Taha  
**University ID:** 2410014  
**Official assignment idea:** #6 — Human Activity Recognition

## 1. Idea and problem statement
Wearable and smartphone motion sensors can recognize daily activities without manual user input. This software-only project will classify human activities using accelerometer and gyroscope measurements from a public dataset. A simulated sensor stream is planned for a later phase; no hardware is purchased or built.

## 2. Research question
How accurately can machine-learning models classify daily human activities from smartphone accelerometer and gyroscope features in a public sensor dataset?

## 3. Machine-learning task
**Task:** Multiclass classification.  
**Target:** Activity: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING.  
**Features:** 561 time- and frequency-domain features derived from tri-axial accelerometer and gyroscope signals, including body acceleration, gravity acceleration, angular velocity and summary statistics.

## 4. Dataset and data plan
**Dataset:** UCI Machine Learning Repository, [Human Activity Recognition Using Smartphones](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones).  
**Size:** 10,299 labeled observations: 7,352 train and 2,947 test; 561 numeric features and six activity classes. Data were collected from 30 volunteers using smartphone accelerometer and gyroscope sensors. The public dataset provides labels. It exceeds the 5,000-row software-only data requirement for the later phase. Simulated streaming is planned for a later phase, not completed in Phase 1.

## 5. Tools
Python 3, Google Colab/Jupyter, pandas, NumPy, scikit-learn, matplotlib and GitHub. A separate small public diabetes dataset is used for the **required Phase 1 linear-regression starter exercise**; the actual HAR task is classification.

## 6. Three related works
1. Anguita, D., Ghio, A., Oneto, L., Parra, X., & Reyes-Ortiz, J. L. (2013). A public domain dataset for human activity recognition using smartphones. *ESANN 2013*.
2. Lara, O. D., & Labrador, M. A. (2013). A survey on human activity recognition using wearable sensors. *IEEE Communications Surveys & Tutorials, 15*(3), 1192–1209.
3. Reyes-Ortiz, J. L., Oneto, L., Samà, A., Parra, X., & Anguita, D. (2016). Transition-aware human activity recognition using smartphones. *Neurocomputing, 171*, 754–767.

## 7. Phase 1 deliverables and scope
This proposal, the shared GitHub repository and a Google Colab notebook loading a public dataset and running first linear regression. The HAR model, simulated stream, comparisons and demonstration are later phases. Instructor approval for the software-only track is requested.