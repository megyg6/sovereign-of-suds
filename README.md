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
- Notebooks info

#### Data Question:
 Does alcohol by volume (ABV) play a role in how well a beer is scored? 
    
#### Web Scraping:
The site that data was gathered from uses Cloudflare, software that protects against bot attacks and web scraping. To bypass that, Cloudscraper was used. (https://pypi.org/project/cloudscraper/) (documentation) To begin the project, one page of beer was scraped first to understand where to find the data in the html code from 'inspect element' on the webpage. The next step was to "zoom out" a level and scrape the hrefs that held the parameters needed to pull multiple beers from a list reflected on one webpage. Following this step, there needed to be a way to loop through each page of the beer subtype. The last step was "zooming out" another level to scrape the subtype links from the beer-type page.

(In the opposite direction of how it was built the scraper took the following route: Beer-style page (had a list of subtype links) > page (from which there were multiple) of links to beer webpage > webpage of beer data > data gathering)

![alt text](![image](https://github.com/megyg6/sovereign-of-suds/assets/130840783/a308e9cf-bfe4-48b2-b596-46f3229c3abb)
)


#### Data Cleaning:
Due to a challenge, when scraping the website, multiple notebooks were created and a few duplicates arose from this. An empty list was created to stack each data frame on top of each other, and then it was concatenated with its indices to match the new data frame size. Data types were adjusted and changed, but to do so, characters had to be removed or replaced. The biggest change during this process was the addition of the 'type' column. This version of the cleaned data frame was saved as a csv file and used in the following EDA portion.

![alt text](![image](https://github.com/megyg6/sovereign-of-suds/assets/130840783/a308e9cf-bfe4-48b2-b596-46f3229c3abb)
)

#### EDA:
This portion dealt with getting to know the data by looking at numerical ranges and amounts as well as looking at the type of categorical data obtained. It was noticed that not all types of beer had the same amount of data gathered due to the different number of subtypes each had. It was also noted that only one subtype had significantly less data than the other subtypes. When looking at it on the website scraped, this was due to the subcategory not having more than sixteen beers total. 
The majority of the EDA consisted of grouping, counting, looking for midpoints, graphing, and understanding how to present its story to an audience.
The final visualizations were later done using Tableau.

#### Challenges: 
1) There were moments when the site (and this could have also been in conjunction with internet instability) placed a time-out on the web scraping process. The original intention had been to scrape every beer element from the website. These timeouts were random and lasted for different intervals. However, it was found that by starting a new notebook and restarting the process, the scraper could function again (not always, but more often than not). To also combat this, if the scraper was being blocked, the header portion was alternated and there were a few 'time delays' placed during the process. (A proxy was not used during this project, but would have been the best option to deal with this issue.)

2) Initially, Cloudscraper was only called once at the beginning of a notebook, but eventually it was noticed that 403 would pop up later on as a status when double-checking if the scraper was receiving a response. (Perhaps due to a personal limitation, when reading through the documentation, this might have been the case, but a strategy was implemented to overcome this.) This led to the creation of 'cook_soup' as a defined function, to go through the process of calling Cloudscraper and 'making soup' with the BeautifulSoup library.

3) During the web scraping process, the type of beer was not collected, only the subtype was named. This prompted the creation of an extensive if / else statement.
  
