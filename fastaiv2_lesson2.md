[Link to the video](https://www.youtube.com/watch?v=JNxcznsrRb8)
[Wiki of the video](http://forums.fast.ai/t/wiki-lesson-2/9399)

[This article](https://medium.com/@hiromi_suenaga/deep-learning-2-part-1-lesson-2-eeae2edd2be4) talks about the course

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