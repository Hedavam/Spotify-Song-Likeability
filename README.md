# Can Audio Features Alone Predict Song Enjoyment?

## Abstract & Presentation
* Abstract: [https://docs.google.com/document/d/1lSZIfg9X1pzv59c_jzuF31h75lCVtbhayJeIXI2fy1A/edit?usp=sharing*](https://docs.google.com/document/d/1lSZIfg9X1pzv59c_jzuF31h75lCVtbhayJeIXI2fy1A/edit?usp=sharing)
* Presentation: [https://docs.google.com/presentation/d/1_-r23gsWpp7A-4_4wjIkOdc4CBSZh9ksumJCPx1pAXs/edit#slide=id.g1ac087ac278_0_0](https://docs.google.com/presentation/d/1_-r23gsWpp7A-4_4wjIkOdc4CBSZh9ksumJCPx1pAXs/edit?usp=sharing)

## Instructions
The primary solution code is in solution.py. To run, type `python solution.py -n 100` in the console. `-n` indicates how large the sample (test) group should be. To us search functionality add `-s "Song Name"`. This will only search from among the existing data due to the recent API changes that limit our access to Spotify data. The code for the audio feature fetch and old search functionality (pre API change) remains in the code but is no longer called. `-t` indicates how many tests to run so `-t 10` for example will run 10 tests and output the average of the metrics across the tests.

Running the code will not work without out Spotify secrets which are not included in this repository. To bypass the Spotify integration comment out Step 2 and Step 4 in the solution and add the following lines after Step 4:

`tests = int(args.tests)`

`test_song = tracks.loc[tracks["track_id"] == None]`

This will disable the search functionality but will not functionally alter anything else because, after the API changes, we are no longer pulling Spotify data and are, instead, pulling from our previously pulled data in tracks.json
