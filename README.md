# Web Scraping Challenge - Mission to Mars

## The Challenge
Build a web application that scrapes various websites such as [Mars News Site](https://redplanetscience.com/)for data related to the Mission to Mars and displays the information in a single HTML page using BeautifulSoup. 


## File Directory
- `mission_to_mars.ipynb contains all scraping and analysis script
- Images folder contains screenshots of Mars app
- Template folder holds `index.html` which is our main web page displaying all the scraped data

## Process
- Using Pandas, scraped the Mars Facts webpage [here](https://galaxyfacts-mars.com) and converted the data to a HTML table string.
- With `splinter` navigated the site and found the image url for the current images.
- Saved both the image url string for the full resolution image,and name and title of the image. Then used a Python dictionary to store the data.
- Appended the dictionary with the image url string and the hemisphere title to a list. This list contained one dictionary for each hemisphere.
- Using MongoDB with Flask, created a HTML page that displays all the scraped information.
- Created a Python script with a function `scrape` that executes all scraping code and returns one Python dictionary containing all of the scraped data.
- `/scrape` route made to import `scrape_mars.py`  script and calls the `scrape` function. The route queries Mongo database to paas the dictionary data and display the data in the appropriate HTML elements. 
- 
## Results

<img width="586" alt="final_app" src="https://user-images.githubusercontent.com/16246354/156901691-5d83af40-0b8d-42a9-8ec2-efc0fc6f186c.png">
