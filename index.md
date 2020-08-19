## Welcome to our COVID-19 Narrative & Claim-Mapping Visualization

This is our supplementary guide where you can find information on how this visualization was created, what this visualization should be used for, and what it should not be used for. Any direct questions about the visualization should be directed to [@Katelyn98](https://github.com/katelyn98).

Some distinctions between defintions in regards to our visualization: 
- **Topic** ~ A category generalizing a group of narratives
  - Example of topics include Cures, Preventions, and Origns.
- **Narrative** ~ A specific category grouping several claims within a given topic
  - Example of narratives for Cures include using natural oils/herbs, whiskey mixed with honey, or disinfectants. 
 - **Claim** ~ A subjective generalized statement being made in objective context 
    - Example of a narrative within the claims for cures category is: _"Hot whiskey mixed with honey cures Coronavirus"_

### Hand-Curated Labeled Dataset

The hand-curated dataset is in no means meant to advertise, categorize, or promote trends of information - it is solely used for assisting in the development of the narrative-mapping visualization. This dataset does not also take into account sarcasm, jokes, or the validity of statements/URLs. Any tweet/URL talking about the narrative that was deemed relevant was added to the dataset. This hand-curated dataset consisted of 779 tweets that were hand-picked and manually labeled from March and April 2020. The twitter data was hydrated from this [COVID-19 Twitter Dataset](https://github.com/echen102/COVID-19-TweetIDs). To view specific code on how this dataset was created, view our open source [GitHub repository]() (***COMING SOON***). 

***Filtering***

We had 60,442,735 tweets combined from March and April 2020. We applied filters to narrow down to tweets that were in English, were tagged with a location, and shared a URL. In some cases the URL that was shared was to another tweet - this is how Twitter's API represents retweeted tweets. After applying filters, we were left with 177,279 tweets. From these tweets, we grouped all the tweets by a common URL. Then for every URL, we printed out the URL and the text of the tweet that referenced that URL. A keyword search was then performed on the text of the tweets by URL - keywords used include: _"cure"_, _"oil"_, _"tea"_, _"mask"_, _"natural"_, _"traditional"_, and _"prevent"_. If a tweet or URL matched one of the keywords, they were briefly further investigated - if they seemed relevant, they were labeled and added to the dataset. 

***Political Affiliation***

Every tweet in our dataset references a URL. There are a few different cases of URLs that are present in this dataset. Below is a list of occurences that a URL appears:
1) *Retweeted URLs/Narratives*
  a) Retweeted news article tweeted by a regular Twitter user
  b) Retweeted news article tweeted by a news agency account on Twitter
  c) Retweeted commentary by political figures or well-known CEOs relating to COVID-19 **narratives** or **claims**
2) *Tweeted URLs/Narratives*
  a) Tweeted news article by a regular Twitter user
  b) Tweeted news article by a news agency account
  
In order to label URLs with a poltical affiliation, the URLs were manually searched for in the [NELA-GT-2019](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/O7FWPO) dataset using the AllSide Bias label. _Side Note: NELA-GT-2019 Dataset is a "A Large Multi-Labelled News Dataset for the Study of Misinformation in News Articles"_. URLs in this dataset categorized as _"Lean Left"_ or _"Lean Right"_ from AllSides Bias label were relabeled as _"Left"_ or _"Right"_ respectively. Some political figures were also given a poltiical affiliation of the polticial party they are currently associated with. 

### How to View our Visualization

**IQT Internal Employees** 

Visit this [link](https://vsrv-plotly.a.internal/claim-mapping/) to view the internal Narrative & Claim-Mapping Visualization. You can also view all the code behind this project on [GitLab](https://gitlab.iqt.org/labs/lab41/claim-mapping). Make sure you are signed on to the VPN or it will not work.

**External Use** 

***COMING SOON***
Check back soon to visit the public version of our Narrative & Claim-Mapping Visualization once it's released! 
