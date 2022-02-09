# 🪐 [WIP] spacy-span-analyzer

A simple tool to analyze the [Spans](https://spacy.io/api/span) in your
dataset. It's tightly integrated with
[spaCy](https://github.com/explosion/spaCy), so you can easily incorporate it
to existing NLP pipelines. This is also a reproduction of Papay, et al's work on [*Dissecting Span
Identification Tasks with Performance
Prediction*](https://aclanthology.org/2020.emnlp-main.396.pdf) (EMNLP 2020).


## ⏯ Usage

You can use the Span Analyzer both as a command-line tool and library:

```sh
spacy-span-analyzer ./path/to/dataset.spacy
```

```python
from spacy_span_analyzer import SpanAnalyzer
from spacy.tokens import DocBin

# Ensure that your dataset is a DocBin
my_dataset = DocBin().from_disk("./path/to/data.spacy")
analyze = SpanAnalyzer(my_dataset)
analyze.frequency
analyze.span_distinctiveness
analyze.all
```
