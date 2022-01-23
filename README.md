# Sign-Language-Classification

Overview : CNN on sign language data set with 24 labels.

# Kaggle Dataset Link
https://www.kaggle.com/datamunge/sign-language-mnist

# Data Preprocessing
A .csv file with 785 columns with 1st column as label and next 784 columns as 28x28 image data (grey scale 0-255) <br>
Use data to create an np array with dimensions of (#num_instances, 28,28,1)<br>

Note: The labels have a range of [0,24] but 9 label is not in the data so converted into [0,23] i.e. 24 labels.

# Model Used
A 3x3 CNN is used with 2 layers of Convolutions and 2 layers of MaxPooling with input shape of (28,28,1). <br>
Flattened and added a Dense layer and last Dense layer with 24 nodes.<br>
The activation function is 'relu' except the last layer which has 'softmax'.

Compile with Sparse categorical crossentropy (as higher number of labels) along with 'adam' otimizer.

# Results
With 25 epochs of training,<br>
Training accuracy : 92.3% <br>
Validation accuracy : 98.2% <br>
When the Validation set (7k+ images) is used again to evaluate the testing accuracy falls to 86.8% <br>

A visualization at the end on how the accuracy and Loss across epochs (for both Training and Validation) makes good progress at first but slows down at the end.
