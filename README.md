
## Analysis of Social Chatter vs Market Results, Post IPO
---
### Executive Summary
Prior to filing an initial public offering(IPO), a privately held company's value is largely a guess.  While the company needs to meet IPO criteria, by providing insight into income, assets, revenue growth, etc. Pre-IPO companies don't have any feedback or demonstrated buyer history to measure the immediate purchase of its shares at a particular price.  
This analysis measures social queues to market movements in an attempt to find a correlation.

---
### Concept
When companies IPO there is no historical trade activity to complete financial modeling analysis.  Our analysis reviews social chatter for 90 days from the IPO launch to see if it could be used as a mechanism to determining future stock fluctuations and/or trading volume.
The overall motivation for this project was the general excitement in the uptick of IPO’s and the curiosity of finding a way to validate or predict market prices and volumes.
 
---
### Data Source 
List of companies that IPO’d
    - This list was used to determine 15 samples  
Twitter 
    - A general public use software named snscrape was used to scrape twitter. This allowed us to pull lots of raw twitter data while also setting certain criteria. 
Stock data 
    - The Alpaca API was used, as we had a working knowledge of the API and it met time constraints.

---
### Data Collection & Cleaning
SNScrape
    - 90 days Twitter Data in .json format - Going over an output of 100,000 results we found often crashed the program
    - Created Pandas Dataframes from .json data to clean the data
    - Once ready, exported the Twitter data to .csv to use in our analysis notebook.
Used Python collections module to count tweets by day
    - Alpaca SDK
    - Generally clean data pulls
    - Formatted datetime to date
    - Dropped columns that were irrelevant
SQL
  - Added each individual stocks data (Twitter & Market) as SQL tables and joined accordingly throughout analysis

---
### Approach
Tech 
  - SNScrape
  - Alpaca SDK
  - Pandas
  - Jupyter Lab
  - hvPlot & Matplotlib

Roles 
  - Viny - Lead Coder & Data Cleaner
  - Niki - Code Collaborator & Project Manager
  - Jake - Code Collaborator & Data Visualizer  

Challenges 
  - Stock picks based on ticker (Examaple: ticker is a word)
  - Amount of data
  - Multiple axes graphs

---
### Outcome 
The data reflects that there is often a correlation between Twitter mentions and daily stock trading volumes. However, we did not find a correlation in Twitter mentions and price movement. 

*insert tables*
---
### Next Steps 
Additional topics to research
    - The effects of social influencers on stock volumes and price
    - The effects of CEO tweets, publications, media outlets, on stock volumes and price 
    - Deep dive into defining, researching and analyzing social sentiments. 

---
### Appendix list of stocks used   
| Company | IPO Date | Ticker |
| :--- | :--- | :---:| 
|Oatly	|5/20/2021	|OTLY|
|Air BNB 	|12/10/2020	|ABNB|
|Esports Technologies 	|4/15/2021	|EBET|
|Apria 	|2/11/2021	|APR|
|F45 Training  	|7/15/2021	|FXLV|
|Upstart Holdings	|12/16/2020	|UPST|
|Bumble 	|2/11/2021	|BMBL|
|Regencell Bioscience 	|7/16/2021	|RGC|
|Sprinklr	|6/23/2021	|CXM|
|DigitalOcean	|3/24/2021	|DOCN|
|Skydeck Acquisition Corp	|1/28/2021	|SKYA|
|Coupang	|3/11/2021	|CPNG|
|Vizio	|3/25/2021	|VZIO|
|Duolingo	|7/28/2021	|DUOL|
|VTEX	|7/21/2021	|VETX|

