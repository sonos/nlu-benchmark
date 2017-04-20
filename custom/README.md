# Natural Language Understanding benchmark

This file contains the results of the benchmark we ran on March 16th 2017 to compare natural language understanding services offering custom solutions (a naive model based on regular expressions, Lastmile's RASA NLU with MITIE and SpaCy backends, Recast.ai, and Snips) for three intents. This benchmark and its results will be described in more details in a soon to be released blog post.

We focused on three types of `intents`:
* NavigateTracks with one `slot` (action) that is neither built-in nor gazetteer-based,
* GetWeather with two `slots` (location and timeRange) that are built-in like.

400 queries have been generated for each intent with crowdsourcing methods, 300 are for training and 100 for validation. The data is structured by `intent` in `training_set.json` and `validate_set.json`. 

The results of the benchmark are displayed on the different figures. More specifically, `execution_time` displays the total time elapsed in seconds to `fit` the model and the median `predict` time to parse one query (it does take into account the duration of API calls for API.AI and Recast.ai). `intent_classification` prodivides for each `intent` the classification `precision`. `token_classification` includes for each `intent` and for each `slot` the classification `precision` and `recall`. 
Each value is displayed 5 times, corresponding to the number of random samples selected for each training size. 

### Disclaimer
This benchmark has been run by Snips, which is one of the solutions benchmarked. To avoid biases in responses, this benchmark has been run in a blindfolded way, by a team independent from the data scientists working on the problem. The raw data is provided here to guarantee transparency.

