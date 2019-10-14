# Jodi's Internship Advisory

Hello reader. I used this project to practice web scraping, data munging and data visualization, which are basic skills a data scientist should possess.

The guinea pig I used is Indeed.ca. I wanted to scrape its query results, which are job postings, for text of job title, company name, location, summary and salary. The purpose of this analysis is to understand internship postings I may be personally interested in.


### Python Packages

If you wish to run my script, please install:

• Python 3.0, Jupyter Notebook

• Requests, BeautifulSoup

• Pandas, Numpy, Matplotlib

• Geopandas, Descartes

• NLTK, sklearn, re


### Overview

Overview of data scraped on indeed.ca on September 23rd 2019.

• Queried indeed.ca for jobs with keywords: 'data+intern', 'devops+intern', 'full+stack+intern', 'python+intern', 'tester+intern'; max results = 5000

• Final combined csv: 5 columns, 976 rows

• Column names: 'job_title', 'company_name', 'location', 'summary', 'salary'

• Data type: all strings/objects

• 521 unique job titles, 252 unique company names, only 25 postings with salary information

### Pre-processing

• Used pandas dataframe methods to clean scraped data

• Used word_tokenize method from NLTK to split the summary text, extracted summary words without stopwords (sklearn)

### What companies am I likely to work for...

<p align="center"> 
<img src="/images/company_wordcloud.png">
</p>

WordCloud python library was used to generate this image.

• TD Bank is overrepresented

• Ciena takes second

### Which Canadian city will I be in?

<p align="center"> 
<img src="/images/location_choropleth.png">
</p>

Geopandas and Descartes helped combine job location count and the Canadian map to create a choropleth map.
.shp data of the Canadian map was found [here.](https://www.sciencebase.gov/catalog/item/5ab555c6e4b081f61ab78093)

• Internship postings highly concentrated in Ontario with a total of 566 out of 976, with no close second

<p align="center"> 
<img src="/images/top_cities.png" width="200" height="280">
</p>

• Toronto is the city with the greatest number of relevant internships

• Montreal, Vancouver and Ottawa are all great places to be in for tech internships

### What are keywords HR like to use?

<p align="center"> 
<img src="/test_csvs/test_pngs/machine.png">
</p>

<p align="center"> 
<img src="/test_csvs/test_pngs/software.png">
</p>

<p align="center"> 
<img src="/test_csvs/test_pngs/developer.png">
</p>

### Conclusions

### Acknowledgments

A big thanks to Haolong, my ITI1120 teaching assistant. He gave me tips on dataframes and graphs.

Another shout out to awesome data bloggers at Medium.com, whose code I studied.

Thank you Google, Stackoverflow, Kaggle - and various other open source information.
