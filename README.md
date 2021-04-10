# MIDAS-TASK-3
This repository is mainly the solution of MIDAS Summer Internship Task-3
## Task 3: NLP
Assignment Details-
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
STEP-1 Splitting the product categories in order to get the primary category

~~~
df['product_category'] = df['product_category_tree'].str.strip('["*]"').str.split('>>').str[0].str.strip()
~~~

STEP-2 Then we figure out the top ten product categories

~~~
df['product_category'].value_counts(normalize=True)[:10].plot(kind="bar")
~~~

STEP-3 Declaring a new column namely "Number_of_Words" in order to count the words present in the product description

~~~
data_df['Number_of_words'] = data_df['description'].apply(lambda x:len(str(x).split()))
~~~

STEP-4 
