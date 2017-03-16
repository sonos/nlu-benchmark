# Natural Language Understanding benchmark

This file contains the results of the benchmark we ran on March 16th 2017 to compare natural language understanding services offering custom solutions (a naive model based on regular expressions, Lastmile's RASA NLU, Recast.ai, and Snips' Pcfg parser) for three intents. This benchmark and its results will be described in more details in a soon to be released blog post.

We focused on three types of `intents`:
* NavigateTracks with one `slot` that is neither built-in nor gazetteer-based,
* GetWeather with two `slots` that are built-in,
* PlayMusic with nine `slots` among which two are gazetteer-based.

400 queries have been generated for each intent with crowdsourcing methods, 300 are for training and 100 for validation.

The data is structured by `intent` in `training_set.json` and `validate_set.json`. 

The results of the benchmark are structured by `type` (execution time, intent classification precision, and token classification precision and recall), then by `training size` (number of queries selected from the training set, from `n=5` to `n=50`), and finally by `model`.

Each value is displayed 5 times, corresponding to the number of random samples selected for each training size. 

### Disclaimer
This benchmark has been run by Snips, which is one of the solutions benchmarked. To avoid biases in responses, this benchmark has been run in a blindfolded way, by a team independent from the data scientists working on the problem. The raw data is provided here to guarantee transparency.

