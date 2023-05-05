## News Recommender

You have been recruited as data scientists by a start-up, JhakaasNewsVala, based out of Mumbai. The company is developing an app that promises to deliver a unique news experience to its app
users.

The company has identified it target market as working professionals. Recognising the fact that retention (defined here as a visit after the first visit) is a huge issue for apps, they understand the need to make an impact on the first visit itself. The problem however is that they know nothing about the user interests or demographics at the time to personalise the news feed to them.

### What to do ?

The task requires us to make a news article recommender that utilises a user profile (rating given by user or interests selected by user). But the company, *JhakaasNewsVala* hasn't provided any such data nor a texual news corpus.

1. So, using beautiful soup, selenium and python  data-wrangling techniques for web-scraping, a news articles corpus is generated with their categories and descriptions to create data dump. 

![web-scrapping](/figures/web-scrapping.png)

As shown in the above figure, a csv data dump namely `0_news_articles.csv` is generated after scrapping news articles from a famous Indian News website. The csv dump is as follows:

  | Data Dump              | Characteristic Fields or Columns                                         |
  |------------------------|--------------------------------------------------------------------------|
  | 0_news_articles.csv    | `Articles ID`, ` Title`, ` Description`, ` Date`, ` Category` and ` URL` |
  

1. In order to understand the imapct after first visit, variables like `User ID`, `Article Rank`, `Clickstream` etc need to be provided from the company but unfortunately, the scenario isn't like that so, these variables have been generated using random functional generators for populating the dataset.

- It also generates click-bait data based on articles rank and screen-time to further apply word embedding techniques such tf-idf, word2vec for performing collaborative news recommendation.
- Incorporated user defined ratings and ranking to further use LightRF and LightFM to explore hybrid and collaborative filtering based recommender models.

The flow of data is explained below: 

 ![Reference of data flow](/figures/flow_diagram.png) 

 ## Credits

 [Karanjot Vilkhu](https://github.com/karanjotsv)
