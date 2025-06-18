# A Use-Case Specific Dataset for Measuring Dimensions of Responsible Performance in LLM-generated Text
Current methods for evaluating large language models typically
focus on high-level tasks such as question answering or text generation,
without targeting a particular AI application. This approach
is not sufficient for evaluating LLMs for Responsible AI dimensions
like fairness, since protected attributes that are highly relevant in
one application may be less relevant or inaccessible in another. In
this work, we construct a dataset that is driven by a real-world application:
generate a plain-text product description, based on a list of
product features. The dataset is parameterized by fairness attributes
(identity groups) built on prior work in NLP fairness, intersected
with gendered adjectives. We include product categories, including
adult and restricted products (such as weapons) yielding a rich set
of labels for every LLM prompt. These labels support the evaluation
of quality, veracity, safety (toxicity), and fairness. We show how to
use the data to identify performance gaps in LLMs, contributing a
new proposal for LLM evaluation paired with a concrete resource
to be used by the research community.

## The Dataset 
The file `application-eval-data_2025-06.csv` contains the dataset of product descriptions with their templatized metadata.

### Sample Use
Using [`mlcroissant`](https://huggingface.co/docs/dataset-viewer/en/mlcroissant):
```
import mlcroissant as mlc

dataset = mlc.Dataset(jsonld="croissant.json")
records = dataset.records(record_set="csv")

print(next(iter(records)))
```

Using [TensorFlow datasets](https://www.tensorflow.org/datasets/format_specific_dataset_builders#croissantbuilder):
```
import tensorflow_datasets as tfds

builder = tfds.dataset_builders.CroissantBuilder(
    jsonld="croissant.json",
    file_format="array_record"
)
builder.download_and_prepare()

ds = builder.as_data_source()

print(ds["default"][0])
```

## The License
The data is published under the CC BY 4.0 license. Please cite this github repository when using the data.

## Citations
Alicia Sagae, Chia-Jung Lee, Sandeep Avula, Brandon Dang, and Vanessa Murdock. "A Use-Case Specific Dataset for Measuring Dimensions of Responsible Performance in LLM-generated Text". Github repository: https://github.com/amazon-science/application-eval-data. 2025.
