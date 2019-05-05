# TelegramNews

## About Data Set ##
Data set has news posts of popular news agencies in the world which we use in our paper <link> for SIGIR 2019. The data has two parts, the one form Telegram, an Instant messaging service and the other one from Twitter.

### Telegram ###
This set contains telegram news channels posts from their begining until October 8, 2017. 
The data is in mongodb dump format (bson) and you can easily restore it via `mongorestore` command and use it.

For each post we have:
* date: The post's publish time
* message: The post's text ( this could be empty )
* entities: Entities which you can use in telegram for a post like image, video, mentions, hashtags, and links ( this could be empty )
* channel: The post owner channel details

### Twitter ###

The Twitter data is in csv format files.


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
