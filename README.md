# Mini Project - Sentimental Analysis on Covid-19 Tweets
Defina Ambarwati : [Github](https://github.com/definaa2412)
***

## About

Sentiment analysis is scanning of words written or said by a person to recognize or determine their emotion (most likely feeling) that time. So in this project, we are going to use python for applying sentiment analysis on the people's tweets in certain period. We will use the pre-trained model for sentiment analysis, **VADER** (Valence Aware Dictionary for Sentiment Reasoning). **VADER** is a rule-based sentiment analysis tool that is specifically applied to sentiments expressed in social media.

## Dataset
Dataset used is consisting of data related to the tweets from 24th of July 2020 to the 30th of August 2020 with covid19 hashtags and obtained from Coursera. This data consists of 179108 tweets and 13 related features such as 

<div align="center">

<table>
<tr>
  <td align="center"> user_name </td>
</tr>
<tr>
  <td align="center"> user_location </td>
</tr>
<tr>
  <td align="center"> user_description </td>
</tr>
<tr>
  <td align="center"> user_created </td>
</tr>
<tr>
  <td align="center"> user_followers </td>
</tr>
<tr>
  <td align="center"> user_friends </td>
</tr>
  <td align="center"> user_favourites </td>
</tr>
<tr>
  <td align="center"> user_verified </td>
</tr>
<tr>
  <td align="center"> date </td>
</tr>
<tr>
  <td align="center"> text </td>
</tr>
<tr>
  <td align="center"> hashtags </td>
</tr>
<tr>
  <td align="center"> source </td>
</tr>
<tr>
  <td align="center"> is_retweet </td>
</tr>
</table>

</div>

## Goal
  To understand and analyze several public opinions about Covid-19 in certain period so the goverment or related organizations can make wise decisions about it.

## Summary
### Data Preprocessing
1. Take only the needed columns (**user_name**, **date** and **text**)
2. Remove URL from tweets.
3. Convert all tweets to lowercase text.
4. Removing punctuations and stop words.

### Sentiment Analysis
1. Get the polarity scores from all tweets using **VADER Sentiment Analysis** pre-trained model.

<div align="center">
  
  ![Polarity](https://github.com/definaa2412/Sentimental-Analysis-on-Covid-19-Tweets/blob/main/images/Polarity%20Score.png)

</div>

2. Labels the score based on its polarity score according to the following compound value criteria.
   
<div align="center">

| Compound Value                    | Label                                                           |   
| -----------------------------   |:---------------------------------------------------------------------:|
| 0                           | Neutral                          |
| > 0                    | Positive           |
| < 0                       | Negative |
  
</div>

3. Plot the sentiment label count

<div align="center">
  
![daily plot](https://github.com/definaa2412/Sentimental-Analysis-on-Covid-19-Tweets/blob/main/images/daily%20plot%20sentiment.png)
  
</div>
  

<p align="justify">  
&nbsp;&nbsp;&nbsp;&nbsp; As we can see, in early July, Covid cases in several countries began to decrease as indicated by the Harvard Institute's plan to reopen schools or bars, while in Arkansan, which was marked by hospitalization rates having gone down.
  
&nbsp;&nbsp;&nbsp;&nbsp; Although in mid July, the cases gone up again indicating by the higher amount of tweet. In that time, discussion about vaccine has started by US Centers for Disease Control and Prevention, so we can conclude that the positive tweets mostly hope of vaccine success.
</p>
  
4. Test Tweet
  
<div align="center">
   
   ![test](https://github.com/definaa2412/Sentimental-Analysis-on-Covid-19-Tweets/blob/main/images/test%20sentiment.png)
  
</div>
  
  &nbsp;&nbsp;&nbsp;&nbsp; As we can see, the VADER model predict the example tweet correctly, which is **negative**
  
## Conclusion

**VADER** pre-trained model is good at recognizing someone's feeling on Covid-19 tweet data. For further learning, it is hoped that we also use other approaches in recognizing someone's feelings through tweet data. Thank you.

