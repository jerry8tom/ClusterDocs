# ClusterDocs
Cluster documents with similar semantic description.

## The Data
300 text files of various formats (ANSI, utf-8, utf-16..) containing englis words and special characters. 

## The Cleaning
- Converted all the files to simple python strings while reading.
- Removed all the stop words, symbols, converted the string to lowercase. 
- Put the sender, receiver and body of the documents into a dataframe for easy manipulation.

## Visualising the data
It is always a good idea to get an insight into the data that we will be working on.
Here I have displayed the most common terms in the corpus after cleaning.
![wordCloud](images/word_cloud.png)

As we can see words like 'people', 'image', 'jpeg', 'file' are the most common terms.
To further quatify we can represent the terms against their frequency.

![wordCount](images/word_count.png)

## Text to Vectors
In order to study the text data we must convert it into numerical(vector) form so that it becomes quantifiable. 
For us finding the frequency of terms and their similarity is useful since we wish to cluster them together.
This is the reason we use tf-idf (term frequency-inverse document frequency) as it refelects the importance of text in the corpus.

![TFIDF](images/tfidf.png)

These are the top 10 terms with highest mean tf-idf.



## The Dependencies
```
pip install -r requirements.txt
```
