

## 1. Title

Evaluation of the difference in usage across major social platforms

## 2.  Abstract

In the paper we are working on, a study is made on several aspects of the twitter platform: **Usage**, Information diffusion, structure of networks. For our extension we chose to focus on the question of usage, and to see if what we have been able to find in terms of results on twitter is similar to what can be seen on other social networks. To do this we will replicate figures 1A and 2 of our paper with data from other platforms. Our goal will be to see if our use of **social networks follows the same pattern regardless of the platform and to what extent**. To compare with the Twitter results, we will use data from **Stack Overflow, Weibo and Reddit**. These social networks which are very different from each other, either in their content or the codes of their user community will allow us to answer our question.

## 3. Research Questions

Do some of the *Twitter* usage patterns transpose to other social networks?

Does the nature of the platform and its mechanisms lead to different usage patterns ?

What is the percentage of questions that get answered in less than an hour on Stack Overflow at a given time of day and for each day of the week ?


## 4. Proposed dataset

-  The **“weibo_data”** dataset from Kaggle. This dataset lists a week's worth of posts on Weibo including the **user ID and post ID**, as well as some other information. This dataset will be used to get a figure of the CCDF of the number of posts by user. https://www.kaggle.com/sunxiaen/weibo-data?select=week1.csv 

-  The **“microblogPCU Data Set”** dataset from the Center for Machine Learning and Intelligent Systems of the University of California, Irvine. It contains data crawled from Sina Weibo microblog including the **time for each post, user ID and post ID**, as well as some other information. This dataset will be used to observe usage patterns of the platform. https://archive.ics.uci.edu/ml/datasets/microblogPCU# 

-  **“French Reddit Discussion”** dataset from Kaggle. This is a Reddit dataset focused on the french-speaking Reddit community containing more than **556,621 conversations with 1,583,083 comments in total.**. This dataset notably stores for each comment the **user ID**, the **comment ID**, the subreddit and more. This dataset will be used to observe usage patterns of the platform. https://www.kaggle.com/breandan/french-reddit-discussion 

-  “Reddit comments Data” dataset from the Pushshift API. This is a **BigQuery dataset** that contains Reddit comments, users, and more, for each year starting in 2005. This dataset will be used to get a figure of the CCDF of the number of posts by user on Reddit. https://www.reddit.com/r/pushshift/comments/bcxguf/new_to_pushshift_read_this_faq/ 

-  “Stack Overflow Data” dataset from Kaggle. This also is a **BigQuery dataset** that contains Stack Overflow content including posts, votes, tags, and badges. https://www.kaggle.com/stackoverflow/stackoverflow?select=comments
  

## 5. Methods

    

**Data collection :** 

Datasets from Weibo, Stack Overflow and Reddit posts are sourced from kaggle. The Weibo dataset is accessible from a .csv file while the BigQuery API will allow us to access the Stack Overflow and Reddit user data. Finally, the french corpus of Reddit comments is accessible as a .xml file from kaggle and converted to .csv using a provided python script.

**Pre-processing :**
 
**Sanity checks** and cleansing the datasets, then pre-processing by **randomly sampling the users** (rather than random sampling from posts in order to try to follow the sampling strategy of the original paper, if the dataset is large enough) then group posts by users.

This step also includes the **processing of the timestamps data** (formatting differs between datasets). 

As stated in the **Proposed dataset** section, different datasets will be used to obtain the replicated figures for Reddit and Weibo. On Reddit, the user's country is not available on its profile, which makes adjusting the timezones to take into account the user's location impossible. To address this, we will be using only the comments from the "/r/France" subreddit (from the “French Reddit Discussion”), and assuming that those who comment on it in french are located in France. Furthermore, the “weibo_data” dataset only contains one week of posts, which is not enough to have a representative view of the weekly usage patterns. To replicate figure 
2 for Weibo, we will be using the “microblogPCU Data Set”, that contains data spread across a longer period.

Since the milestone p4 also includes the replication of the Figure 2 of the 'Testing Propositions' paper as an individual task, we will be using 3 different methods (one per social network, and per member of the group) to generate our visualizations of the usage rhythms. Nevertheless, we will use the same method for all platforms for the replication of the figure 1A.

**Visualization :**
 
Using the number of posts by user, we can compute the **CCDF** to get a comparable figure to the 1A.

From there we will be able to compute the cumulative % of posts by cumulative % of users (figure 1B).

The timestamps will allow us to evaluate the number of posts at a given time in a day, and in a week. Using this data we can represent **the rhythms of usage** and compare them with the figures 2A and 2B.

  

## 6. Proposed timeline

    

**Week 1:** Pre-processing of the data and complementary research. By the end of week 1, the data should be sampled and formatted correctly.

**Week 2:** Realization of the plots in order to compare the results from twitter to ours from other social platforms. End of week 2, plots done and solid ideas for the data story and contents of presentation.

**Week 3:** Finalization of the data story and realization of the video.

  

## 7. Organization within the team


In week 1, each team member performed the aforementioned pre-processing steps on one of the 3 datasets. Charles David worked on Reddit dataset, Yassine on Stack Overflow and finally Kamyar worked on the Weibo dataset. Everyone also looked for additional datasets from other platforms to possibly add to the study.

In week 2, everyone has replicated the figures 1a, 2a and 2b of the social network that was assigned to him. All the computation and the main plots were done and the notebooks were also partly commented and cleaned. 

In week 3, everyone wrote a part of the datastory and created the plots and data needed to produce them: Yassine worked on the introduction, the extra "When to ask a question on Stack Overflow?" and the conclusion, Kamyar worked on the "Are you power users" part and Charles David worked on "User Behaviour" part. Then, Yassine mainly worked on the datastory and the layout of the website, while Charles David merged and cleaned all the notebooks. Kamyar helped Charles David with the notebooks.
