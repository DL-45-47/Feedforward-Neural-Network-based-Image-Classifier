## Assignment 1 - Feedforward Neural Network

### Report Link : 
https://wandb.ai/prachisahu47/Feed_Forward_Neural_Network_modules/reports/Copy-of-miteshk-s-Assignment-1--Vmlldzo1MzA0MDA

### Files :
* **DLA1.ipynb** - Final executable code with Sweep functionality
* **DLA1_test_plot.ipynb** - Extra module for confusion matrix plot and accuracy plot on test data
* **README.md** - Brief description about project

### Quick Run :
* Firstly execute *sweep_config* and *wandb.sweep* modules that initialize sweep with parameters and return sweep id.
* Then execute *wandb.agent* that train model with various combination of parameters.<br/>
**Note -** *It is suggested to pre-run all modules i.e. import, algorithms and supportive functionalities.*

### Key Points for Execution :
* It is a modular code in jupyter notebook format.
* One who needs to run this notebook should have a wandb login which is needed for execution of the code.
* Code is structured based on sweep functionality. There are two important sweep functions -
  * wandb.sweep - to initiate sweep with config parameters and project name and returns sweep id
  * wandb.agent - take parameters as sweep id and function name to be executed in loop with different combinations of parameters.
* All Functionalities as given below are also essential for successful execution of Gradient descent algorithms.
* It is preferred to execute all algorithm at begin as well, since sweep function randomly choose algorithms for execution.

### Algorithms included :
* **Gradient Descent**
* **Stocastic Gradient Descent**
* **Momentum Gradient Descent**
* **Nesterov Accelerated Gradient Descent**
* **RMSProp Gradient Descent**
* **Adam Gradient Descent**
* **Nadam Gradient Descent**

### Functionalities used :
* **forward_prop** - Apply forward propagation using weights and bias and return activation layer, preactivation layer and output layer values
* **backward_prop** - Apply backpropagation using activation layer, preactivation layer and output layer values and return gradient of weights and bias
* **init_w_and_b** - Initiate weights and bias
* **activation_func** - Based on choice of activation function, returns corresponding result of activation function
* **activation_func_derivative** - This function helps in calculation of derivative of activation function in backpropagation algorithm
* **softmax** - Calculate softmax function for output layer using pre-activation layer output
* **cross_entropy** - Calculate cross entropy loss on training set by applying L2-regularization
* **val_cross_entropy** - Calculate cross entropy loss on validation set by applying L2-regularization
* **mean_squared_error** - Calculate mean sqaured error on training set by applying L2-regularization
* **val_mean_squared_error** - Calculate mean squared error on validation set by applying L2-regularization
* **get_accuracy** - Calculate accuracy on training set
* **val_get_accuracy** - Calculate accuracy on validation set
* **predict** - Uses input, weights and bias and returns vector of predicted probability corresponding to each class as result
