# Heart-Disease-ML
Creating a neural network to predict the possibility of someone getting heart disease within 5 years

Neural networks have been a recent discovery within the field of computer science, and have been used in many different scientific fields. For example, neural networks and other machine learning networks such as bayesian networks, have been used in the healthcare field. This is due to the fact that doctors cannot diagnose a patient quick enough so using artificial intelligence makes disease/disorder diagnosis faster and more efficient

In this neural network, I focus on heart disease, and given an input of certain attributes or features of a person, the network should be able to decipher the probability of the person getting a diagnosis for heart disease within the next five years.

So, firstly, I will explain a few machine learning concepts present in the neural network 


Neural networks
- neural networks are designed to learn a certain concept given a dataset, and since computers can process a lot of information, they can train the data and "learn" to generalize information from the given data.


Neurons and densely-connected layers
- neural networks, also known as artificial networks, are modeled similarly to how the brain processes information. In order to visualize the neurons and the layers in the neural network, I have provided a link to a picture of its structure
https://www.google.com/search?sa=G&hl=en&q=neural+network+dense+layer&tbm=isch&tbs=simg:CAQSlQEJEXoHkcJRnWQaiQELEKjU2AQaBAgVCAoMCxCwjKcIGmAKXggDEiZVkQhWnAiYCNIdkgj-ApkImwiWPsU9xD3AJ681wz2MKcY90DawNRow6ckWPz6CcBT_1pfDK6jsqk8vgcdo0ZJS52QPXlItVxSeIFUv1jsbZHFBhgy0D1udbIAQMCxCOrv4IGgoKCAgBEgQ7oBKQDA&ved=0ahUKEwiEhseCpe7gAhWtSt8KHX0cDNMQwg4IKCgA

Neural networks have an input layer, which consists of a certain number of neurons, dependent on the network. At the end, it has an output layer, which usually consists of less neurons than the input layer. In the middle, there are layers known as hidden layers, which the network performs complex mathemetical operations and propogates the data(moves forward) to the next layer.




Gradient descent




Propogation and backpropogation



If you have any other further questons regarding any of these topics, as they are very difficult to understand, I recommend watching these videos by 3Blue1Brown. He does a great job of explaining these difficult concepts.
https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi

Also, for this particular neural net, I used the cleveland dataset from the UCI repository. https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/processed.cleveland.data

Ok, so now I am going to explain what each line of my code does, and the overall format of the neural network.


Structure/Architecture
input layer- 10 nodes, relu activation
hidden layer 1- 40 nodes, relu activation
hidden layer 2- 15 nodes, relu activation
hidden layer 3- 5 nodes, relu activation
output layer- 1 node, sigmoid activation for probability



In the beginning, we import dense layers and sequential model from the keras library, as well as numpy and h5py. If you need help downloading all the libraries, as well as tensorflow and python 3.7, here is a link to a video explaining how to do it. 
https://www.youtube.com/watch?v=59duINoc8GM


Numpy_random_seed produces a random seed with a certain data for the network, so if other people used the same seed with the neural netowork they can reproduce the results of it.



After we specify the seed, we need to load in our dataset. Whether it is a neural network on heart disease, diabetes, lung diseases, etc, you need to load in a dataset so that your network can train and test the data.  I reccomend using the UCI repository to find the dataset that you need for your own neural network. The delimiter just indicates that the commas in our dataset split up the data, so for example, if our data went like 30.0, 68.0, 75.0, etc,  we need to specify that the comma seperates the numbers as they are different inputs or attributes. 


Next, once we give our neural network the dataset, it doesn't know the inputs and outputs. So, we need to specify the which numbers represent the inputs in our dataset and which number represents the output. The network will need to know the output because it will use the cost function to minimize the loss of the data, which will improve the accuracy of the network.



