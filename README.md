NepaliKit
=========

[![Current Release Version](https://img.shields.io/github/release/explosion/nepalikit.svg?style=flat-square&logo=github)](https://github.com/explosion/nepalikit/releases)
[![pypi Version](https://img.shields.io/pypi/v/nepalikit.svg?style=flat-square&logo=pypi&logoColor=white)](https://pypi.org/project/NepaliKit/)
[![PyPi downloads](https://static.pepy.tech/personalized-badge/NepaliKit?period=total&units=international_system&left_color=grey&right_color=orange&left_text=pip%20downloads)](https://pypi.org/project/NepaliKit/)

NepaliKit is a Python library for natural language processing tasks in the Nepali language.

Installation
------------

You can install NepaliKit using pip:

    pip install nepalikit

Alternatively, you can clone the repository and install it manually:

    git clone https://github.com/prabhashj07/nepalikit.git
    cd nepalikit
    pip install .

Features
--------

NepaliKit provides the following features:

- **Tokenization**: Tokenize Nepali text using the SentencePiece tokenizer.
- **Preprocessing**: Clean and preprocess Nepali text data, including removing HTML tags, special characters, and other cleaning tasks.
- **Stopword Management**: Load, add, and remove stopwords from Nepali text.
- **Sentence Operations**: Segment Nepali text into sentences based on punctuation marks.
- **SentencePiece Model Training**: Train custom SentencePiece models for Nepali text data.
- **Utility Functions**: Various utility functions for text processing and manipulation.
- **Integration with PyTorch**: Utilities for integrating with PyTorch for machine learning tasks.

Usage
-----

### Tokenization Example

```python
from nepalikit.tokenization import SentencePieceTokenizer

text = "नमस्ते, के छ खबर?"
tokenizer = SentencePieceTokenizer()
tokens = tokenizer.tokenize(text)
print(tokens)
```

## Preprocessing Example
-----

```python
from nepalikit.preprocessing import TextProcessor

text = "<p>नमस्ते, के छ खबर?</p>"
processor = TextProcessor()
clean_text = processor.remove_html_tags(text)
clean_text = processor.remove_special_characters(clean_text)
print(clean_text)
```
### Stopword Example 
-----
```python
from nepalikit.manage_stopwords import load_stopwords, remove_stopword

stopwords = load_stopwords('/path/to/stopword/directory')
remove_stopword('कुनै_स्टापवर्ड')
```

License
-----
This project is licensed under the MIT License.

Author
-----
- Prabhash Kumar Jha
- Email: prabhashj07@gmail.com
