# Steel Plates fault diagnosis using Classification Models

## Objective:

   The objective of the project is to classify steel plates fault into 7 different types. The end goal is to train several machine Learning Algorithms for automatic pattern recognition. In doing so, I have employed **Logistic Regression**, **KNN**, **Naïve Bayes**, **Decision Trees** and **Random Forest**. Also, I have used **_Cross-validation_** to find the most optimum hyper-parameters. Finally, I compare the models and see  how well each model perform using Classification metrics: Confusion Matrix, Precision, Recall and F-1 Score.

## Motivation:


A fault may be defined as an unacceptable difference of at least one characteristic property or attribute of a system from acceptable usual typical performance. The main purpose of any fault diagnosis system is to determine the location and occurrence time of possible faults on the basis of accessible data and knowledge about the performance of diagnosed processes. Manual fault diagnosis system is the traditional way where an expert with electronic meter tries to obtain some information about relevant operational equipment, check the maintenance manual and then diagnose the probable causes of a particular fault.  However, intelligent fault diagnosis techniques can provide quick and correct systems that help to keep product quality problems at bay and facilitates precautionary maintenance.    
        
This project evaluates the performances of several popular and effective data mining models to diagnose seven commonly occurring faults of the steel plate namely; Pastry, Z_Scratch, K_Scatch, Stains, Dirtiness, Bumps and Other_Faults.
 

## Data Collection:

URL : [http://archive.ics.uci.edu/ml/datasets/steel%2Bplates%2Bfaults]

### Source:

> Semeion, Research Center of Sciences of Communication, Via Sersale 117, 00128, Rome, Italy. 
www.semeion.it

### References:

>> M Buscema, S Terzi, W Tastle, A New Meta-Classifier,in NAFIPS 2010, Toronto (CANADA),26-28 July 2010, 978-1-4244-7858-6/10 Â©2010 IEEE

>> M Buscema, MetaNet: The Theory of Independent Judges, in Substance Use & Misuse, 33(2), 439-461,1998

## Workflow :

   1. **Exploratory Data Analysis**
       - 1.1 Count Plot to show the number of defects belonging to each defect type.
       - 1.2 Visual analysis of the correlation between the factors.
       - 1.3 Correlation Matrix    
       
   2. **Model Development and Classification**
        - 2.1 Data Preparation
        - 2.2 Model Development
            - 2.2.1 Logistic Regression
            - 2.2.2 KNN
            - 2.2.3 Naïve Bayes
            - 2.2.4 Decision Trees
            - 2.2.5 Random Forest
   3. **Principal Component Analysis**
        - 3.1 PCA Transformation
            - 3.1.1 Obtain CoVariance Matrix
            - 3.1.2 Obtain EigenVectors and EigenValues
            - 3.1.3 Plot EigenValues
        - 3.2 Dimension Reduction to Principal Components
            - 3.2.1 Reduction of Dimension
        - 3.3 Modelling and Classification
            - 3.3.1 Logistic Regression
            - 3.3.2 K Nearest Neighbor
            - Naïve Bayes
            - Decision Trees
            - Random Forest
   
## Results:

   1. EDA helps in giving a preliminary glimpse on how various factors are affecting the development of Defects.
       - We notice that 'other defects', 'bumps' and 'K_Scratch' are major defects.
   2. Cross-Validation is an effective way to find the best Hyper-parameters.
   3. Decision Tree outperforms other Non-Ensamble models.
   4. Naïve Bayes performs better on a PCA model i.e., when the dimensions are reduced.
   5. Random Forests can substantially increase the efficiency but are computationally expansive when dealing with a large dataset as in this case.

   
   

|    **Model**     |    **Classification Accuracy**    | **Classification Error**   |
 |:------------:|:-----------------------------:|:----------------------:|
 | `Logistic Regression`| 67.61 |32.39|
 | `KNN` | 71.46 |28.54|
 | `Naïve Bayes `| 34.71 |**65.29**|
 | `Decision Trees` | 72.04|27.96|
 | `Random Forest` | **79.43** |20.57|
 
 
 | **PCA Model**| **PCA Classification Accuracy** | **PCA Classification Error**|
 |:-----:| :-----------------------------: | :-------------:|
 | `Logistic Regression`|37.56 |62.44|
 | `KNN` | **45.79** |54.21|
 | `Naïve Bayes` | 43.4 |56.6|
 | `Decision Trees` | 35.85 |**64.15**|
 | `Random Forest` | 44.94 |55.06|

## Conclusion:

Several Classification techniques fair pretty well in predicting the defect-type.  Although data mining techniques are capable of extracting patterns and relationships hidden deep into large datasets, without the cooperation and feedback from the experts and professional, their results are useless. The patterns found via data mining techniques should be evaluated by professionals who have years of experience in Predicting steel plates faults. 
    
