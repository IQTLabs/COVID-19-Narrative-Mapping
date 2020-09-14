## Welcome to our COVID-19 Narrative & Claim-Mapping Visualization!

IQT Labs created this narrative & claim-mapping tool to track the spread of mis/dis-information about COVID-19 over time: information epidemiology. We wanted to map tweets relating to specific claims or narratives in geographic and political space, as well as time. This enables us to visualize the lifecycle of a claim or narrative: when and where did a false narrative originate, how did it propagate, and is it still active? We are also interested in seeing which narratives or claims become politicized over time. The current prototype displays 563 tweets from March-May 2020, containing 59 unique URL links about Cures, Prevention, or Origins, many of which are misleading. Where available, we include metadata on source bias for each URL, with news source domain bias derived from the [NELA-GT-2019 Dataset](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/O7FWPO). Future versions will integrate with our automated claim-matching API, which identifies close semantic matches from Tweets to previously fact-checked claims. Read further to see how we made the dataset as well as how you can use this open source visualization with your own data! Any direct questions about the visualization can be directed to [@Katelyn98](https://github.com/katelyn98) or [@ninalopatina](https://github.com/ninalopatina).

First, a few definitions: 
- **Topic** ~ A broad category that includes several distinct narratives
  - Examples of topics include Cures, Preventions, and Origins.
- **Narrative** ~ A more specific category, grouping several claims within a given topic
  - Examples of common misinformation narratives about Cures include treatment with natural oils/herbs, whiskey mixed with honey, or disinfectants. 
 - **Claim** ~ A subjective generalized statement being made in an objective context 
    - An example of a claim within one of the above narratives is: _"Hot whiskey mixed with honey cures Coronavirus"_

### Dataset

The current prototype visualizes a manually curated dataset. Any tweet/URL talking about the narrative that was deemed relevant was added to the dataset. This dataset consisted of 563 tweets that were manually labeled from March, April, and May 2020. The source Twitter data was hydrated from the [COVID-19 Twitter Dataset](https://github.com/echen102/COVID-19-TweetIDs). 

***Filtering***

We started with 92,783,762 tweets from March, April, and May 2020. We applied filters to narrow down to tweets that were in English, were tagged with a location, and shared a URL. In some cases, the URL that was shared was to another tweet - this is how Twitter's API represents retweeted tweets. After applying filters, we had 263,346 tweets. We grouped all of these tweets by a common URL. Then for every URL, we printed out the URL and the text of the tweet that referenced that URL. We then performed keyword search on the text of the tweets by URL - keywords used terms commonly used in misinformed claims about COVID-19, including: _"cure"_, _"oil"_, _"tea"_, _"mask"_, _"natural"_, _"traditional"_, and _"prevent"_. If a tweet or URL matched one of the keywords, they were briefly further investigated - if they seemed relevant, they were labeled and added to the dataset. We collected 59 unique URLs relating to Cures, Prevention, and Origins. We then mapped all of the tweets that contained the URL links in this curated dataset. This dataset does not differentiate between sarcasm, jokes, or the validity of statements/URLs. To view our preprocessing code, please visit our open source [GitHub repository]() (***COMING SOON***). 

***Political Bias***

Every tweet in the displayed dataset references a URL. Below is a list of the ways in which a URL can appear:  
1. *Retweeted URLs/Narratives*  
    * Retweeted news article tweeted by a regular Twitter user.  
    * Retweeted news article tweeted by a news agency account on Twitter.  
    * Retweeted commentary by well-known individuals relating to COVID-19 **narratives** or **claims**.  
2. *Tweeted URLs/Narratives*  
    * Tweeted news article by a regular Twitter user.  
    * Tweeted news article by a news agency account.  
  
In order to label URLs with a poltical bias, we searched for the domain in the [NELA-GT-2019](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/O7FWPO) dataset using the AllSide Bias label. _Side Note: NELA-GT-2019 Dataset is a "A Large Multi-Labelled News Dataset for the Study of Misinformation in News Articles"_. URLs in this dataset categorized as _"Lean Left"_ or _"Lean Right"_ from AllSides Bias label were relabeled as _"Left"_ or _"Right"_ respectively. As a 501(c)(3) not-for-profit, IQT Labs is prohibited from “participating in, or intervene in (including the publishing or distributing of statements), any political campaign on behalf of (or in opposition to) any candidate for public office.”  To avoid any perception of political campaign intervention, we therefore also removed political candidates from this dataset.

### How to View our Visualization

**IQT Internal Employees** 

Visit this [link](https://vsrv-plotly.a.internal/claim-mapping/) to view the internal Narrative & Claim-Mapping Visualization. You can also view all the code to run this visualization on [GitLab](https://gitlab.iqt.org/labs/lab41/claim-mapping). Make sure you are signed on to the VPN or it will not work.

**External Visitors** 

***COMING SOON***
Check back soon to visit the public version of our Narrative & Claim-Mapping Visualization once it's released! 
