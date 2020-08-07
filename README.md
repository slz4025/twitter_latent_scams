# twitter_latent_scams

Identifying and analyzing conversations around scams with the goal of finding latent scam instances.

I recommend you save the tweet data in json format (one tweet per line) to Google Drive to use these notebooks. The notebooks will help label your data as being relevant to the scam conversation.
Run the notebooks in the following order, paying attention to the output of the code blocks.
1. filterer -- This will filter your data to the core, English-speaking conversation.
2. scorer -- This is a first past scorer of your data which uses regex.
3. semi-supervised classifier -- This will label your filtered tweets. It uses the top results from the scorer to approximate the scam-relevant class.

[TODO] The output will be a TSV with the tweet and the label.
