# A python wrapper for the Answer Constraint Engine

This package is a wrapper for [ACE](http://sweaglesw.org/linguistics/ace)

## Installation

```bash
pip install ACEngine
```

## Quick Start

### English Grammar Resource

```python
from ace.paraphrase import generate_paraphrase
text = "The quick brown fox that jumped over the lazy dog took a nap."
paraphrase_list = generate_paraphrase(text)
for paraphrase in paraphrase_list:
    print(paraphrase)
# The brown quick fox which jumped over the lazy dog took a nap.
# The brown quick fox that jumped over the lazy dog took a nap.
# A nap was taken by the brown quick fox which jumped over the lazy dog.
# The brown quick fox who jumped over the lazy dog took a nap.
# A nap was taken by the brown quick fox that jumped over the lazy dog.
# A nap was taken by the brown quick fox, which jumped over the lazy dog.
# A nap was taken by the quick brown fox, which jumped over the lazy dog.
# The brown quick fox, which jumped over the lazy dog, took a nap.
# The quick brown fox which jumped over the lazy dog took a nap.
# The quick brown fox, which jumped over the lazy dog, took a nap.
# A nap was taken by the brown quick fox who jumped over the lazy dog.
# A nap was taken by the brown quick fox, who jumped over the lazy dog.
# The quick brown fox that jumped over the lazy dog took a nap.
# A nap was taken by the quick brown fox, who jumped over the lazy dog.
# The brown quick fox, who jumped over the lazy dog, took a nap.
# The quick brown fox, who jumped over the lazy dog, took a nap.
# A nap was taken by the brown quick fox, that jumped over the lazy dog.
# A nap was taken by the quick brown fox, that jumped over the lazy dog.
# The brown quick fox, that jumped over the lazy dog, took a nap.
# The quick brown fox, that jumped over the lazy dog, took a nap.
# A nap was taken by the quick brown fox which jumped over the lazy dog.
# The quick brown fox who jumped over the lazy dog took a nap.
# A nap was taken by the quick brown fox that jumped over the lazy dog.
# A nap was taken by the quick brown fox who jumped over the lazy dog.
```

### The Jacy Japanese Grammar

```python
from ace.paraphrase import generate_paraphrase
text = "太郎 が 次郎 に 本 を 渡し た"
paraphrase_list = generate_paraphrase(text, grammar='jacy')
for paraphrase in paraphrase_list:
    print(paraphrase)
# 太郎 が 次郎 に 本 を 渡し た
# 次郎 に 太郎 が 本 を 渡し た
# 次郎 に 本 を 太郎 が 渡し た
```
