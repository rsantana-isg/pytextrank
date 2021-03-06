Python impl for TextRank
========================

Python implementation of *TextRank*, based on the 
`Mihalcea 2004 <http://web.eecs.umich.edu/~mihalcea/papers/mihalcea.emnlp04.pdf>`_
paper.

Modifications to the original Mihalcea algorithm include:

-  fixed bug; see `Java impl, 2008 <https://github.com/ceteri/textrank>`_
-  use of lemmatization instead of stemming
-  verbs included in the graph (but not in the resulting keyphrases)
-  normalized keyphrase ranks used in summarization

The results produced by this implementation are intended more for use
as *feature vectors* in machine learning, not as academic paper
summaries.

Inspired by `Williams 2016 <http://mike.place/2016/summarization/>`_
talk on *text summarization*.


Dependencies and Installation
-----------------------------

This code has dependencies on several other Python projects:

-  `TextBlob <http://textblob.readthedocs.io/>`_
-  `spaCy <https://spacy.io/docs/usage/>`_
-  `NetworkX <http://networkx.readthedocs.io/>`_
-  `datasketch <https://github.com/ekzhu/datasketch>`_
-  `graphviz <https://pypi.python.org/pypi/graphviz>`_

To install from `PyPi <https://pypi.python.org/pypi/pytextrank>`_:

::

    pip install pytextrank


To install from this Git repo:

::

    pip install -r requirements.txt

After installation you need to download a language model:

::

    python -m nltk.downloader punkt
    python -m nltk.downloader wordnet
    python -m textblob.download_corpora
    python -m spacy.en.download all

Also, the runtime depends on a local file called ``stop.txt`` which
contains a list of *stopwords*. You can override this in the
`normalize_key_phrases()` call.


Example Usage
-------------

See `PyTextRank wiki <https://github.com/ceteri/pytextrank/wiki/Examples>`_


Kudos
-----

`@htmartin <https://github.com/htmartin>`_
`@williamsmj <https://github.com/williamsmj/>`_
`@eugenep <https://github.com/eugenep/>`_
`@mattkohl <https://github.com/mattkohl>`_
`@vanita5 <https://github.com/vanita5>`_
`@HarshGrandeur <https://github.com/HarshGrandeur>`_
`@mnowotka <https://github.com/mnowotka>`_
