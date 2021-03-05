# doccano-transformer

Doccano Transformer helps you to transform an exported dataset into the format of your favorite machine learning library.
* 修复了中文标注转化时位置前移的问题
* 修改了conll02的输出格式，更好的适应各模型的输入要求

## Supported formats

Doccano Transformer supports the following formats:

* CoNLL 2003
* spaCy

## Install

To install `doccano-transformer`, simply use `pip`:

```bash
pip install doccano-transformer
```

## Examples

### Named Entity Recognition

The following formats are supported:

- CoNLL 2003
- spaCy

```python
from doccano_transformer.datasets import NERDataset
from doccano_transformer.utils import read_jsonl

dataset = read_jsonl(filepath='example.jsonl', dataset=NERDataset, encoding='utf-8')
dataset.to_conll2003(tokenizer=str.split)
dataset.to_spacy(tokenizer=str.split)
```

## License

[MIT](https://github.com/doccano/doccano-transformer/blob/master/LICENSE)
