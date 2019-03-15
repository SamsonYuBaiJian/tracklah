# Traclories
Calorie estimation with Keras, Gensim, NLTK and pandas (VGG-16 failed).
Automating calorie tracking by integrating DBS PayLah! and Healthy 365.
Collected nutritional data from Allrecipes with BeautifulSoup.

## Steps:
1. Scrape food information from https://www.allrecipes.com/recipes/. (./calorie-estimation/scraper.py)
    - Information is saved. (./calorie-estimation/info.csv)
2. Apply natural language processing with Gensim and NLTK to find the five nearest word vectors. (./calorie-estimation/nlp_test.py)
3. Use Keras dense layers and ReLU activations to train neural network to apply the appropriate weights to the five vectors for each datapoint. (./calorie-estimation/weight_net.py)
    - Model and model history are saved. (./calorie-estimation/model.h5 and ./calorie-estimation/history)
4. Allow users to predict calories in new food items. (./calorie-estimation/final.py)

Note: The computer vision test with VGG-16 failed because the approximate nearest neighbour algorithm used to build the tree structure for existing datapoints could not be updated incrementally to estimate the calories in new food items. (./calorie-estimation/cv_unused)
