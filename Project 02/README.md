# Jigsaw Unintended Bias in Toxicity Classification
Project from the Kaggle competition: [Jigsaw unintended bias in toxicity classification](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification).

## Project Overview
Natural Language Processing is a complex field which is hypothesised to be part of AI-complete set of problems, implying that the difficulty of these computational problems is equivalent to that of solving the central artificial intelligence problem making computers as intelligent as people. With over 90% of data ever generated being produced in the last 2 years and with a great proportion being human generated unstructured text there is an ever increasing need to advance the field of Natural Language Processing.

However, as highlighted by the Kaggle competition ​Jigsaw unintended bias in toxicity classification​, existing models suffer from unintended bias where models might predict high likelihood of toxicity for content containing certain words (e.g. "gay") even when those comments were not actually toxic (such as "I am a gay woman"), leaving machine only classification models still sub-standard.

Having tools that are able to flag up toxic content without suffering from unintended bias is of paramount importance to preserve Internet's fairness and freedom of speech.

## Data Overview
Data can be downloaded from the Kaggle [page](https://www.kaggle.com/c/12500/download-all).

Data overview Attribute information:

- comment_text: text of individual comments
- target: toxicity label( to be predicted to for test data. target>=0.5 will be consider to be positive class(toxic))

Pretrained Models used can be downloaded from : 

``` 
pytorch-pretrained-BERT: https://www.kaggle.com/haqishen/pytorchpretrainedberthaqishen
Glove Pre-trained word vector: https://nlp.stanford.edu/data/glove.42B.300d.zip
```   

## Dependencies
```
torch
keras
sklearn
numpy
pandas
nltk
tqdm
pickle
scipy
```
## Executing Program

- The notebook was run on Kaggle with GPU on.
- Total Execution time was approximately 1.25 hours.

## Authors

Md Raisul Islam
[Linkedin](https://www.linkedin.com/in/raisul-islam89/) || [Kaggle](https://www.kaggle.com/raisulju)

## License

Copyright 2021, Md Raisul Islam.

This project is licensed under the Apache Version 2.0 License.

## Acknowledgments
The Project is created for the Upskill ISA IM Machine Learning Engineer Program.

