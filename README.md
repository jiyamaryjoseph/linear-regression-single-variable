# linear-regression-single-variable (also using Libraries  of Pickle and joblib)
Here  I am using linear regression for single variable dataset.

## Pickle & sklearn Joblib 


                       Suppose you are working on a practice problem related to house rent given lots of data points and input features. It’s quite common to perform EDA, Preprocessing(may need to    create additional features), and feeding our data to our model. In this scenario even if we use the simplest Linear Regression Model (multiple variables) it may become huge in   size due to all the input_features and all the parameters which will be time-consuming to re-train again and again for use.


#### Method 1 – Pickle – 2 Steps
Many of you will be familiar with the pickle module, however, if not it’s good to know that the pickle module allows you to pickle a file using de-serialization which means simply breaking down an object into its constituting components. For e.g, our model files attribute like the one we saw.

To save a file using pickle one needs to open a file, load it under some alias name and dump all the info of the model. This can be achieved using below code:

##### loading library
import pickle
##### create an iterator object with write permission - model.pkl
    with open("D:\\data\\model_pickleonLinearreg", 'wb')as f:
        pickle.dump(reg,f)
    
    
 #### One can load this file back again into a model using the same logic, here we are using the reg variable for referencing the model and then using it to predict the per capital income on the year of 2020

##### load saved model
    with open("D:\\data\\model_pickleonLinearreg", 'rb')as f:
       model=pickle.load(f)

##### check prediction
model.predict([[2020]]) # similar

