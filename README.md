# Sovereign of Suds
## An analysis of the most reviewed beers on Beer Advocate (A community dedicated to the support and promotion of beer)
Capstone Project for Cohort DA10 at Nashville Software School 

### Motivation and Description:
This project was motivated to build an activity that advanced web scraping, data cleaning, EDA, insight gathering, and visualization skills. The project is designed to help consumers order a beer that they will most likely enjoy at a brewery or bar by providing better insight into top-reviewed beers from BeerAdvocate (https://www.beeradvocate.com/). This would help individuals who find all the beery options overwhelming. 

### Table of Contents:
- Data Questions
- Web Scraping
- Data Cleaning
- EDA
- Challenges

#### Data Question:
 Does alcohol by volume (ABV) play a role in how well a beer is scored? 
    
#### Web Scraping:
The site that data was gathered from uses Cloudflare, software that protects against bot attacks and web scraping. To bypass that, Cloudscraper was used. (https://pypi.org/project/cloudscraper/) (documentation) To begin the project, one page of beer was scraped first to understand where to find the data in the html code from 'inspect element' on the webpage. The next step was to "zoom out" a level and scrape the hrefs that held the parameters needed to pull multiple beers from the list reflected on one webpage of a beer subtype. Following this step, there needed to be a way to loop through each page of the subtype. The last step was "zooming out" another level to scrape the subtype links from the beer-type page.

(In the opposite direction of how it was built the scraper took the following route: Beer-style page with list subtype links > subtype list with multiple pages > webpage of beer data > data gathering)

![alt text](![image](https://github.com/megyg6/sovereign-of-suds/assets/130840783/a308e9cf-bfe4-48b2-b596-46f3229c3abb)
)


#### Data Cleaning:


#### EDA:

#### Challenges: 


  # Read me in progress
  
