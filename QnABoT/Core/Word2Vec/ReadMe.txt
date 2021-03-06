
Yapı Kredi QnA BoT version 0.2

Defintion:
This program is a Question&Answer bot which brings the top 5 best match among a predefined set of questions based on semantic search.

Methodology:
Vector space models (VSMs) represent (embed) words in a continuous vector space where semantically similar words are mapped to nearby points

Word2vec is a particularly computationally-efficient predictive model for learning word embeddings from raw text.
It was created and published in 2013 by a team of researchers led by Tomas Mikolov at Google. ref: https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf

Pre-trained model is loaded: "word2vec.model"
Each word represented as a vector in a 200 dimensional hyperspace.

Corpus details: 
Combination of financial news retrieved from bloomberght.com and FAQs from yapıkredi.com
20000 news paragraphs consist of 433000 words in total
Processed with TurkishNlpPipeLine
Source code available under the directory: /ProjectNotebooks/DataCollection.ipynb
Language: Turkish
Encoding: UTF-8


If you would like to train the model with a different domain run 
"builmodel.py" provide a text file ("docs_processed.txt") which includes list of ,lists of processed tokens separated by blank space, separated by newline character. 

ex:
docs_processed.txt
a b
c d
e f

[['a','b'],['c','d'],['e','f']]


Visualize the embeddings:
[Embedding Projector](http://projector.tensorflow.org), 
Upload tsv Files(created with model) a file of vectors, and a file of meta data available under the directory:
 ./tsvFiles/vecs.tsv
 ./tsvFiles/meta.tsv


Retrieve similarity scores for ranking:
Cosine similarity is a metric used to determine how similar the documents are irrespective of their size.
Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space.
The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance because of the size
they could still have a smaller angle between them. Smaller the angle, higher the similarity.




