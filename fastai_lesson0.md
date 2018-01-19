# Video
Actual lessons starts at : 23:22
23:22 -> 29:44 Explanation of convolution (convolution-intro.ipynb)
29:44 -> 33:05 Explanation of MaxPooling
33:05 -> 35:47 Correlate average maxPooling result, compare square error
35:47 -> 37:21 Discussion about convolution filter
37:21 -> END   Linear regression (sgd-intro.ipynb : define straight line, and make gradient descent matplotlib animation)


# Notebook convolution-intro.ipynb
be able to display handwriten numbers and show the result of the convolution product on an image

# Notebook mnist.ipynb
## Setup
Steps:
- download the dataset 
- use np.expand_dims to reshape X_train (60000, 28, 28) -> (60000, 1, 28, 28)
- create y_train = onehot(y_train) -> transform values [0 - 9] into vector of zeros and one at the right value
[5, 0, 4, 1, 9] -> [
        [ 0.,  0.,  0.,  0.,  0.,  1.,  0.,  0.,  0.,  0.],
        [ 1.,  0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.],
        [ 0.,  0.,  0.,  0.,  1.,  0.,  0.,  0.,  0.,  0.],
        [ 0.,  1.,  0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.],
        [ 0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.,  0.,  1.]]
- normalize X_train (x-mean_px)/std_px

## Linear Model
Steps:
- Define the model: normalize + Dense 10
- create generators for test set and train set (keras internal use)
- Train the model: (There may be problems with keras version "N became n")