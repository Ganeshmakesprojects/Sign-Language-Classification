# Sign-Language-Classification

Overview : CNN on sign language data set with 24 labels.

# Data Preprocessing
A .csv file with 785 columns with 1st column as label and next 784 columns as 28x28 image data (grey scale 0-255)
Use the data to create a np array with dimensions of (#num_instances, 28,28,1)

Note: The labels have a range of [0,24] but 9 label is not in the data so converted into [0,23] i.e. 24 labels.

# Model Used
A 3x3 CNN is used with 2 layers of Convolutions and 2 layers of MaxPooling with input shape of (28,28,1). 
Then Flattened and use a Dense layer and last layer with 24 nodes.
The activation function is 'relu' except the last layer which has 'softmax'.

Compile with Sparse categorical crossentropy (as higher number of labels) along with 'adam' otimizer.

# Results
With 25 epochs of training,
Training accuracy : 
Validation accuracy : 
If the Validation set is used again to evaluate the testing accuracy falls to 

A visualizartion is given on how the accuracy and Loss across epochs for both Training and Validation makes good progress at the start and flattens out at the end.
