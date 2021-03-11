# Funding a Start-up:
### Evaluating the Business Impact of Funding Types, Sources, Amounts and Timing
### Authors: Caleb Case | Aaliyah Fiala | Jonathan Kerr | Sai Muktevi | Kevin Sweet

## Introduction
Developing a new business takes time, money, and expertise.  Accelerating its growth takes even more of the same. It can take years to achieve profitability so many new businesses look to investors to bridge the financial gaps.  

This study will examine relationships between various features of the fundraising process (such as amount and type of money raised), how financing differs between industries, and whether seed funding is a good predictor of venture funding.

 We will be attempting to answer the following questions using statistical analysis:
Is the average amount of money raised correlated with the industry the company is in?
Can a company expect to have more financing rounds if they’re in a particular industry?
Does the amount of money raised in the seed round correlate with the year it was raised?
Does the proportion of companies that get seed funding also get venture funding?

## Dataset Description
Our original source of data is Crunchbase. Although we haven’t directly used any Crunchbase APIs to obtain this data, we obtained it via a secondary source on kaggle. Crunchbase is a platform for finding business information about private and public companies. Crunchbase information includes investments and funding information, founding members and individuals in leadership positions, mergers and acquisitions, news, and industry trends. Originally built to track startups, the Crunchbase website contains information on public and private companies on a global scale.

Crunchbase sources its data in four ways: the venture program, machine learning, an in-house data team, and the Crunchbase community. Members of the public can submit information to the Crunchbase database. These submissions are subject to registration, social validation, and are often reviewed by a moderator before being accepted for publication.
 
This dataset was found on Kaggle consisting of funding, investments and other details about startup companies collected via Crunchbase. This dataset contains 49,437 data points where each point represents a startup company. There are 40 different attributes associated with the data. There’s basic location information such as country, state and city. Important dates associated with each startup such as when they received their first and last funding or when they were founded, are included. We also have important links to the websites of these companies, the type of industry they operate in and the markets they cater to. The rest of the information is mainly based on funding amounts and types of funding received. Then we have an attribute called status that shows whether a startup is operating, acquired or closed. A table of each attribute and their descriptions can be found in the Appendix (9.1).

The data is largely composed of different types of funding amounts (in USD) and is mostly quantitative in nature. There are other fields that describe important dates and years. The survivorship of startups described by the status is nominal in nature. Apart from this we have other fields that provide more qualitative information about each of the companies like their market areas, categories, and location.       
54294
## Issues and Biases
Upon an initial quick exploratory data analysis (EDA) of the dataset, we arrived at multiple conclusions about the dataset and ran into some barriers. The total data contains about 5% closed startups, 11 % null and above 70% operating startups. This can be contrasted with a 90% failure rate of startups. Therefore any analysis performed on this database regarding survivorship might be intrinsically biased because data doesn't include a lot of failed startups. This eliminates the possibility of using the “status” attribute for any statistical analysis on the entirety of the dataset forcing us to filter in on particular aspects of the data for study. If we can choose certain parameters to look at and eliminate the confounding variables to some degree then we can have better statistical significance in our analysis results.

It appears that 46.3% of the total data comes from the USA. This means that almost half of the data is mostly from America and in that data almost 36% is only from California. We realized that the amount, type and means of funding from region to region can vary greatly depending on socio-economic factors at play in that region. After deciding we would be looking only at the USA data, another concern was with the distribution of data across different markets which led us to find that almost 30% of the companies didn’t have a clear distinction of which market they were from (filled in with “other”). Among the remaining that did have clear market information, around 15% operated in only the Software and Biotechnology markets. 

Other discrepancies, biases or interesting findings in the data are mentioned in the following. The year at which a company was founded dated back further than 1950 which seemed concerning as there could have been an issue in recording the data. However, most companies were found to be between 1980 to 2014. The average total funding came to be around 15 million USD across the different companies. We found that the highest total funding received was about 30 billion USD by Verizon Communications. This was an interesting find to encourage us to go back and see what range of data we would be looking at with such outliers. Regarding funding types, it was also found that only 28% of companies got funding in the “seed” stage. Such information about the different funding sources allowed us to shape our questions about the data for analysis.

These issues and discrepancies were explored more as we designed our approach and narrowed down our scope which will be explained in further detail in the following sections. Keeping in mind all of this information we proceeded to frame our questions ensuring quality in our analysis.    

