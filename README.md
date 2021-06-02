## Welcome
The repository provides the code for measuring societal biases and phenomena in text corpora as dicussed in the [paper](https://arxiv.org/abs/1812.10424):

**Measuring Societal Biases from Text Corpora with Smoothed First-Order Co-occurrence**
*Navid Rekabsaz, Robert West, James Henderson, Allan Hanbury
In proceedings of the AAAI Conference on Web and Social Media (ICWSM) 2021*

In this repository, you will find the implementation of the *smoothed first-order bias measurement* method as well as three high-order methods.

### Word Embeddings
All provided methods use word embeddings to measure bias in the underlying text corpus. The methods are suited for word2vec skip-gram (SG) and GloVe. You can use any pre-trained versions of these models so far that the model contains context vectors in addition to word vectors. If you train the models from scratch, please use [gensim](https://radimrehurek.com/gensim/) library for SG or the [standard tool of GloVe](https://nlp.stanford.edu/projects/glove/), and store the context-vectors after finishing the training.

To be able to reproduce the experiments, you can download our word embedding models, trained on an English Wikipedia text corpus. First download the compressed embeddings from:

SG: `https://drive.jku.at/filr/public-link/file-download/ff808082798b3a630179cd4ddabc0921/29517/8035538091838691595/sg.tar.gz`
GloVe: `https://drive.jku.at/filr/public-link/file-download/ff808082798b3a630179cd46d4c20919/29516/-84631503989242620/glove.tar.gz`

Execute the following step to decompress the files in the `word_embeddings` folder.
```
cd word_embeddings
```
Copy the files `sg.tar.gz` and `glove.tar.gz` to this folder and run:
```
tar xvzf sg.tar.gz
tar xvzf glove.tar.gz
```

### Bias Measurement
The notebooks `bias-measurement-SG.ipynb` and `bias-measurement-GloVe.ipynb` provide the implementation of bias measurement methods.  

### Contact
Feel free to contact [Navid](mailto:navid.rekabsaz@jku.at) if you have any question.

### Reference
```
@inproceedings{rekabsaz2021fairnessir,
    title={Measuring Societal Biases from Text Corpora with Smoothed First-OrderCo-occurrence},
    author={Rekabsaz, Navid and West, Robert and Henderson, James and Hanbury, Allan},
    booktitle={In proceedings of the International AAAI Conference on Web and Social Media (ICWSM'21)},
    year={2021},
    publisher = {{AAAI}}
}
```

