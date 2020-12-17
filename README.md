

## 1. Title

Evaluation of the difference in usage across major social platforms

## 2.  Abstract

In the paper we are working on, a study is made on several aspects of the twitter platform: **Usage**, Information diffusion, structure of networks. For our extension we chose to focus on the question of usage, and to see if what we have been able to find in terms of results on twitter is similar to what can be seen on other social networks. To do this we will replicate figures 1 and 2 of our paper with data from other platforms. Our goal will be to see if our use of **social networks follows the same pattern regardless of the platform and to what extent**. To compare twitter results, we will use data from the **StackOverFlow, Facebook and Reddit** platforms. These social networks which are very different from each other, either in their content or the codes of their user community will allow us to answer our question.

## 3. Research Questions

Do some of the *Twitter* usage patterns transpose to other social networks?

Does the nature of the platform and its mechanisms lead to different usage patterns ?

Does the usage of a *work-oriented* platform differ from those of more traditional social networks ?

## 4. Proposed dataset

-  The **“weibo_data”** dataset from Kaggle. This dataset lists a week's worth of posts on Weibo including the **user ID and post ID**, as well as some other information. This dataset will be used to get a figure of the CCDF of the number of posts by user. https://www.kaggle.com/sunxiaen/weibo-data?select=week1.csv 

-  The **“microblogPCU Data Set”** dataset from the Center for Machine Learning and Intelligent Systems of the University of California, Irvine. It contains data crawled from Sina Weibo microblog including the **time for each post, user ID and post ID**, as well as some other information. This dataset will be used to observe usage patterns of the platform. https://archive.ics.uci.edu/ml/datasets/microblogPCU# 

-  **“French Reddit Discussion”** dataset from Kaggle. This is a Reddit dataset focused on the french-speaking Reddit community containing more than **556,621 conversations with 1,583,083 comments in total.**. This dataset notably stores for each comment the **user ID**, the **comment ID**, the subreddit and more. This dataset will be used to observe usage patterns of the platform. https://www.kaggle.com/breandan/french-reddit-discussion 

-  “Reddit comments Data” dataset from the Pushshift API. This is a **BigQuery dataset** that contains Reddit comments, users, and more, for each year starting in 2005. This dataset will be used to get a figure of the CCDF of the number of posts by user on Reddit. https://www.reddit.com/r/pushshift/comments/bcxguf/new_to_pushshift_read_this_faq/ 

-  “Stack Overflow Data” dataset from Kaggle. This also is a **BigQuery dataset** that contains Stack Overflow content including posts, votes, tags, and badges. https://www.kaggle.com/stackoverflow/stackoverflow?select=comments
  

## 5. Methods

    

**Data collection :** 

Datasets from Weibo, Stackoverflow and Reddit posts are sourced from kaggle. The Weibo dataset is accessible from a .csv file while the BigQuery API will allow us to access the Stackoverflow and Reddit user data. Finally, the french corpus of Reddit comments is accessible as a .xml file from kaggle and converted to .csv using a provided python script.

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

    

In week 1, each team member will perform the aforementioned pre-processing steps on one of the 3 new datasets. Kamyar will then check that the formatting is in line with our original expectations and consistent across the datasets and perform the random sampling of the users. In the meantime, Yassine and Charles David will continue to look for datasets from other platforms to possibly add to the study.

In the beginning of week 2, Charles David will replicate the figure 1A for all the platforms studied, while Kamyar and Yassine will focus on the usage patterns (figures 2A and 2B). Whoever finishes first will do the replication of 1B while the others start brainstorming about the media used for the presentation of the results. By the end of week 2, all the computation and plots should be done.

To start week 3, Kamyar will work on the media to present the results, while Charles David and Yassine refine the data story. Once the data story is complete, the whole team will focus on finalizing the presentation.

## 8. Questions for TAs

    
Do you have any tips for searching for datasets? Are there any platforms for retrieving public datasets ?
