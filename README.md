# Heart-Disease-ML
Creating a neural network to predict the possibility of someone getting heart disease within 5 years

Neural networks have been a recent discovery within the field of computer science, and have been used in many different scientific fields. For example, neural networks and other machine learning networks such as bayesian networks, have been used in the healthcare field. This is due to the fact that doctors cannot diagnose a patient quick enough so using artificial intelligence makes disease/disorder diagnosis faster and more efficient

In this neural network, I focus on heart disease, and given an input of certain attributes or features of a person, the network should be able to decipher the probability of the person getting a diagnosis for heart disease within the next five years.

So, firstly, I will explain a few machine learning concepts present in the neural network 


Neural networks
- neural networks are designed to learn a certain concept given a data set, and since computers can process a lot of information, they can train the data and "learn" to generalize information from the given data.


Neurons and densely-connected layers
- neural networks, also known as artificial networks, are modeled similarly to how the brain processes information. In order to visualize the neurons and the layers in the neural network, I have provided a picture of the architecture that a neural netowrk tends to follow.



//put picture of neural networks


Neural networks have an input layer, which consists of a certain number of neurons, dependent on the network. At the end, it has an output layer, which usually consists of less neurons than the input layer. In the middle, there are layers known as hidden layers, which the network performs complex mathematical operations and propagates the data(moves forward) to the next layer. By going from layer to layer, it is able to increase its accuracy, and learn from the data. This is due to many concepts such as gradient descent and backpropogation.




Gradient descent
- Gradient descent is a mathematical way to reduce the cost function. Basically, it optimizes the performance of the program by finding the minimum of a function by continuoudly moving in the negative gradient, hence the name gradient descent. We use it to update the randomly assigned parameters(weights and biases) of the program so that we can find the right ones so that our model can accurately predict the answer. 

//put picture of gradient descent


Backpropagation
- Backpropogation is where you find how much a certain weight affects the functionality of the program. We adjust each weight in porportion to how much it actually affects the program. 

//put picture of backpropagation


If you have any other further questions regarding any of these topics, as they are very difficult to understand, I recommend watching these videos by 3Blue1Brown. He does a great job of explaining these difficult concepts.
https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi


Also, for this particular neural net, I used the Cleveland data set from the UCI repository. https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/processed.cleveland.data





Now I am going to explain what each line of my code does, and the overall format of the neural network.


Structure/Architecture
input layer- 10 nodes, relu activation
hidden layer 1- 40 nodes, relu activation
hidden layer 2- 15 nodes, relu activation
hidden layer 3- 5 nodes, relu activation
output layer- 1 node, sigmoid activation for probability



In the beginning, we import dense layers and sequential model from the keras library, as well as numpy and h5py. If you need help downloading all the libraries, as well as tensorflow and python 3.7, here is a link to a video explaining how to do it. 
https://www.youtube.com/watch?v=59duINoc8GM


//input images before explanation of code

Numpy_random_seed produces a random seed with a certain data for the network, so if other people used the same seed with the neural network they can reproduce the results of it.



After we specify the seed, we need to load in our data set. Whether it is a neural network on heart disease, diabetes, lung diseases, etc, you need to load in a data set so that your network can train and test the data.  I recommend using the UCI repository to find the data set that you need for your own neural network. The delimiter just indicates that the commas in our data set split up the data, so for example, if our data went like 30.0, 68.0, 75.0, etc,  we need to specify that the comma separates the numbers as they are different inputs or attributes. 


Next, once we give our neural network the data set, it doesn't know the inputs and outputs. So, we need to specify the which numbers represent the inputs in our data set and which number represents the output. The network will need to know the output because it will use the cost function to see how far the networks output is from the actual output and minimize the loss of the data, which will then improve the accuracy of the network.


Now, we don't want to train all of our data in the data set as we will have no data to test the model to check how effective it is. So, from keras, we import train_test_split and tell the computer how much data should be saved for training and how much should be used for testing(generally, it is 80-20 split or 75-25 split as a majority of the data should be used for training the model, and the remaining should be used for testing it. Random_state should just ________________


Next, we need to specify the model that we are using as well as add the layers, which are densely connected in this neural network. Keras makes this very simple, as once you import dense from keras.layers and dense from keras.models it takes a couple of lines of code to add the layers. First, you specify the model that you are using, which is sequential in this neural network. The sequential model is just a linear stack of layers, so you need to base your model of your datasets. Afterwards, you need to add all of your layers, such as the input layer, the hidden layers, and the output layer. So, you add each dense layers, and need to sepcify an activation for each layer, which I will explain shortly. However, for the input layer, you need to specify the dimensions to start the network, but you do not need to specify it for any of the other layers as the other layers automatically references the dimensions from the input layer. However, for every single layer in the neural network, you need to specify the activation in which to use. To summarize, a neural network gets the input neurons, does complex mathematical operations, uses an activation function, and passes that value to the next layer, and repeats this process until the end of the network. So, for each layer, the network uses a certain activation function, such as softmax, sigmoid,relu, etc. In this instance, we will be using relu activation for each layer until the final layer, in which we will use sigmoid activation. After we perform these complex operations, we use activation to turn that number into another number, dependeing on the certain activation. For example, the relu activation turns that number into either a 0 or a 1, while sigmoid activation takes that huge number and squishes it into a value between 0 and 1. So, relu activation is more commonly used nowadays, and we wuse it as activation for every layer(except the output layer) as it allows our network to propogate accurately and become more accurate. However, we use sigmoid activation for the last layer because we want a probability of getting heart disease as our ouput, and the sigmoid activation does that as it transforms the original number after the complex mathematical operations and squishes it to a number between 0 and 1. 


//Keep going through each line of code till done



So, that is how to make a neural network to diagnose heart disease in 15 lines of code. I hope you learned new information and gained knowledge on machine learning and neural networks, and make your own neural network in the future.


- Sanketh Gudapati







