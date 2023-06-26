# Fake-News-Real-News

Files are in Releases you can have it by clicking on the tag button above the project.

# 1. Data Preprocessing:
In this step, we combine the fake and real news datasets into a single dataset. The data is 
then shuffled to ensure a random distribution. The dataset is split into training, validation, 
and test sets using the train_test_split function from scikit-learn. The news titles are 
preprocessed by converting them to lowercase, removing non-alphabetic characters, and 
performing stemming using the PorterStemmer from the NLTK library.

# 2. Word Embedding:
The news titles are tokenized using the Tokenizer class from TensorFlow's Keras library. 
This class is used to tokenize the words and create sequences. The titles are then padded 
to a maximum length of 42 using the pad_sequences function. The padding ensures that 
all sequences have the same length, which is required for input to the LSTM model.

# 3. Model Selection and Implementation
In this step, we choose the LSTM model for detecting fake news. The model consists of 
an Embedding layer, an LSTM layer with 128 units, and a Dense layer with a sigmoid 
activation function for binary classification. The Embedding layer is used to learn the 
representation of words in the news titles. The LSTM layer helps capture the contextual 
information and dependencies between words. The output layer with sigmoid activation 
predicts the probability of the news being fake or real.

# 4. Evaluation and Testing:
The model is compiled with the Adam optimizer and binary cross-entropy loss function. 
It is then trained on the training set and validated on the validation set using the fit 
method. The model is evaluated on the test set to obtain the test loss and accuracy.

# 5. Predicting News Label:
The predict_news function is implemented to preprocess the input news and predict its 
label (fake or real). The input news is preprocessed using the same steps as during 
training and then tokenized and padded. The loaded model is used to make predictions on 
the processed input news, and the label is determined based on the prediction probability.

# 6. Conclusion: 
This code demonstrates a pipeline for detecting fake news using an LSTM model. The 
dataset is preprocessed, the LSTM model is trained and evaluated, and the model is then 
used to predict the label of an input news. The LSTM model is chosen for its ability to 
capture sequential dependencies in text data. The code can be further enhanced by 
incorporating additional preprocessing steps, exploring different model architectures, and 
using more advanced natural language processing techniques
