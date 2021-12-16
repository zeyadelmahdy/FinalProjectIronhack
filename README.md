# Used Car Value Estimator - Final Project Ironhack

by Zeyad ElMahdy

## Understanding Used Car Prices in Canada 

### Table of content

- [Problem Statement](#problem-statement)
- [Process & Methods](#process-&-methods)
- [Final Product](#final-product)
- [Wishlist](#wishlist)

### Problem Statement

Too often people are trying to buy or sell used cars without really knowing how to price their car or worse not knowing if they are being ripped off by someone. Through this project, we set out to give power to the people and provide visibility/transperancy to the Canadian car market by letting users know the actual market value of any given vehicle. 

### Process & Methods

#### The Data Set: 

We decided to scrape Kijiji Autos listings as it is the most popular listings website in Canada. As the project moved on, we found that scraping the whole website would take much longer than expected to we decided to enhance the dataset by bringing in an external set from Kaggle. Both datasets contained data points such as make, model, year, color, mileage, location, color. The Kaggle data was much more comprehensive than Kijiji as it included very granular details such as the VIN number and other unecessary data points for our project. 

#### The Task: 

Use the data at hand to create a tool that returns the current market value of any given car based on a set of features initially Make, Model, and Year. Later on Mileage was added to the equation to give better estimates based on condition. 

### Methodology 

- Scraping the data
- Exploring & cleaning the data
- Creating logic for the user input tool
- Reviewing results


##### Scraping the data 

First step was to identify what data points we need. We concluded that we needed the below at a minimum: 
 - Make
 - Model
 - Year
 - Mileage
 - Location

So we started to explore Kijiji Autos's HTML but was faced with the challenge of infinite scroll. We then moved on to the general kijiji listings. However, that also came with it's challenges. Scraping that proved very tedious and time consuming as the scraper had to visit each listing to fetch the data so we were only able to scrape 4k listings before it crashed. 

That was when we decided to bring an external dataset from Kaggle to help enhance the project. 

##### Exploring & cleaning the data
We examined the data in both Python and Tableau to see if we can identify any issues/trends within the data

- Droping nulls
- Removed unnecessary columns
- Cars priced at $0
- Cars with 0 mileage

### Final Product
We had to map out every scenario the user could add and create a possible response for it. Then we created queries to run based on the input. 

The program takes Make, Model and Year from the user and runs based on the average price of these features (given that they exit in the database). 

Then it prompts the user to ask for their Maximum Mileage, checking each listing that is less than the max and returning an updated market value based on that. 

The input stops after the mileage section and then does not re-start. 

##### Reviewing results

After each initial result, we had to double check each given variable to make sure the program was given accurate resulsts. Some iterations were made at that point to make the model a bit more rigid and to handle lower case data for example. 

Overall, the program works well if the required car is in the database. 


### Wishlist

With more time and resources we would have liked to have more data points on a car's maintenance and accident history. This will be crucial in allowing us to make certain recommendations based on how durable a certain car is. 

