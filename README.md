# Neural Network Charity Analysis
## Overview
### Purpose

The purpose of this Analysis is to determine which non profit foundations will be successful if given donations and if that money is used efficiently. The data will be preprocessed and then compiled trained and evaluated and then we run 3 test optimizations attempting to target higher accuracy. We thoroughly preprocess the data to make the models run smoothly before evaluation.


## Results
### Data Preprocessing

First part of preprocessing was to drop the EIN and NAME columns which were all just strings that would degrade the model
Second step was to find the columns with numerous unique valus the 2 biggest other then ask_amt which is neccesary for a solid accuracy were the Application_Type column which we binned and reduced the unique values.

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing1.png)
![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing2.png)

The Third step was to  bin the classifications column which was another heavy unique value column.

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing3.png)

Then we generate a categorical variable list so we can properly one hot encode the data.

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing4.png)

One Hot Encoder and merge the dataframes together.

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing5onehotencoder.png)

Split our Data ontp Features & Target.
Features are the X variable which is every column minus the is_successful column.
Target is the y variable which is the is_successful column.
The 2 columns that were neither features or targets were the EIN and NAME columns.
And scale the data after splitting the data into train and test variables

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing5featuretarget.png)

### Compiling, Training, and Evaluating the Model

Define the base model to be used and Compile the model to run.

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/compiled.png)

Trained & Evaluated Model

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/trained%26evaluated.png)

### Optimization Attempts

Attempt 1 Adding a third hidden layer

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/optimization1.png)

Attempt 2 adding 3rd hidden layer and 50 additional epochs

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/optimization2.png)

Attempt 3 adding additions epochs and using Selu instead of Relu

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/optimization3.png)

None of the optimization models met the 75% accuracy requirement, I also tried many other models that included 10x neurons changing and modifying more activation layers, deleting STATUS column and other columns from the data. none proved efficient enough to increase the accuracy of the model.

## Summary
### Overall Summary

This analysis was relatively thorough other then my lack of ability to acheive the 75% average accuracy of the model. I did however try many different variations of the model to attempt to acheive a higher accuracy %. However all of my efforts resulted in approximately 73% accuracy. 

### Recommendation

There really isnt much to recommend about this analysis as it did its job and the task was accomplished with showing there is approximately 73% success rate if the money is given to a random charity. However if I could make 1 recommendation it would be to provide a possibility where the charity would provide use receipts to show they are actually using the money effectively once granted a charitible donation. However the model and the analysis are performed properly.


    Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

