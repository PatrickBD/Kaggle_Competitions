# Kaggle_Competitions
A compilation of code and data from dozens of Kaggle competitions I participated in.

New and old code notebooks made for Kaggle competitions. My GitHub can get rather cluttered making a new repository to feature for each one and some smaller or older code samples need a good home without obscuring newer and larger projects. As of this writing, I have participated in close to 40 Kaggle competitions and have an overall Competitions Expert rank of 512 of 96,038. 

(My red-headed stepchild Indeed Machine Learning Competition is also in here, despite being hosted on HackerRank)

# Data_Science_Bowl_2018
Object Detection of cells for Data Science Bowl 2018 on Kaggle

The Kaggle Data Science Bowl 2018 was about automatically detecting and separating cells in slide images from under a microscope. One of the most complex and difficult object detection problem, up to dozen of visually similar cells need to be seperated in a pixel by pixel basis. The competition ended in April of 2018

### U-Net

A U-Net is a CNN model that maintains the benefits of max pooling while retaining pixel location for accurate object detection. In a normal CNN structure, max pooling is usually used to to make the model understand that important features are not location dependant while shrinking down the image. However, this removes the location information entirely which is not good for object detection. A U-Net starts by following a similar CNN structure with max pooling but then expands out similar to an auto encoder. The difference is that U-Nets retain information from between pooling layers and feed that information when expanding back out (Deconvolutional NN). This way, U-Nets gain feature detection advantages and independence while retaining the exact pixel locations for object detection.

U-Nets were the state of the art go to model for this type of object detection only a few years ago, dominating similar competitions easily. While still very useful and accurate, some other models like Mask RCNN can get better results nowadays. 

The Kaggle competition and related dataset can be found here: https://www.kaggle.com/c/data-science-bowl-2018

# Google_Analytics_Data_Analysis
Data visualization and analysis of Google Analytic data from the Gstore (EDA)

This is exploritory data analysis for the Google Analytics Customer Revenue Prediction Competion on Kaggle. The competition ended on November 30th 2018 and the results are evaluated on future data compiled between December 1st 2018 to January 31st 2019.

Competition Objective
"In this competition, you’re challenged to analyze a Google Merchandise Store (also known as GStore, where Google swag is sold) customer dataset to predict revenue per customer. Hopefully, the outcome will be more actionable operational changes and a better use of marketing budgets for those companies who choose to use data analysis on top of GA data."

The Kaggle competition and related dataset can be found here: https://www.kaggle.com/c/ga-customer-revenue-prediction

# Humpback_Whale_Identification_Challenge
Image Classification of whale tails to determine identify the whale it came from

The difficulty in this image classification challenge comes from having thousands of different whales to classify between, often with one image example of each. This is mitigated somewhat with the allowance of 5 predictions per test image. Another part of the challenge is dealing with whales that have not been seen yet, which unlike the other categories, has ~800 samples. This makes for an extreme local minimum that is very tricky to get out of. Recognising this is the first step to a decent predictive model.

I got to this challenge late and only had 2 days to work on and train it. Still made substantial improvements passed the baseline in that time and improved the model after the competition deadline.

The Kaggle competition and related dataset can be found here: https://www.kaggle.com/c/whale-categorization-playground

# Indeed_Job_Tagging
Machine learning algorithm made to determine job tags based on job posts. This was made for the Indeed Machine Learning CodeSprint on Hacker Rank. It got 29th place, which was enoungh to win the T-shirt prize. It gives job posts tags based off their raw descriptions by looking for keywords. Just exicuting the test.rb with the test/train files in the same folder will create a tags.tsv with the answers. It has an F1-Score of 0.685. The CodeSprint was only open for a short time so this code was created in a short window. The final code runs well but not as flexabile as ideal. The only package used was "csv".

### (Update)
I revisted the data for this CodeSprint to see how I would do with my new NLP skills. The revist uses Bidirrectional GRU and CNN layers to get the validation F1-Score to 0.7365, which would have put it in the top ten. That is far enough to satisify my curiosity.


# Kaggle_Toxic_Comment
My top bidirectional GRU model and Submissions that achieved a bronze medal in Kaggle Toxic Comment Challenge.

The notebook achived 0.9835 ROC in the competition, which is pretty much as high as a single model could go in the competition. Any scores higher than that are achived by ensembling methods. My subsquent ensemble model got to 0.9865 ROC, which was enough to reach a bronze medal and put me in the top 7%. (The highest model was 0.9885 for reference, with top ten being at 0.9875)

This model, in its many forms, was shared with many particpates at the Boston Kaggle study group. It was the insparational base for over 20 subsquent models from other members of the group. That is why the notebook has so many notes on how to use it, it was an introductry notebook to NLP neural networks for many people.

The Kaggle competition and related dataset can be found here: https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge

# Mercari_Price_Suggestion_Challenge_Challenge
A RNN, Ridge, and RidgeCV aggregate model for the Mercari Kaggle competition (RMSLE score of 0.427) 

The Mercari Price Suggestion Challenge is a $100,000 machine learning competition on Kaggle. The goal being to predict the sale price of items on Mercari. Mercari wants to have this prediction so that it can suggest to it's users what price new postings are likely to sell at. 

As an added complication, the challenge only allowed submissions using Kaggle kernals. This means that everyone's code is run on a simulated computer, about as powerful as a good desktop computer,  and has a time limit of 1 hour. No additional dataframes can be saved or brought in between runs.

My model is an aggregate a RNN and 2 Ridge models. It is kept in a jypiter notebook here or in the notebook kernal on Kaggle. It is probably best to view the Kaggle kernal, as all the test and train files are there and ready to explore. If using this GitHub, the test and train files will still need to be picked up on the challenge page. I did good in the compo, I was in the top 100 for a while. I decided that I had other projects to work on so I left it at this point. I published this notebook as a tutorial for others in the compo. As such it has many notes and ideas in the markdowns and comments. It is the best scoring public kernal of the compo as of this posting.


The Kaggle competition and related dataset can be found here: https://www.kaggle.com/c/mercari-price-suggestion-challenge

The original Kernal can be tried and run here: https://www.kaggle.com/valkling/mercari-rnn-2ridge-models-with-notes-0-42755


# Plant_Seedlings_Classification
My Notebook for Plant Seedlings Classification Image Processing Challenge on Kaggle

*Can you differentiate a weed from a crop seedling?*

*The ability to do so effectively can mean better crop yields and better stewardship of the environment.*

*The Aarhus University Signal Processing group, in collaboration with University of Southern Denmark, has recently released a dataset* *containing images of approximately 960 unique plants belonging to 12 species at several growth stages.*

I used this with some voting ensembling between model variations for my final score.

The Kaggle competition and related dataset can be found here: https://www.kaggle.com/c/plant-seedlings-classification
