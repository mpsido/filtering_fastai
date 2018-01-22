Base on this video https://www.youtube.com/watch?v=IPBSB1HLNLo&feature=youtu.be

blabla until 6:21
Can use cresle 


# Paperspace setup
6:21 -> 12:57
There is a paperspace setup we can run just like this
    curl http://files.fast.ai/setup/paperspace | bash
This command installs everything

Then here is how to run the notebook
    cd fastai
    git pull
    jupyter notebook


# Running the notebook
https://github.com/fastai/fastai/blob/master/courses/dl1/lesson1.ipynb

12:57 -> 14.49
blabla about how to use jupyter notebook
use python 3

14.49 -> 16:11 how to set up the data set
cresle vs paperspace setup


16:11 expected content of the folder
    !ls {PATH}
expected output: models  sample  test1  tmp  train  valid
blabla until 18:36


18:36 -> 18:44 (just follow the notebook)
plot the first cat

18:44 -> 20:00
how is composed the input image (rgb, pixels)

20:00 -> 20:27 context (not really useful)
dataset comes from kaggle, the accuracy used to be 80 %

20:27 -> 21:32
the three lines of code to do training
run the code and explain the output
loss function training set/validation set + accuracy

21:32 -> 24:13
blabla we are better than 2013 and it takes 17seconds
blabla we are using research papers
blabla we are using pytorch

24:13 -> 25:33
Get into the model 
how is labeled the training set
pytorch returns the log of the probability instead of the probability itself

25:33 -> 25:57
blabla learn to use numpy

25:57 -> 27:47
plot the correct images

27:47 -> 28:57
blabla we plot things because we want to understand where our model is wrong
28:25 -> 28:57 some images need data augmentation to be recognized because they are not correctly shaped


28:57 -> 30:53
blabla try with new images yourself

# What is a Neural network
30:53
blabla education is top down
blabla fast.ai has a different approach
blabla we are going to solve more and more problems
blabla zzzzz
33:57 -> 39:25 blabla course workflow 
39:25 -> 41:28 blabla try the code before knowing the theory
41:28 -> 44:44 blabla where the notebook spends time + where we can use image classifiers
44:44 blabla deep learning is a kind of machine learning

48:50 what is a neural network

49:48 presentation of gradient descent
in neural network we have one global minimum
gpu are good to run this algorithm

53:12 -> 57:00 blabla google invest in deep learning
microsoft skype translate

57:00 -> 59:14 blabla

59:14 -> 1:02.12
presentation of convolution

1:02.12 -> 1:04.27 non linear layer

1:04.27-> 1:08.00
principle of gradient descent
what is the learning rate

1:08.00 -> 1:11.36
displaying convolution filters layers

1:11.27 -> 1:11.57 30 seconds of blabla

1:11.57 -> 1:19.28
how to set the learning rate

1:19.28 -> 1:20.40
how to choose the number of epochs
run until accuracy gets worse (overfitting)

1:20.40 -> 1:21.57 
things to try

1:21.57 -> 
blabla jupyter trics (tab = autocompletion) (shift+tab = function parameters)
(shift+tab *2 = documentation)
(shift+tab *3 = documentation in a pop up window)
(?? + function = source code of the function)