# Table of contents
- [CISI Dataset](#cisi-dataset) 
    - [Reference](#reference)
    - [Context](#context)
    - [Content](#content)
    - [Acknowlegments](#acknowledgements)
- [Stopwords dataset](#stopwords-dataset)

# CISI Dataset
A dataset for Information Retrieval   
A public dataset from the University of Glasgow's Information Retrieval Group   
## Reference 
[Kaggle](https://www.kaggle.com/datasets/dmaso01dsta/cisi-a-dataset-for-information-retrieval)  

## Context
This is a text-based dataset that can be used for Information Retrieval (IR). It is publicly available from the University of Glasgow (http://ir.dcs.gla.ac.uk/resources/test_collections/cisi/).

## Content
The data were collected by the Centre for Inventions and Scientific Information ("CISI") and consist of text data about 1,460 documents and 112 associated queries. Its purpose is to be used to build models of information retrieval where a given query will return a list of document IDs relevant to the query. The file "CISI.REL" contains the correct list (ie. "gold standard" or "ground proof") of query-document matching and your model can be compared against this "gold standard" to see how it has performed.

## Acknowledgements
As mentioned above, this dataset has been made publicly available by the Information Retrieval Group at the University of Glasgow (https://www.gla.ac.uk/schools/computing/research/researchsections/ida-section/informationretrieval/).


# Stopwords dataset
Stopwords are common words that are often ignored in text processing since they occur frequently but don't carry significant meaning. Examples of stopwords include "the," "is," "in," "and," "with," etc.

In the context of NLTK, you can access a pre-defined list of stopwords for various languages. Here's how you can use the NLTK library to work with stopwords:

1. Installing NLTK: If you haven't already, install NLTK using pip install nltk.

2. Downloading the Stopwords Dataset: Use the following command to download the stopwords dataset:
```
import nltk
nltk.download('stopwords')
```
3. Accessing the Stopwords for a Specific Language: You can access the stopwords for a specific language, like English, using the following code:
```
from nltk.corpus import stopwords
stop_words = set(stopwords.words('english'))
```
`stop_words` will be a set containing English stopwords.

4. Removing Stopwords from Text: You can remove stopwords from a given text using a list comprehension. Here's an example:
```
words = ["this", "is", "a", "sample", "text"]
filtered_words = [word for word in words if word not in stop_words]
```
`filtered_words` will contain the words from `words` that are not in the `stop_words` set.

NLTK provides stopwords for several languages, so you can use the appropriate language code in the `stopwords.words()` function to get stopwords for other languages. You can see the full list of available languages with `stopwords.fileids()`.
