Can skip "Overview" video

Final goal: making domain expert able to use deep learning
Part 1 best practises
Part 2 join research
7:23 we need GPU
9:28 amazon P2 instances

[amazon setup](http://wiki.fast.ai/index.php/AWS_install)

# Preparation lesson 1
47:47-> 59:48
* download the data from [here](http://files.fast.ai/data/)  (file dogscat.zip)
* alternative download from [kaggle](http://wiki.fast.ai/index.php/Kaggle_CLI)

maybe need to separate dogs and cats in different directories 54:18
57:25 split into training set and validation set (1000 cats and 1000 dogs)
58:22 sample directory (8 cats/dogs in train set, and 4 cats/dogs in test set)

http://files.fast.ai/models/ (file  vgg16.h5 )

source code from https://github.com/fastai/courses/tree/master/deeplearning1/nbs

# lesson 1
59:48->1:03.29 start lesson 1 but a lot of blabla until  summarized [here](http://wiki.fast.ai/index.php/Python_libraries)

1:03.29 -> 1:04.49
Explain:  
     %matplotlib inline
tells jupyter notebook do display matplot lib graphs inside the window

Explain why do we have a path variable (switch from sample to train data)

1:04.49-> 1:06.50 -> "blabla use anaconda"

1:06.50 -> 1:08.07  numpy

Import micellaneaous libs (utils.py)
   import utils

## Pretrained model
1:09.26 -> 1:14.06
pretrained with imagenet (worth a look)
images cathegories
the images only contain one thing, which is not real case use

1:14.06 -> 1:15.15 how do download the pretrained weigths

1:15.15 -> 1:17.05 presentation of vgg
vgg is not the most powerful but it is an easy to reuse base for image recognition

1:17.05 -> 1:18.49
7 lines of code introduction (not really useful)

1:19.02 -> 1:21.28 answer to the question why do we use pretrained models

## Keras backends

1:21.54 -> 1:24.32
vgg object
based on keras 
based on theano (transform python into GPU code)
theano is based on cuda/cudnn
keras can also convert to tensorflow code

1:24.32 -> 1:26.30
tensorflow vs theano
blabla about do we need lots of data and lots of GPU
1:26.30 -> 1:27.11
use tensorflow to manage multi GPU

1:27.11 -> 1:28.04
how to configure keras backend
1:28.04 -> 1:28.53
.theanorc configuration file to tell theano to use GPU


## Explain the 7 lines of code
1:29.29 -> 1:30.28 (useless blabla)
vgg object creation, lines of code behind the scenes

1:30.28 -> 1.30:48
minibatch
1.31:14 -> 1:32.07
GPU are efficient when we parallelize execution
not all of it at once because of GPU intern memory

1:32.07 -> 1:33.24
get_batches 
construct the mini batch from the content of the directory 
example : grab 4 images and 4 labels

1:33.24 -> 1:34.08
use vgg to tell us what it sees in the images (before finetuning)

1:34.08 -> 1:34.41
how sure vgg is 

1:34.41 -> 1:37.00
turn probabilities into finetuning