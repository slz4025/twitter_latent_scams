# twitter_latent_scams

A pipeline to help identify and analyze topics of conversations around scams.

I recommend you save the tweet data in json format (one tweet per line) to Google Drive to use these notebooks. The notebooks will help label your data as being relevant to the scam conversation.

Run the notebooks in the following order, paying attention to the output of the code blocks.
1. `filterer` - This will filter your data to the core, English-speaking conversation.
2. `first_pass_scorer` - This is a first past scorer of your data which uses regex.
3. `tweet2tokens` - This will convert each tweet's body into a list of processed tokens.
4. `cluster_scorer` - This will allow you to perform TopSBM on different first-pass score thresholds. You should filter the data by a threshold on this score to get a good distribution of definitely/questionably scam-relevant data.
5. `cluster_analysis` - This will perform TopSBM and allow you to analyze your groups in more depth. It will perform a K-Means on each group to pick the ten or so most representative tweets of the group, which are, for each K-Means cluster, the tweet closest to its centroid.
