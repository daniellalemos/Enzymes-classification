<img src='images/logo.png' width='150'>


# Enzymes classification

This repository was created as part of the Intelligent systems for bioinformatics project to support its development. The objective was to predict the subclasses for Transferases using machine and deep learning approaches.


## Context 

Enzymes are proteins that act as biological catalysts by accelerating chemical reactions. An enzyme is therefore a molecule that increases the speed of biochemical reaction in an organism. 

Enzymes are classified by the Nomenclature Committee of the International Union of Biochemistry into Enzyme Comission (EC) numbers, a four digit numerical representation separated by periods (e.g. 2.6.1.9). 

The four levels of EC numbers are related to each other in a functional hierarchy. The first number describes one of the 7 main enzymatic classes, the second describes the subclass, the third represents the sub-subclass and the fourth refers to the substrate of the enzyme.

Here, we will predict the subclass for the class 2 (transferases).


### Dataset

We will use the ECPred dataset (Sequeira et al., 2021, ECPred: a tool for the prediction of the enzymatic functions of protein sequences based on the EC nomenclature.)
This dataset contain many enzymatics classes (1-7), the class 0 is not enzymatic. We only will work with the class 2. 


### Transferases

Transferases are enzymes that catalyse the transfer of a functional group from a donor molecule, often a coenzyme, to an acceptor molecule.
The different subclasses of this enzymes are presented in the table below.

<p align="center" width="100%">
    <img width="80%" src="https://github.com/daniellalemos/Enzymes-classification/blob/main/images/transferases_subclasses.png">
</p>


## Files information

- Preprocessing and unsupervised analysis:
    - Jupyter Notebook with Python scripts using io, numpy, pandas, matplotlib and random packages. 
    - These are utilized to extract the ec levels (class and subclass) to select a class with balanced data. 
    - During this step, we needed to encode the aminoacids to numeric numbers for machine learning and deep learning.
    - With this we made a selection of the best features and proceeded to make an unsupervised exploration of the dataset using two methods: PCA and t-SNE.


- Machine learning:
  - In this notebook is developed multiple machine learning models that can predict the subclasses of transferases. 
    - The models used were: LogisticRegression, Random Forest, SVM and KNN.
  - It was created a function (score_test_set) with many metrics for evaluating the models, comparing the predicted values with the real values.
    - The metrics used were: Accuracy, MCC, f1 score, confusion matrix, false discovery rate, sensitive; hit rate; recall or true positive rate, specificity or true negative rate and classification report. 
  - It was also used a ROC curve that allows visualizing the tradeoff between the classifier’s sensitivity and specificity. 



 
## Authors: 

- Alexandra Coelho (PG45458)
- Andreia Gomes (PG45463)
- Catarina Ferreira (PG45467)
- Daniela Lemos (PG45469)
