# textClassifier

textClassifierHATT.py has the implementation of [Hierarchical Attention Networks for Document Classification](https://www.cs.cmu.edu/~diyiy/docs/naacl16.pdf). Please see [Keras Google group discussion](https://groups.google.com/forum/#!topic/keras-users/IWK9opMFavQ)

textClassifierConv has implemented [Convolutional Neural Networks for Sentence Classification](https://www.cs.cmu.edu/~diyiy/docs/naacl16.pdf).

textClassifierRNN has implemented bidirectional LSTM and one level attentional RNN.

## update on 6/22/2017 ##
To derive the attention weight which can be useful to identify important words for the classification. Please see my latest update on the post. All you need to do is run a forward pass right before attention layer output. The result is not very promising. I will update the post once I have further result.

---
We update the textClassifierHATT with `python 2.7` and `keras 2.0.8`

```
# clone the repo
git clone {repo address}

# install Dependent library
cd textClassifier
pip install -r req.xt

# download imdb train from Kaggle in the below link and keep the files in the working directory
https://www.kaggle.com/c/word2vec-nlp-tutorial/download/labeledTrainData.tsv
# download glove word vector
wget http://nlp.stanford.edu/data/glove.6B.zip
unzip glove.6B.zip

# install nltk 'punkt' using the following code in python interpretor
>>>import nltk
>>>nltk.download('punkt')

# train the model
python textClassifierHATT.py

# note if in case while installing word2vec, cython error occurs then 
pip install --upgrade cython
```



Enjoy！
