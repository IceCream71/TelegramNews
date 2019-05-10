# TelegramNews

## About the dataset ##
[Telegram](https://telegram.org) is a popular and fast growing instant messaging service. TelegramNews is a collection of news posts published by a set of popular news agencies through Telegram. This dataset also contains the tweets produced by the same news agencies in the same time period. 

TelegramNews is publicly available for research purposes. It has been used for news popualrity detection and analysis. It can potentially be used for various tasks, such as news summarization. 

### Telegram data format ###
This dataset contains telegram posts published by a set of news agencies from their starting date until October 8, 2017. 
The data is in mongodb dump format (bson) and you can easily restore it via the `mongorestore` command.

For each post we have:
* date: The post's publish time.
* message: The post's text (this can be empty).
* entities: Entities which you can use in Telegram for a post like image, video, mentions, hashtags, and links (this can be empty).
  * You can find out what could be in the message enity from [telegram schema definition(MessageEntity)](https://tjhorner.com/tl-schema/type/MessageEntity), and the Telegram's official [docs](https://core.telegram.org/schema).
* channel: The post owner channel details.
* views: Number of unique telegram users that have seen the post.

### Twitter data format ###
The Twitter data is in csv format. The data was collected from March 8, 2017 to October 8, 2017.

For each record we have:
* id: The tweet's id.
* created_at: The tweet's publish time
* text: The tweets's text
* favorites: The tweet's favorites number. 
* retweets: The tweet's retweet number.

## Citation
This dataset has been created by Mohammad Naseri and Hamed Zamani, for analyzing and predicting news popularity in instant messaging services. If you found this data useful, please refer to the following paper:

``` 
@inproceedings{Naseri:2019,
  title={Analyzing and Predicting News Popularity in an Instant Messaging Service},
  author={Naseri, Mohammad and Zamani, Hamed},
  booktitle={Proceedings of the 42nd ACM SIGIR International Conference on Research and Development in Information Retrieval},
  series={SIGIR '19},
  location={Paris, France},
  year={2019}
}
```
