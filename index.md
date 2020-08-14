## Welcome to our COVID-19 Narrative Mapping Visualizatoin

This is our supplementary guide where you can find information on how this visualization was created, what this visualization should be used for, and what it should not be used for. Any direct questions about the visualization should be directed to [@Katelyn98](https://github.com/katelyn98).

Some distanctions between defintions in regards to our visualization: 
- **Claim** ~ A subjective generalized statement being made in objective context
  - These are more general and considered as a parent category. There have been several claims spreading related to the current Coronavirus Pandemic about Origin Stories, Cures and Treatments, etc. 
- **Narrative** ~ A specific subjective statement being made in an objective context
  - These are more specific and considered as a child category. THere have been several narratives spreading related to specific claims made during the current Coronavirus Pandemic. 
  - An example of a narrative within the claims for cures category is: _"Hot whiskey mixed with honey cures Coronavirus"_

The current visualization presents a variety of narratives related to claims for cures. 

### Hand-Curated Labeled Dataset

The hand-curated dataset is in no means meant to advertise, categorize, or promote trends of information - it is solely used for assisting in the development of the narrative-mapping visualization. This dataset does not also take into account sarcasm, jokes, or the validity of statements/URLs. Any tweet/URL talking about the narrative that was deemed relevant was added to the dataset. This hand-curated dataset consisted of 779 tweets that were hand-picked and manually labeled from March and April 2020. The twitter data was hydrated from this [COVID-19 Twitter Dataset](https://github.com/echen102/COVID-19-TweetIDs). To view specific code on how this dataset was created, view our open source [GitHub repository]() (**add link**). 

***Filtering***
We had 60,442,735 tweets combined from March and April 2020. We applied filters to narrow down to tweets that were in English, were tagged with a location, and shared a URL. In some cases the URL that was shared was to another tweet - this is how Twitter's API represents retweeted tweets. After applying filters, we were left with 177,279 tweets. From these tweets, we grouped all the tweets by a common URL. Then for every URL, we printed out the URL and the text of the tweet that referenced that URL. A keyword search was then performed on the text of the tweets by URL - keywords used include: "_cure_", "_oil_", "_tea_", "_mask_", "_natural_", "_traditional_", and "_prevent_". If a tweet or URL matched one of the keywords, they were briefly further investigated - if they seemed relevant, they were labeled and added to the dataset. 

### Narrative-Mapping Visualization

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/katelyn98/COVID-19-Narrative-Mapping/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Metadata Analysis Visualizations

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
