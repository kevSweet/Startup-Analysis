# Funding a Start-up:
## Evaluating the Business Impact of Funding Types, Sources, Amounts and Timing
### Authors: Caleb Case | Aaliyah Hänni | Jonathan Kerr | Sai Muktevi | Kevin Sweet
## Abstract
This study reviews several questions of interest for entrepreneurs as well as investors about Start-up organizations. We performed our analysis using the Kaggle dataset of Crunchbase 2014 snapshot, which includes approximated 50,000 companies. We found that the average amount of money raised, and the average number of funding rounds, both vary by industry. We concluded that the average amount of seed money invested is increasing 13.5% annually. We also found, controversially, that companies that did not have seed rounds are 4 times more likely to have a venture round. Our results should be received with caution, as our dataset included strong survivorship, regional, and market bias.

## Introduction
Developing a new business takes time, money, and expertise.  Accelerating its growth takes even more of the same. It can take years to achieve profitability so many new businesses look to investors to bridge the financial gaps.  

This study will examine relationships between various features of the fundraising process (such as amount and type of money raised), how financing differs between industries, and whether seed funding is a good predictor of venture funding.

We will be attempting to answer the following questions using statistical analysis:

1. Is the average amount of money raised correlated with the industry the company is in?
2. Can a company expect to have more financing rounds if they’re in a particular industry?
3. Does the amount of money raised in the seed round correlate with the year it was raised?
4. Does the proportion of companies that get seed funding also get venture funding?

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

## Conclusion
In the analysis of the crunchbase dataset, we discovered a number of statistically significant features.  We found that within this data group:
The average amount of funding a company raises is associated with the industry the company is in.
The average number of fundraising rounds are associated with the industry the company is in.
The amount of seed money being invested is increasing over time (13.5% growth YoY).
Companies that don’t do a seed round tend to do venture rounds more frequently.

It can’t be overstated that given the previously mentioned biases in the data, these findings should be viewed with skepticism.  It is not realistic to assume that 55% of all startup companies are going to receive venture capital funding, especially when industry norms are closer to 0.05% (Wood, 2020).  With this result in doubt, we have to consider that our other results could also be strongly biased, putting the statistical significance of all our findings into question.  While we would recommend using our methodology for further study in this area, we can’t recommend extrapolating the results to real world predictions.

## Future Works
Grouping Markets
A difficulty that arose while assessing markets and how different types or funding amounts varied between them was that there were about 754 different categories of markets that start-ups operated in. We chose to scope down our project by selectively handpicking a few markets that had enough data to be considered for analysis. We found that many categories of markets were largely similar and could be grouped into larger umbrellas of categories. The groups could be centered around software, healthcare/medicine, multimedia  and so on. There was also the possibility of creating two categories of Technology and Not Technology that was considered. A study further developing the idea of grouping these markets and testing hypotheses based on funding types for these larger groups would be interesting to pursue. This would give us a better understanding of more successful markets or market-types in terms of funding.   

Bubbles and Lower-Percentile Seed Funding
One discovery of interest was that the 25th and 50th percentiles of seed funding only showed growth during the early 2000’s dotcom boom, and dropped back to a constant rate after the crash. Further exploration is warranted in determining if this type of behavior could be useful in predicting future bubbles before they crash.

Impact of Industry on Seed Funding Over Time
The dotcom bubble had a dramatic impact on the average seed funding levels, even though it should have primarily impacted software companies. A further analysis into seed funding trends by industry may reveal how deeply our findings are the result of just software or specific industries experiencing heavy growth.

Validate Seed and Venture Funding Findings
With the many issues and biases that we came across in this dataset, we realized that we could never have a high confidence in generalizing our results. We decided that in order to validate our findings, the only path forward would be to find similar datasets which are less biased and conduct the same tests. In this way we could validate our findings regarding seed and venture funding and develop more generalized results useful for further study into start-up funding type dynamics. 

## File Structure
Below is a tree representation of our github repository:
```
│   .gitignore
│   LICENSE.md
│   README.md
│
├───Datasets
│       industryData.csv
│       investments_VC.csv
│       kaggle_data_cleaned.csv
│       kaggle_data_cleaned.rds
│
├───Documentation
│       Funding a Start-up Presentation.pptx
│
├───EDA
│       Amount Raised by Industry Exploratory Analysis.Rmd
│	Amount-Raised-by-Industry-Exploratory-Analysis.html
│	CheckAnalysisAssumptions.Rmd
│       Exploratory Analysis.nb.html
│       Exploratory Analysis.Rmd
│	Number of Rounds Exploratory Analysis.Rmd
│	Number of Rounds Exploratory Analysis.nb.html
│	
├───Industry Analysis
│   │   Funding by Industry.Rmd
│   │   Funding-by-Industry.html
│   │
│   └───Figures
│           unnamed-chunk-3-1.png
│           unnamed-chunk-4-1.png
│           unnamed-chunk-4-2.png
│           unnamed-chunk-4-3.png
│           unnamed-chunk-4-4.png
│
├───Seed and Venture Funding
│       SeedAndVentureFunding.Rmd
│ 	SeedAndVentureFunding.html
│
└───Seed Funding Over Time
        SeedFundingOverTime.rmd
        SeedFundingOverTime.html
```
