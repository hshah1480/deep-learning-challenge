# Deep Learning
# Module 21 Challenge

# Background:
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

# Report:
## Overview
The aim of this investigation is to develop a binary classifier employing a deep learning neural network, which can forecast the approval rate of applicants seeking funding from Alphabet Soup, a nonprofit organization. The dataset furnished includes details on more than 34,000 organizations, encompassing attributes like application type, affiliated industry sector, government organization categorization, funding utilization purpose, income classification, requested funding amount, and effectiveness of fund usage. The analytical process commences with data preprocessing, involving the elimination of redundant columns, encoding categorical variables, and partitioning the data into training and testing sets. Subsequently, the neural network model is conceived, trained, and assessed to gauge its loss and accuracy. Lastly, the model undergoes optimization through diverse techniques, including adjustments to input data, augmentation of neurons and hidden layers, employment of varied activation functions, and fine-tuning the number of epochs. The ultimate objective is to attain a predictive accuracy surpassing 75% and to archive the optimized model in an HDF5 file format.

# Results:
## Data Preprocessing
* The column named "IS_SUCCESSFUL" is the target of this model (dependent variable). If true, the money was used effectively.
* The features of this model are the NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT
* For all optimization attempts "EIN" variable was removed as the data is neither a Target or a Feature.
* Different variables were excluded in the various optimization models - "STATUS", "SPECIAL_CONSIDERATIONS", "NAME"


# Compiling, Training, and Evaluating the Model
## Original Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  **Answer:** 2 hidden layers were used in the original model of 80 and 30 neurons respectively. Activation function of "ReLU" were used for both. The outer layer activatuon was "Sigmoid". 100 Epochs were used to train the model.


* Were you able to achieve the target model performance?
  **Answer:** No, the result was 72.4%


# Optimization model 1

* What steps did you take in your attempts to increase model performance?
  **Answer:** n my first optimization model, I tried adding another hidden layer and increasing the nodes to 100, 30 and 10. Activation of "ReLU" was used on the first layer and the "Sigmoid" on the 2nd & 3rd layer.

* Were you able to achieve the target model performance?
  **Answer:** No, the result was 72.8%


# Optimization model 2

* What steps did you take in your attempts to increase model performance?
  **Answer:** I dropped 'SPECIAL_CONSIDERATIONS' column along with 'EIN' and 'NAME'.
I changed the 'APPLICATION_TYPE' cut-off from 500 to 700.
In my second optimization model, I changed the nodes to 100, 60 and 20. Activation of "ReLU" on the first and second layer and "Sigmoid" 3rd.

* Were you able to achieve the target model performance?
  **Answer:** No, the result was 72.5%


# Optimization model 3

* What steps did you take in your attempts to increase model performance?
  **Answer:** I dropped 'SPECIAL_CONSIDERATIONS' 'EIN' and 'STATUS' columns.
 I chose a cut-off value for 'NAME' of 4 which reduced the number of records to 475. In my third optimization model, I changed the nodes to 25, 15 and 3. Activation of "ReLU" on the first layer and "Sigmoid" on the second and third.

* Were you able to achieve the target model performance?
 **Answer:** Yes, the result was 79.2%



# Summary:
In summary, the utilization of TensorFlow and Keras in constructing a deep learning model yielded a predictive accuracy of 79% when categorizing the success of organizations supported by Alphabet Soup using their distinctive features. Various optimization strategies were employed during the model's development, encompassing the removal of columns, categorical variable binning, incorporation of hidden layers and neurons, and experimentation with different activation functions, among other fine-tuning adjustments. It's worth noting that the intended predictive accuracy threshold of 75% was met, but it demanded extensive optimization iterations to attain this level of performance.


