In January 2018, we ran an additional series of experiments to  evaluate our Natural Language Understanding (NLU) solution.

These experiments replicate the analysis made by Braun et al., 2017, published in _Evaluating Natural Language Understanding Services for Conversational Question Answering Systems_ as part of SIGDIAL 2017 proceedings ([pdf](http://workshop.colips.org/wochat/@sigdial2017/documents/SIGDIAL22.pdf)). This article proposes a comparison of 4 NLU services:

- Luis.ai
- Watson
- API.ai
- Rasa

We reproduced the analysis with the same methodology, on the [same datasets](https://github.com/sebischair/NLU-Evaluation-Corpora), for both Snips NLU library and Rasa, in their January 2018 versions. For Rasa, we considered all three possible backends (Spacy, SKLearn + MITIE, MITIE). However, only Spacy was run on all 3 datasets, for train time reasons.

The exact same splits as in the original article were used for the _Ubuntu_ and _Web Applications_ corpuses. A training flag is also present in the _Chatbot_ [dataset](https://github.com/sebischair/NLU-Evaluation-Corpora) but it was added after we ran the benchmark. Hence, back then, the train/test split was not explicit for this dataset: in that case, we ran a 5-fold cross-validation.

Raw metrics by intent and slot can be found in the `/results` folder. Below, you will find the results obtained, for each dataset. Note that _None_ intents were ignored when computing the metrics, as in the original article.


Chatbots
========

| NLU Engine              | Precision | Recall | F-score |
| ----------------------- | --------- | ------ | ------- |
| Snips                   | 95%       | 89%    | 92%     |
| Rasa (Spacy)            | 93%       | 92%    | 93%     |

Web applications
================

| NLU Engine              | Precision | Recall | F-score |
| ----------------------- | --------- | ------ | ------- |
| Snips                   | 65%       | 65%    | 65%     |
| Rasa (Spacy)            | 59%       | 61%    | 60%     |
| Rasa (SKLearn + MITIE) | 49%       | 74%    | 59%     |
| Rasa (MITIE)           | 51%       | 76%    | 61%     |

Ubuntu
======

| NLU Engine              | Precision | Recall | F-score |
| ----------------------- | --------- | ------ | ------- |
| Snips                   | 81%       | 82%    | 82%     |
| Rasa (Spacy)            | 80%       | 77%    | 78%     |
| Rasa (SKLearn + MITIE) | 82%       | 83%    | 83%     |
| Rasa (MITIE)           | 83%       | 84%    | 84%     |

Total
======

| NLU Engine              | Precision | Recall | F-score |
| ----------------------- | --------- | ------ | ------- |
| Snips                   | 89%       | 85%    | 87%     |
| Rasa (Spacy)            | 87%       | 85%    | 86%     |
