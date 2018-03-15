[Link to the video](https://www.youtube.com/watch?v=JNxcznsrRb8)
[Wiki of the video](http://forums.fast.ai/t/wiki-lesson-2/9399)

[This article](https://medium.com/@hiromi_suenaga/deep-learning-2-part-1-lesson-2-eeae2edd2be4) talks about the course

Read about [learning rates](https://towardsdatascience.com/understanding-learning-rates-and-how-it-improves-performance-in-deep-learning-d0d4059c1c10)

00:00 -> 3:37
blabla

3:37 -> 4:45 
explain what are the values output from the training

# What is the Learning rate

00:04:45 -> 7:34 What is a Learning Rate (LR),

7:34 -> 8:35 learning rate finder

8:35 -> 9:17 blabla scientific notation


9:17 -> 10:10
choose the right loss from the curve


10:10 -> 12:19
blabla my method is so much tougher than the others

12:19 -> 12:36
how to choose the learning rate (reminder)

12:36 -> 14:00
blabla 
question what is the advantage of this method
use this learning rate with adam

14:00 -> 14:53
question Adam finetunes learning rate itself
answer: Adam still needs a learning rate

(silence)

# Overfitting, getting more data

15:01 -> 15:49
use more data to avoid overfitting

# Data augmentation
15:49 -> 18:30
explanation of data augmentation

18:30 -> 19:15
question: why don't we take the learning rate corresponding to the minimal loss
can skip this because the teacher repeats the question

19:15 -> 21:21
answering the question

21:21 -> 23:04
blabla


23:04 -> 24:10
should we recompute the best learning rate at every epoch

24:10 -> 25:41
interesting but repeating the same explanation about data augmentation 

25:41 -> 29:10
precompute=True
don't recompute the activations that were 

29:10 -> 30:15
use precompute=False to make data augmentation efficient
interpretation of the result, the training loss is higher than validation loss meaning we are not overfitting

30:15 -> 40:32
cycle_len=1
learning rate annealing, decreasing the learning rate as we get closer to the minimum
cosine annealing
make jumps in the learning rate to find other minima
cycle_len parameters sets the number of epochs for each jump (1 means every epoch)
snapshot ensemple: save the weights for every minimum (see cycle_save_len parameter)

40:32 -> 42:33
save weights

(silence/inaudible question)

42:50 -> 43:49
train model from scratch
pre-computed activations

43:49 -> 48:23
finetuning
when retraining the precomputed model
unfreeze a layer to retrain it
46:39 create array of learning rates for every layer

48:23-> 49:45
question repeating for which layers are the different learning rates for

49:45 -> 50:25
difference with grid search

50:25 -> 51:01
what if we have images of different size
answer is we talk about this later

51:01 -> 51:16
can we set a learning rate for only one layer
yes: unfreeze_to(layer_number)

51:16 -> 51:39
in practise we never need to do this

(silence)

51:43 -> 52:28
does it help if little data
no, it helps when have limited GPU ressources
you can only freeze layers from layer n onwards


52:28 -> 55:25
go back to learning rates cycles explanation
cycle_mult doubling the length of the cycle after each cycle
explore quickly at the begining then explore the minima better

(silence)
55:29 -> 56:50
question then explaning again why do we explore different minima
size of the minima

56:50 -> 1:00.03
why non square images get wrong predictions
use data augmentation during prediction
TTA:test time augmentation

1:00.03 -> 1:01.35
train time augmentation vs test time augmentation

1:01.35 -> 1:02.27
what is the padding ?
-> one kind of data augmentation "add a border"
reflection padding


1:02.27-> 1:03.29
should we zoom or use padding

(silence)

question: data augmentation for things other than image ?
underdevelopped -> 1:04.19

(silence)

use a sliding window ?
not for training time
maybe for test time augmentation, still under testing -> 1:05.36

# Libraries

1:05.36 -> 1:10:53
blabla...
question the ML are open source ?
fast.ai is open source
pytorch... not easy to use, but very powerful
they tryed to build a library on top of pytorch
blabla...

(silence)

1:11.04 -> 1:11.47
blabla...
question pyro ?

(break)

1:11.47 -> 1:13:00
confusion matrix (plot_confusion_matrix)

1:13:00 -> 1:13:52
plotting the images on wich the model was wrong

1:13:52 -> 1:16:39
summarize what we need to do to make a good image classifier
how to setup lr_find and which layers to retrain

1:16:39 -> 1:17:32
training the model again for an other kaggle competition
presenting the competion: recognizing dogs

1:17:32 -> 1:19:32
using kaggle-cli to download images
(blabla)
using pandas to read the csv file containing the labels

1:19:32 -> 1:23:00
configuring training
1:21:35 configuring cross validation 


1:23:00 -> 1:29:20
blabla
tools to get the file names
1:24:43 python dict comprehension
python * before variable means transform container into coma separated content
1:25:30 tricks to see a histogram of the size of the images
1:26:30 question about the size of the validation set depends how accurate the model has to be on the real data
1:28:27 how big is the thing I am looking for in the image


1:29:20 -> 1:30:55
shrink images at the begining of the training for faster computation
when we use bigger images or bigger batch size the GPU may run out of memory...

1:30:55 -> 
