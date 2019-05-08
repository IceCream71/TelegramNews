# TelegramNews

## About Data Set ##
Data set has news posts of popular news agencies in the world which we use in our paper <link> for SIGIR 2019. The data has two parts, the one form Telegram, an Instant messaging service and the other one from Twitter.

### Telegram ###
This set contains telegram news channels posts from their begining until October 8, 2017. 
The data is in mongodb dump format (bson) and you can easily restore it via `mongorestore` command and use it.

For each post we have:
* date: The post's publish time.
* message: The post's text ( this could be empty ).
* entities: Entities which you can use in telegram for a post like image, video, mentions, hashtags, and links ( this could be empty ).
  * You can find out what could be in the message enity from [telegram schema definition(MessageEntity)](https://tjhorner.com/tl-schema/type/MessageEntity), and telegram's official [docs](https://core.telegram.org/schema).
* channel: The post owner channel details.
* views: Number of unique telegram users whom sees the post.

### Twitter ###

The Twitter data is in csv format files for each news agancy from March 8, 2017 to October 8, 2017.

For each record we have:
* id: The tweet's id.
* created_at: The tweet's publish time
* text: The tweets's text
* favorites: The tweet's favorites number. 
* retweets: The tweet's retweet number.

## References
If you use our dataset or code, please cite our paper:

``` 
@inproceedings{newspop:2019,
  title={Analyzing and Predicting News Popularity in an Instant Messaging Service},
  author={Naseri M., Zamani H.},
  booktitle={SIGIR},
  location={Paris, France},
  year={2019}
}
```
