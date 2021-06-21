# Category Prediction Through Description using BERT MODEL

## NLP
Details-
Use a given dataset to build a model to predict the category using description. Write code in python. Using Jupyter notebook is encouraged. 

  1) Show how you would clean and process the data
  2) Show how you would visualize this data
  3) Show how you would measure the accuracy of the model
  4) What ideas do you have to improve the accuracy of the model? What other algorithms would you try?

## About Data : 
You have to clean this data, In the product category tree separate all the categories, figure out the primary category, and then use the model to predict this.
If you want to remove some categories for lack of data, you are also free to do that, mention this with explanation and some visualization.
Questions are made this way to check if candidates are able to understand this.

## Note: 
1) Goal is to predict the product category.
2) Description should be the main feature. Feel free to use other features if it'd improve the model.
3) Include a Readme.pdf file with approach in detail and report the accuracy and what models were used.

# Product Classifier #
This project is about multi class classification using NLP.
Here we are provided with flipkart dataset from which we have to predict the primary category using product description.


## Installation
In order to reproduce the results produced by the notebook the following needs to be installed.
Use of virtual environment while installing these libraries is preferable.
 
~~~
pip install -q tensorflow-text
pip install -q tf-models-official
pip install wordcloud
pip install gensim
pip install nltk
pip install spacy
pip install transformers
pip install wget
pip install transformers
pip install wget
pip install pandas
pip install numpy
pip install seaborn
pip install matplotlib
pip install torch
~~~

# Approach

### 1) Data For Analysis
    From the product_category_tree we consider the primary catergory as the root of this tree. 
    Example: For the category given tree '["Footwear >> Women's Footwear >> Ballerinas >> AW Bellies"]' the primary category is Footwear
    
### 2) Exploratory Data Analysis
    Visulazation of Dataset is being done under this section
    
### 3) Data Cleaning
    Data is being cleaned before going through Data Preparation
    
### 4) Data Preparation
    Data preprocessing is done in the following fashion.
    Tokenization of the description of the product. (Post cleaning the description for the product).
    Lemmatizing the tokenized data in-order to prepare it for usagein the model.
 
### 5) Model Preparation and Training
    Here we are removing all the product categories for which less than 10 products are present.
    
### 6) Result
    So,after detailed analysis I have used BERT(Bidirectional Encoder Representations from Transformers) Model. It is designed to pre-train deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context. 
#### F1-Score
    
#### Training loss: 0.018742394280544406
#### Validation loss: 0.15305931800355793
#### F1 Score (Weighted): 0.9792079018736954

![Screenshot 2021-04-10 at 10 51 17 PM](https://user-images.githubusercontent.com/41789975/114278837-44a9ba80-9a4f-11eb-9d18-84c401c7c601.png)

#### Accuracy

![Screenshot 2021-04-10 at 10 52 21 PM](https://user-images.githubusercontent.com/41789975/114278883-6acf5a80-9a4f-11eb-8f25-7200aa0cb365.png)

![Screenshot 2021-04-10 at 10 52 45 PM](https://user-images.githubusercontent.com/41789975/114278898-791d7680-9a4f-11eb-8a05-c5ebe7de6117.png)
