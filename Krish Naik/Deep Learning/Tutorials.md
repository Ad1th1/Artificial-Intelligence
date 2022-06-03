Tutorial 1: Introduction to Neural Network and Deep Learning (Note 1)

- Deep learning -> Neural Networks -> Perceptron 
- ANN, CNN, RNN
- Jeoffrey Hinton -> invented back-propogation
- give a neural network, features and inputs. Train it to learn new things
- input layer -> layer of any number of neurons (hidden layer, line from each input to one neuron) -> output layer

_________________________________________________________________________________________

Tutorial 2: How does Neural Network work? (Note 1)
- Forward Propogation
  - inputs, weights assigned to inputs -> passed to hidden neuron
  - hidden neuron -> activation function
  - bias is added
  - weight updating happens with backwards propogation
  
_________________________________________________________________________________________

Tutorial 3: Activation Functions: (Note 1)

- Sigmoid Activation Function = used in logistic regressions = always used to get the final output in classification problems
- Relu Activation Function = used in regression and hidden layers of classification

_________________________________________________________________________________________

Tutorial 4: How to train neural networks with back-propogation: (Note 1)
- loss function, minimize loss and update weights
- requires back propogation to update weights
- learning rate (subtracted from old weight to get new weight on updation) must be very small
- vanishing and exploding gradient

_________________________________________________________________________________________

Tutorial 5: Multilayer Neural Network and Gradient Descent (Note 2)
- loss function calculated -> minimized using optimizer and updation of weight takes place using gradient descent
- select a suitable learning rate (using hyperparameter optimization) 
- loss needs to decrease after several changes / hops vis a vis forward and backward propogations

______________________________________________________________________________________

Tutorial 6: Chain Rule in Backpropogation (Note 2)
- backpropogation is all about weight updation to minimize loss
- learning rate is found using hyperparameter optimization

_______________________________________________________________________________

Tutorial 7: Vanishing Gradient Problem (Note 3)
- sigmoid maps inputs to a value from 0 to 1
- derivative of sigmoid is from 0 to 0.25
- as we keep backpropogating, derivative value keeps decreasing
- as number of hidden layers keeps increasing, derivative value keeps decreasing
- this is the problem of sigmoid -> caused by the range of derivative of sigmoid being between 0 and 0.25 
- derivative might become super smaall -> w(new) might be approximately equal to w(old)
- same problem is caused even by tan(h), whose derivate ranges between 0 and 1
- vanishing gradient problem was the reason early developers used very small number of neural networks.
- This problem is solved by using relu functions

_______________________________________________________________________________



















