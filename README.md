# Word Embeddings (Word2Vec) for Nepali Language

![Word Embeddings for Nepali language](Word Embeddings for Nepali language.png?raw=true "Title")

This pre-trained Word2Vec model has 300-dimensional vectors for more than 0.5 million Nepali words and phrases. A separate Nepali language text corpus was created using the news contents freely available in the public domain. The text corpus contained more than 100 million running words.

<h2>Word2Vec Model</h2>
<ul>
<li>Embeddings Dimension: 300</li>

<li>Architecture: Continuous - BOW</li>

<li>Training algorithm: Negative sampling = 15</li>

<li>Context (window) size: 10</li>

<li>Token minimum count: 2</li>
<li>Encoded in UTF-8</li>
</ul>

Download the model from here: https://drive.google.com/file/d/1ik38vahOmzhiU2DBi78VOqDt7YFPsk5w/.

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

The desing of the Nepali text corpus and the training of the Word2Vec model was done in Lab-03, School of Computer and System Sciences, Jawaharlal Nehru University, New Delhi.
