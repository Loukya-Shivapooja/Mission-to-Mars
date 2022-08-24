# Mission-to-Mars
## Project Overview
The purpose of this project is to build a Web App that will scrape several websites for the most recent Mars data. The extracted data is stored in a NoSQL database and then an HTML page is created to display the findings.
### Resources
* Web pages scraped:
  * https://data-class-mars.s3.amazonaws.com/Mars/index.html
  * https://spaceimages-mars.com
  * https://galaxyfacts-mars.com
  * https://marshemispheres.com/
* Software:
  * Python
  * Jupyter Notebook
  * Pandas, BeautifulSoup, Splinter, ChromeDriverManager, Flask, PyMongo
  * MongoDB
  * HTML5
  * Bootstrap 3
## Objective
#### Step 1 - Scraping**
**NASA Mars News**
Scrape the NASA Mars News Site and collect the latest News Title and Paragraph Text
**Featured Image**
* Visit the URL for the JPL Featured Space Image
* Use Splinter to navigate the site and find the image URL for the current Featured Mars Image and assign the URL string to a variable called featured_image_url
* Make sure to find the image URL to the full size .jpg image
* Make sure to save a complete URL string for this image
**Mars Facts**
* Visit the Mars Facts webpage and use Pandas to scrape the table containing facts about the planet including Diameter, Mass, etc.
* Use Pandas to convert the data to a HTML table string
**Mars Hemispheres**
* Visit the USGS Astrogeology site to obtain high resolution images for each of Mar's hemispheres
* Save both the image URL string for the full resolution hemisphere image, and the Hemisphere title containing the hemisphere name.
* Use a Python dictionary to store the data using the keys img_url and title
* Append the dictionary with the image URL string and the hemisphere title to a list
* This list will contain one dictionary for each hemisphere
#### Step 2 - MongoDB and Flask Application
* Use MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from the URLs above
* Convert Jupyter Notebook into a Python Script called scrape_mars.py with a function called scrape that will execute all of the scraping code from above and return one Python Dictionary containing all of the scraped data
* Create a route called /scrape that will import the scrape_mars.py script and call the scrape function
  * Store the return value in Mongo as a Python Dictionary
* Create a root route / that will query the Mongo database and pass the Mars Data into an HTML template to display the data
* Create a template HTML file called index.html that will take the Mars Data Dictionary and display all of the data in the appropriate HTML elements
## Summary
<img width="1305" alt="Screen Shot 2022-08-24 at 11 15 19 AM" src="https://user-images.githubusercontent.com/107584361/186493267-338b207d-1027-4a3f-b79c-35ba40f0206a.png">

* The web page is updated with Mars hemisphere heading, Mars images and titles of each images. 
* Bootstrap 3 components are used to style the webpage such as 
  * An image is added to header background.
  * The click button is changed to red.
  * The Back-ground of the page is cahnged to teal color.
  * The back-ground color of the paragraphs are changed to differnt color.
  * The table back-ground and title back-ground are change to different color. 
<img width="1309" alt="Screen Shot 2022-08-24 at 11 15 49 AM" src="https://user-images.githubusercontent.com/107584361/186495356-ce93c805-c26f-4fa7-b946-b1fb6c53ef3c.png">
