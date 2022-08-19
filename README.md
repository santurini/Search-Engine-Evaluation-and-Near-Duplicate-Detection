# Search Engine Evaluation and Near Duplicate Detection
![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

Exploiting the PyTerrier library to perform Search Engine Evaluation and Near Duplicate Detection on different datasets.

## PyTerrier - Search Engine Evaluation

PyTerrier is a software framework for information retrieval experiements in Python. 

*   It embeds all the previous frameworks;
*   It allows performing experiments in a **declarative way**.

#### Importing Datasets
The datasets module allows easy access to existing standard test collections. In particular, each defined dataset can download and provide easy access to:
* files containing the documents of the corpus
* topics (queries), as a dataframe, ready for retrieval
* relevance assessments (aka, labels or qrels), as a dataframe, ready for evaluation
* ready-made Terrier indices, where appropriate

#### Indexing
PyTerrier has a number of useful classes for creating Terrier indices, which can be used for retrieval, query expansion, etc. There are four indexer classes:

* You can create an index from TREC-formatted files, from a TREC test collection, using TRECCollectionIndexer.
* You can use FilesIndexer for indexing TXT, PDF, Microsoft Word files, etc.
* For indexing Pandas Dataframe you can use DFIndexer.
* For any **abitrary iterable dictionaries**, you can use IterDictIndexer.

#### Terrier Retrieval
**BatchRetrieve** is one of the most commonly used PyTerrier objects. It represents a retrieval transformation, in which queries are mapped to retrieved documents. BatchRetrieve uses a pre-existing Terrier index data structure, typically saved on disk.

#### Running Experiments
PyTerrier aims to make it easy to conduct an information retrieval **experiment**, namely, to run a transformer **pipeline** over a set of queries, and evaluating the outcome using standard information retrieval evaluation metrics based on known relevant documents (obtained from a set relevance assessments, also known as qrels).
The main way to achieve this is using `pt.Experiment()`.

## Near Duplicate Detection
<p align="center">
  <img src="https://user-images.githubusercontent.com/91251307/185661909-fb532b28-f014-4a05-a9a9-a24914f08464.png" style="width:800px">
</p>
