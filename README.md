# RAI Assessment of LLMs with Granular Application Data
Current methods for evaluating large language models often fail to answer the central question of end-users: *how well will it work for **my** application?* 

This mismatch occurs because LLM benchmarks often focus on high-level tasks such as question answering or text generation, without targeting a practical application. The gap is even wider when evaluating LLMs for Responsible AI dimensions like fairness, since protected attributes that are highly relevant in one application may be less relevant or inaccessible in another. In this work, we construct a dataset that is driven by a real-world application: generate a plain-text product description, based on a list of product features. The dataset is parameterized by granular fairness attributes of race, gender, and age, and supports the evaluation of fairness, quality, safety, and veracity. We demonstrate the utility of this dataset for identifying performance gaps in LLMs, contributing a new proposal for LLM evaluation paired with a concrete resource to be used by the research community.


## The Dataset 
The file `application-eval-data_2025-02.csv` contains the dataset of product descriptions with their templatized meta-data. 

## The License
The data is published under the CC BY 4.0 license. Please cite this github repository when using the data.

## Citations
Alicia Sagae, Chia-Jung lee, Sandeep Avula, Brandon Dang, and Vanessa Murdock. "RAI Assessment of LLMs with Granular Application Data". Github repository: https://github.com/amazon-science/application-eval-data. 2025.
