# Word Embeddings (Word2Vec) for Nepali Language

![Word Embeddings for Nepali Language](word_embd_cover.PNG?raw=true)

This pre-trained Word2Vec model has 300-dimensional vectors for more than 0.5 million Nepali words and phrases. A separate Nepali language text corpus was created using the news contents freely available in the public domain. The text corpus contained more than 90 million running words.

<h2>Word2Vec Model</h2>
<ul>
<li>Embeddings Dimension: 300</li>

<li>Architecture: Continuous - BOW</li>

<li>Training algorithm: Negative sampling = 15</li>

<li>Context (window) size: 10</li>

<li>Token minimum count: 2</li>
<li>Encoded in UTF-8</li>
</ul>

Download the model from IEEE Dataport: https://ieee-dataport.org/open-access/300-dimensional-word-embeddings-nepali-language

(Size: 1,881,180,827 bytes and File Type: .txt)

<h2>Using the Word2Vec model</h2>

```python
from gensim.models import KeyedVectors

# Load vectors
model = KeyedVectors.load_word2vec_format(''.../path/to/nepali_embeddings_word2vec.txt', binary=False)

# find similarity between words
model.similarity('फेसबूक','इन्स्टाग्राम')

#most similar words
model.most_similar('ठमेल')

#try some linear algebra maths with Nepali words
model.most_similar(positive=['', ''], negative=[''], topn=1)
```

The design of the Nepali text corpus and the training of the Word2Vec model was done at Database Systems and Artificial Intelligence Lab, School of Computer and System Sciences, Jawaharlal Nehru University, New Delhi.
