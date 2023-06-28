## **Content Based Systems** 

### **Intuition**

Content based systems generate recommendations based on the users preferences and profile. They try to match users to items which they’ve liked previously. The level of similarity between items is generally established based on attributes of items liked by the user. Unlike most collaborative filtering models which leverage ratings between target user and other users, content based models focus on the ratings provided by the target user themselves. In essence, the content based approach leverages different sources of data to generate recommendations.

The simplest forms of content based systems require the following sources of data (these requirements can increase based on the complexity of the system you’re trying to build):

1.  Item level data source — you need a strong source of data associated to the attributes of the item. For our scenario, we have things like book price, num\_pages, published\_year, etc. The more information you know regarding the item, the more beneficial it will be for your system.
2.  User level data source — you need some sort of user feedback based on the item you’re providing recommendations for. This level of feedback can be either implicit or explicit. In our sample data, we’re working with user ratings of books they’ve read. The more user feedback you can track, the more beneficial it will be for your system.

### **Implementation**

1.  Import data from generate\_data function (function provided above) or download the CSV from [here](https://github.com/vatsal220/medium_articles/blob/main/rec_sys/data/data.csv)
2.  Normalize book\_price, book\_ratings, num\_pages
3.  One hot encode publish\_year, book\_genre, text\_lang
4.  Given a book\_id input, calculate the [cosine similarity](https://pyshark.com/cosine-similarity-explained-using-python/) and return top n books similar to the input
5.  code is in main.py

©️ [vatsal220](https://gist.github.com/vatsal220) 