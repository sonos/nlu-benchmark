# Natural Language Understanding benchmark

This file contains the results of the benchmark we ran on June 1st 2017 to compare natural language understanding services offering custom solutions (Wit, Luis, Api, and Snips) for seven intents. This benchmark and its results will be described in more details in a soon to be released blog post.

We focused on seven `intents`:
* SearchCreativeWork (e.g. Find me the House of Cards television show),
* GetWeather (e.g. Is it windy in Boston, MA right now?),
* BookRestaurant (e.g. I want to book a highly rated restaurant for me and my boyfriend tomorrow night)
* PlayMusic (e.g. Play the last track from Beyoncé off Spotify)
* AddToPlaylist (e.g. Add Diamonds to my roadtrip playlist)
* RateBook (e.g. Give 6 stars to Of Mice and Men)
* SearchScreeningEvent (e.g. Check the showtimes for I, Daniel Blake in Paris)

More than 2000 queries have been generated for each intent with crowdsourcing methods. 10, 20, 50, 70, and 2000 queries have been randomly selected 3 times to train the competitors. 

The results of the benchmark are displayed on the different `metrics` files, one per each intent and competitor. More specifically, the `precision` and `recall` are displayed for each `slot`.
Each value is displayed 3 times, corresponding to the number of random samples selected for each training size. 

### Disclaimer
This benchmark has been run by Snips, which is one of the solutions benchmarked. To avoid biases in responses, this benchmark has been run in a blindfolded way, by a team independent from the data scientists working on the problem. The raw data is provided here to guarantee transparency.

