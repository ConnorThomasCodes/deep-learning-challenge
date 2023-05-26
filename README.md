# deep-learning-challenge

### Overview
In this repository, we attempt to take in data from fictional nonprofit Alphabet Soup and create a neural network model to help deternmine which applicants they fund yield a successful/effective use of the donated money

### Preprocessing
* In this case, our target column was "IS_SUCCESSFUL". This was a boolean value with 0 for unsuccessful and 1 for successful
* All other columns served as features in our model. Before creating our neural network, we binned entries from "APPLICATION_TYPE", "CLASSIFICATION", and later on "ASK_AMT"
* We dropped the "EIN" and "NAME" columns as well

### Optimization
* The original neural network was created with 3 hidden layers, with 4, 8, and 8 nodes respectively, and an output layer using tanh as an activation function. It yielded Loss: 0.5554224848747253 and Accuracy: 0.7255976796150208.
* After several attempts at optimization, our best model only yielded Loss: 0.5555945038795471 and Accuracy: 0.7282798886299133. This is a very small improvement over original model (<0.003 increase in Accuracy).
* To optimize our model, we created bins for the "ASK_AMT" column at cutoff values. We also tried increasing the number of nodes in our layers to a much higher number, increasing the amount of hidden layers in our model, and changing our activation function to "sigmoid", but none of these yielded any significant improvement over our original model.
