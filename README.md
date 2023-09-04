# Amazon-ML-challenge 23'

The goal is to develop a machine learning model that can predict the length dimension of a product. Product length is crucial for packaging and storing products efficiently in the warehouse. Moreover, in many cases, it is an important attribute that customers use to assess the product size before purchasing. However, measuring the length of a product manually can be time-consuming and error-prone, especially for large catalogs with millions of products.

The dataset comprises of product title, description, bullet points, product type ID, and product length for 2.2 million products to train and test your submissions.


For the given problem statement, we have used Python programming language and various machine learning libraries like:

●	Scikit-Learn

●	Keras

●	PyTorch

●	Transformers (Hugging Face)

For performing NLP tasks we have used the following language model:

●	BERT

# Approach
1) Creating a BERT-based classifier and setting a fixed seed for reproducibility.
2) Performing the preprocessing tasks, such as handling duplicate entries and missing values.
3) The titles are then encoded into numerical values using a pre-trained multilingual version of BERT, and the encoded data is split into training and validation sets.
4) It then defines a PyTorch Dataset class and uses it to construct DataLoader instances for efficient iteration over the dataset during training and validation.
5) The script builds a classification model by adding a dropout and a linear layer on top of the pre-trained BERT model.
6) After setting up the learning rate scheduler and loss function, the training process is executed in a loop, where in each epoch, the model is trained on the entire dataset and then evaluated on the validation set.
7) The best-performing model on the validation set is saved.
8) Lastly, we evaluate the model using root mean square error (RMSE) as the metric.

