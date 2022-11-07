This project provides tokenizer library for Vietnamese language and 2 command line tools for tokenization and some simple Vietnamese-specific operations with text (i.e. remove diacritics). It is used in Cốc Cốc Search and Ads systems and the main goal in its development was to reach high performance while keeping the quality reasonable for search ranking needs.

Deployed by [trituenhantao.io](https://trituenhantao.io).

## Installing

```
pip install cython
pip install CocCocTokenizer
```

## Using Python bindings

```python
from CocCocTokenizer import PyTokenizer

# load_nontone_data is True by default
T = PyTokenizer(load_nontone_data=True)

# tokenize_option:
# 	0: TOKENIZE_NORMAL (default)
#	1: TOKENIZE_HOST
#	2: TOKENIZE_URL
print(T.word_tokenize("xin chào, tôi là người Việt Nam", tokenize_option=0))

# output: ['xin', 'chào', ',', 'tôi', 'là', 'người', 'Việt_Nam']
```
