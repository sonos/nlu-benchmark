# Natural Language Understanding benchmark

This repository contains the results of three benchmarks that compare natural language understanding services offering:
1. **built-in intents** (Apple’s SiriKit, Amazon’s Alexa, Microsoft’s Luis,
Google’s API.ai, and [Snips.ai](https://snips.ai/)) on a selection of
various intents. This benchmark was performed in December 2016. Its results
are described in length in the [following post](https://medium.com/snips-ai/benchmarking-natural-language-understanding-systems-d35be6ce568d).
2. **custom intent engines** (Google's API.ai, Facebook's Wit, Microsoft's Luis, Amazon's Alexa, and Snips' NLU) for seven chosen intents. This benchmark was performed in June 2017. Its results are described in a [paper](https://arxiv.org/abs/1805.10190) and a [blog post](https://medium.com/@alicecoucke/benchmarking-natural-language-understanding-systems-google-facebook-microsoft-and-snips-2b8ddcf9fb19).
3. **extension of Braun et al., 2017** (Google's API.AI, Microsoft's Luis, IBM's Watson, Rasa)
This experiment replicates the analysis made by Braun et al., 2017, published in Evaluating Natural Language Understanding Services for Conversational Question Answering Systems as part of SIGDIAL 2017 proceedings. Snips and Rasa are added. Details are available in a [paper](https://arxiv.org/abs/1805.10190) and a [blog post](https://medium.com/snips-ai/an-introduction-to-snips-nlu-the-open-source-library-behind-snips-embedded-voice-platform-b12b1a60a41a).

The data is provided for each benchmark and more details about the methods are available in the README file in each folder.

**Any publication based on these datasets must include a full citation to the following paper in which the results were published by the Snips Team<sup>1</sup>:** 

[Coucke A. et al., "Snips Voice Platform: an embedded Spoken Language Understanding system 
for private-by-design voice interfaces." 2018,](https://arxiv.org/abs/1805.10190)

accepted for a spotlight presentation at the [Privacy in Machine Learning and Artificial Intelligence workshop](https://pimlai.github.io/pimlai18/#papers) colocated with ICML 2018.



<sup>1</sup> *The Snips team has joined Sonos in November 2019. These open datasets remain available and their access is now managed by the Sonos Voice Experience Team. Please email sve-research@sonos.com with any question.*
