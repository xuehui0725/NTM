#NTM + Doc2vec (version 0.2 alpha)
Requirements:
Version: Python 2.7+
The program requires some of the python packages including gensim, numpy, scipy, pickle and so on. If your python distribution misses any package it will produce an error called "No module found named ... (Module name)"

doc2vec_TopicVector_NonDet.py: I used the code to generate the results. Here you will find a method named "Train" that is NTM part in addition to doc2vec. I also included an evaluation metric for classification and saving only the topic vectors.

word2vec.py: I changed a little bit in the file to initialize some values such as ntopics (# of Topics) and so on.

# NTM (version 0.1 alpha)
Neural Network Topic Modeling

Requirements:
Version: Python 2.7+
The program requires some of the python packages including gensim, numpy, scipy, pickle and so on. If your python distribution misses any package it will produce an error called "No module found named ... (Module name)"

Steps to run the code:

1) Process the data as you do for giving input to word2vec or doc2vec or you may use the preprocessData.py if it fits on your datasets.
2) Open the file doc2vec.py. Change the line of the "__main__" function as follow:
  sentences = LabeledLineSentence(file_path)
  
  for my case: 
  sentences = LabeledLineSentence('./ntm_3group_news.txt').
  
  The data file is in the same directory the doc2vec.py exists.
3) To save the model of word2vec and doc2vec for further use, you can use the doc2vec python implementation. However, to save the P(ngram|topic) and P(topic|document) distribution, you can dump the variable value (w_lt, w_ld). You will find sample a code in the saveData.py to do so.
