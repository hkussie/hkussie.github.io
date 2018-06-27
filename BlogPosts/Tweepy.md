## Looking at Tweets with the Tweepy Library

For this tutorial we're going to take a look at a very versatile library called Tweepy. Tweepy is a crucial tool for making use of Twitter's API, as it allows us to interact with it in a number of useful ways. For this example, we're going to be focusing on making use of the streaming services that Tweepy provides for us. So let's get started by importing the relevant libraries for this project:

```py
  import tweepy
  import sys    
  from tweepy.streaming import StreamListener
  from tweepy import OAuthHandler
  from tweepy import Stream
```
---
Now that we've imported the libraries needed to access and stream tweets from Twitter, we can begin the process of getting our tweets. The next thing we'll need in our script is our access credentials. To get your own credentials, you'll need to go to the Twitter Application Managment page and register from there. Once this is done, you'll recieve your credentials necessary to stream tweets. Embedded in the code, the necessary credentials should look something like this:

```py
access_token = "N/A"
access_token_secret = "N/A"
consumer_key = "N/A"
consumer_secret = "N/A"

auth = OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)
api = tweepy.API(auth)
```  
---
Now that we've got the necessary credentials, we can start our stream. Tweepy allows for us to filter for tweets in a number of different ways, lets take a look at some of them:

 ```py
class StreamListener(tweepy.StreamListener):

  def on_status(self, status):
    description = status.user.description
		text = status.text		
		loc = status.user.location
		text = status.text
		coords = status.coordinates
		name = status.user.screen_name
		user_created = status.user.created_at
		followers = status.user.created_at
		id_str = status.id_str
		created = status.created_at
		retweets = status.retweet_count
		print(description, text, loc, text, coords, name, user_created, followers, id_str, created, retweets)

	def on_error(self, status_code):
		if status_code == 420:
			return False

```
within the on_status function, there are several objects declared, each one of them set equal to a particular data point pertaining to the tweets that were streaming. While including several objects can provide us a lot of information regarding the tweets that we stream, this means a larger data set and more variables to account for. An alternative searching method, is to search by looking at hashtag values. The example below shows how we can go about this:

```py
stream_listener = StreamListener()
stream = tweepy.Stream(auth=api.auth, listener=stream_listener)

stream.filter(track=["world cup"])
```
Now that we have our tweets, let's take a look at how we might analyze the tweets that we just pulled. One library that we can make use of here is Vader sentiment. Using this library has a number of different applications within the field of linguistics and Machine Learning. However, for this particular example we're going to calculate the sentiment for each tweet that we stream.

Let's take a look at this library in practice, let's open a text file containing some of the tweets that we streamed. In the piece of code below, we're going to open the text file containing our tweets and iterate through each line to calculate the sentiment for each tweet:

```py
tweets = open("world_cup_data.txt", "r")
for tweet in tweets:
  print(tweet)
  sentiment = TextBlob(tweet)
  print("\n\t" + str(sentiment))
```
---
When this script is ran, you'll get a list of values ranging from -1 (a totally negative opinion) to 1 (a totally positive opinion). For further applications of any of the libraries used above, you should check out Twitter's documentation. 
