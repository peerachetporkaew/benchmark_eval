# Syllable-level BLEU Score

```
wget https://github.com/lstnlp/HoogBERTa/raw/refs/heads/syllacut_lib/hoogberta/syllacut-0.1.4-py3-none-any.whl
pip install syllacut-0.1.4-py3-none-any.whl
```

# Basic Usage :

```python
from syllacut import tokenize

ref = open("ref.tokenized.txt","r").read().splitlines()

submission = open("submission.txt","r").read().splitlines()
submission = [tokenize(line) for line in submission]

from sacrebleu import corpus_bleu
score = corpus_bleu(submission, [ref]).score

print("Score = ", score)
```
