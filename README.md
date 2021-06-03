# Twitter_Analysis-Works-for-any-other-text-reallly-
A sentiment analysis using a BERT model

The following is a neural network model that is able to perform sentiment analysis on text.

This model uses the database from kaggle whicch collects tweets from the internet.
There were 1.6 million tweets in total, of which i chose just 40,000 randomly for training and testing of the model. 
Why this is so? Well hardware resources and the fact that this is kust a personal project, so no need to do so.
Feel free to put in more data if you want to use my code. More data always makes the model waork better ;)

Now, while it does say from the description and the database that it is for tweets from twitter, any other from of text works too actually. 
I did some data cleaning prior to training the model. Some things i did include
1) Removing all the hashtags, like #Ole'sAtThewheel and #Glazer'sOut
2) Removing all hyperlinks in the form of https://, http://, www. 
3) Removing all the username references like @Username_Blah1

I deemed all these 'words' as unnecesary and unlikely to affect the model. Hence, why i removed them
That being said, i do acknowldge the act that some usernames coukd perhaps be treated with negative/positive sentiments more often that not eh. JoelGlazer or DonaldTrump maybr
Hoeever, for the purposes of convenience, lets ignore this. Perhaps one thing we could do is to add a 'negative-weight' / 'positive-weight' to such usernames, but lets not get too deep into it.

The model gave an accuracy of around 0.75.
This could have been improved if i 
1) Trained with more epochs
2) Added more data
3) Played around with more hyperparameters

Even so, i think its a rather decent indicator, and after entering some 'tweets' of my own, it worked deently well. 

Some limitations include
1) Text entered cannot be more than 50 words long (This is to prevent the matrices from becoming too big which can present a problem when we're training the model)
2) Slangs might not be picked up and be treated as unknown words ([UNK]) and this can take away the meaning of some words. (A way to tackle this is to potentially introduce a vocab bank and include modern day and commonly used slangs there)
3) As mentioned, some usernames might be aligned with megative/positive connotations most of the time, so we can consider that too!

Feel free to download the relevant code and data and play around with it to achieve better results. Huge credit to https://towardsdatascience.com/text-classification-with-nlp-tf-idf-vs-word2vec-vs-bert-41ff868d1794 where i picked up knowldge on how to work with the BERT model.

