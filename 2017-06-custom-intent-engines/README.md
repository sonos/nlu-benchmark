# Natural Language Understanding benchmark

This file contains the results of the benchmark we ran on June 1st 2017 to compare natural language understanding services offering custom solutions (Wit, Luis, Api, and Snips) for seven intents. This benchmark and its results are described in [this blog post](https://medium.com/@alicecoucke/benchmarking-natural-language-understanding-systems-google-facebook-microsoft-and-snips-2b8ddcf9fb19).

## Method
We focused on seven `intents`:
* SearchCreativeWork (e.g. *Find me the I, Robot television show*),
* GetWeather (e.g. *Is it windy in Boston, MA right now?*),
* BookRestaurant (e.g. *I want to book a highly rated restaurant for me and my boyfriend tomorrow night*),
* PlayMusic (e.g. *Play the last track from Beyoncé off Spotify*),
* AddToPlaylist (e.g. *Add Diamonds to my roadtrip playlist*)
* RateBook (e.g. *Give 6 stars to Of Mice and Men*)
* SearchScreeningEvent (e.g. *Check the showtimes for Wonder Woman in Paris*)

More than 2000 queries have been generated for each intent with crowdsourcing methods. 10, 20, 50, 70, and around 2000 (depending on the intent) queries have been randomly selected several times to train the competitors. The training sets up to 70 queries are drawn among the `train_intent.json` files, and the ~2000 are provided by the `train_intent_full.json` files.

We focused here on slot filling (rather than intent classification), hence the benchmark was performed separately for each intent.

The results of the benchmark are displayed on the different `metrics` files, one per each intent and competitor. More specifically, the `precision` and `recall` are displayed for each `slot`.
Each value is displayed 3 times, corresponding to the number of random samples selected for each training size. 

## Specificities of each provider
In general, we gave each provider the benefit of the doubt. If anything, their performance is overestimated.

### API.ai
The following built-in entities were used:
`@sys.date-time`, `@sys.geo-city-us`, `@sys.geo-country`, `@sys.geo-state-us`, `@sys.music-artist`, `@sys.music-genre`.

The model cannot really be trained programmatically: each intent still needs to be manually saved on the web console (or through a curl command with an updated cookie).
The parsing giving back formatted values for the date-time and location built-in entities without span indices, we counted a prediction as correct if an entity of the same type was present in the original query (without checking for an absolute match).

### Wit.ai
The following built-in entities were used:
`wit$datetime`.

The model cannot really be trained programmatically: each entity needs to be manually set to 'free text' on the web console (or through a curl command with an updated cookie). The parsing giving back formatted values for the datetime built-in entity without span indices, we counted a prediction as correct if a datetime entity was also present in the original query (without checking for an absolute match).

### Luis.ai
The following built-in entities were used:
`datetimeV2`.

The model can be trained fully programmatically through the API reference.

### Alexa
There is not API reference available, we had to proceed manually.
The following built-in entities were used:
`AMAZON.TIME`, `AMAZON.DATE`, `AMAZON.US_CITY`, `AMAZON.Country`, `AMAZON.US_STATE`, `AMAZON.MusicGroup`, `AMAZON.Genre`, `AMAZON.MusicRecording`, `AMAZON.MusicRecording`, `AMAZON.MusicAlbum`, `AMAZON.MusicCreativeWorkType`, `AMAZON.MusicPlaylist`, `AMAZON.Book`, `AMAZON.CreativeWorkType`, `AMAZON.MovieTheater`, `AMAZON.Movie`.

The parsing giving back formatted values for the datetime built-in entity without span indices, we counted a prediction as correct if a datetime entity was also present in the original query (without checking for an absolute match). We also took into account that this provider maps digits to letters.

### Snips
The following built-in entities were used:
`snips/datetime`.



## Disclaimer
This benchmark has been run by Snips, which is one of the solutions benchmarked. To avoid biases in responses, this benchmark has been run in a blindfolded way, by a team independent from the data scientists working on the problem. The raw data is provided here to guarantee transparency.

