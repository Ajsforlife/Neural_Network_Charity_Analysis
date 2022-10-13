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

One Hot Encoder

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing5onehotencoder.png)

Features & Target

Features are the X variable which is every column minus the is_successful column.
Target is the y variable which is the is_successful column.
And scale the data after splitting the data into train and test variables

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/preprocessing5featuretarget.png)

### Compiling, Training, and Evaluating the Model

Compiled

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/compiled.png)

Trained & Evaluated

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/trained%26evaluated.png)

### Optimization Attempts

Attempt 1 Adding a third hidden layer

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/optimization1.png)

Attempt 2 adding 3rd hidden layer and 50 additional epochs

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/optimization2.png)

Attempt 3 adding additions epochs and using Selu instead of Relu

![](https://github.com/Ajsforlife/Neural_Network_Charity_Analysis/blob/main/Pictures/optimization3.png)

## Summary
### Overall Summary

### Recommendation

    Results: Using bulleted lists and images to support your answers, address the following questions.
        Data Preprocessing
            What variable(s) are considered the target(s) for your model?
            What variable(s) are considered to be the features for your model?
            What variable(s) are neither targets nor features, and should be removed from the input data?
        Compiling, Training, and Evaluating the Model
            How many neurons, layers, and activation functions did you select for your neural network model, and why?
            Were you able to achieve the target model performance?
            What steps did you take to try and increase model performance?

    Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

