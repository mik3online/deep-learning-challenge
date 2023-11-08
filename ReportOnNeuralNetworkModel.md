# deep-learning-challenge

**Report on the Performance of Deep Learning Model for Alphabet Soup**

**Overview of the Analysis:**

The purpose of this analysis is to create a deep learning model to predict whether applicants will be successful if they receive funding from Alphabet Soup, a charity organization. To achieve this, I preprocess the data, compile, train, and evaluate a neural network model.

**Results:**

**Data Preprocessing:**

- **Target Variable(s):** The target variable for the model is "IS_SUCCESSFUL," which indicates whether an applicant was successful in receiving funding from Alphabet Soup.

- **Feature Variable(s):** The features for the model are all the columns in the dataset, except "EIN" and "NAME," which were removed as they are not targets or features.

- **Variable(s) Removed:** None of the variables were removed from the input data.

**Compiling, Training, and Evaluating the Model:**

- **Neurons, Layers, and Activation Functions:** The neural network model (nn) consists of two hidden layers and one output layer. The first hidden layer has 80 neurons with the ReLU activation function. The second (optional) hidden layer has 30 neurons with the ReLU activation function. The output layer has a single neuron with a sigmoid activation function.

- **Model Performance:** The model achieved a loss of approximately 1.43 and an accuracy of approximately 0.71 during training and evaluation. While the model's accuracy is relatively good, there may be room for improvement in the loss metric.

- **Steps Taken to Increase Model Performance:** The analysis followed a series of data preprocessing steps, including binning of categorical variables like "APPLICATION_TYPE" and "CLASSIFICATION" to reduce the number of unique values. Additionally, data was scaled using the StandardScaler, and a neural network with two hidden layers was created. Further optimizations can be explored to enhance model performance.

**Summary:**

The deep learning model showed potential for predicting the success of applicants for Alphabet Soup funding. However, there is room for improvement, as the model may benefit from further fine-tuning. In conclusion, while the initial deep learning model provides a good starting point, further experimentation and refinement are needed to optimize its performance for Alphabet Soup's specific classification problem. The following were experimental attempts to optimize the model…

**Optimize the Model - Attempt 1 - Add Hidden Layers:**

- **Model Description:** In this attempt, I expanded the neural network model (nn2) by adding more hidden layers with different numbers of neurons.

  - First hidden layer: 80 neurons with ReLU activation
  - Second hidden layer: 40 neurons with ReLU activation
  - Third hidden layer: 30 neurons with ReLU activation
  - Fourth hidden layer: 20 neurons with ReLU activation
  - Fifth hidden layer: 10 neurons with ReLU activation
  - Output layer: 1 neuron with sigmoid activation

- **Performance:** Unfortunately, this model did not achieve the target performance, as it resulted in a relatively high loss of approximately 0.73 and an accuracy of only about 0.53. The addition of extra hidden layers did not improve model performance in this case.

**Optimize the Model - Attempt 2 - Add Hidden Layer, Change Optimizer to SGD:**

- **Model Description:** In this attempt, I introduced a new neural network model (nn3) by keeping the original architecture and changing the optimizer to Stochastic Gradient Descent (SGD) with a custom learning rate.

  - First hidden layer: 80 neurons with ReLU activation
  - Second hidden layer: 40 neurons with ReLU activation
  - Third hidden layer: 25 neurons with ReLU activation
  - Output layer: 1 neuron with sigmoid activation

- **Performance:** Unfortunately, this model also did not achieve the target performance. The optimizer change resulted in an extremely high loss of approximately 886,500,294,656.0 and an accuracy of only about 0.53. This optimizer change did not improve the model's performance.

**Optimize the Model - Attempt 3 - Change Optimizer to Adagrad:**

- **Model Description:** In this attempt, I created a new neural network model (nn4) with the original architecture and changed the optimizer to Adagrad.

  - First hidden layer: 80 neurons with ReLU activation
  - Second hidden layer: 40 neurons with ReLU activation
  - Third hidden layer: 25 neurons with ReLU activation
  - Output layer: 1 neuron with sigmoid activation

- **Performance:** This model showed slightly improved performance compared to the previous two attempts. It achieved a loss of approximately 0.68 and an accuracy of about 0.59. While it didn't reach the target model performance, it performed better than the previous two models.

**Summary of Model Attempts:**

In summary, the initial deep learning model provided the best performance with a loss of approximately 1.43 and an accuracy of about 0.71. The subsequent model attempts, which involved adding more hidden layers and changing the optimizer, did not result in significant improvements. It is essential to note that improving the model's performance may require further optimization of hyperparameters, model architecture, or additional feature engineering.
