# Natural Language Understanding benchmark

This file contains the results of the benchmark we ran on December 22nd 2016 to compare natural language understanding services offering built-in solutions (Apple’s SiriKit, Amazon’s Alexa, Microsoft’s Luis, Google’s API.ai, and Snips’ SDK) for the intents covered by the [Snips SDK](https://sdk.snips.ai/). This benchmark and its results are described in length in the [following post](
https://snips.ai/content/sdk-benchmark-visualisation/).

The data is structured by `domain`, and by `intent` within each `domain`. For each intent, aggregated statistics are contained in a `benchmark` dictionary containing the `f1`, `precision`, `recall`, and `classification accuracy` for each service, with corresponding uncertainty ranges (2 standard deviations). The same quantities are then given for each slot of each intent.

In addition to the `benchmark`, the list of `queries` is given for each `intent`. For each query, we provide the `classified_intent` returned by the classifier of each service, as well as the response given for each `slot`. For each of these responses, we provide its `value`. A `supervision` key contains either `TRUE`, `FALSE`, or `Not Applicable` if no response was given nor expected. The `expected_a_value` key corresponds to whether a response was expected for this slot. The later is used to compute the recall of the slot fillers, in particular.  

### Disclaimer
This benchmark has been run by Snips, which is one of the solutions benchmarked. To avoid biases in responses, this benchmark has been run in a blindfolded way, by a team independent from the data scientists working on the problem. The raw data is provided here to guarantee transparency.

This benchmark is based on 328 queries, over 10 intents. Collection and supervision of results remained partially manual.
