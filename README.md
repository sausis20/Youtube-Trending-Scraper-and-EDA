# Youtube-Trending-Scraper-and-EDA

The script is a modified version of [this](https://github.com/mitchelljy/Trending-YouTube-Scraper) Youtube's trending video scraper. This script scrapes the most relevant information from videos for the selected countries specified in 'country_codes.txt' file. The example output files can be found in the output directory.

## Country Codes
The script used 12 country codes for which it collected trending video data. These are 2 letter country abbreviations (LT, LV, EE, PL, FI, SE, NO, US, CA, GB, DE, FR), however the following EDA was done only on the Baltic countries (LT, LV, EE). 

## Scraping results
The script collected data between 2022-07-22 and 2022-11-03, and contains data for a total of 76 unique dates. 

## Data cleaning and EDA
After the data was scraped, it was then combined into a single dataset using the script in 'combine csv data.ipynb'. Additionally, as every country has different video category codes (i.e. 2 - Autos & Vehicles, 10	- Music, 17 - Sports, etc), categories for LT, LV and EE were additionally scraped and added to the dataset. 

The Exploratory Data Analysis can be found in 'data cleaning and EDA.ipynb' file. 

## EDA conclusions
- 40% of trending videos have less than 1 million views, and 66% have less than 2 million views
- Some videos were trending for mulpitle days and therefore appeared in the dataset more than once. From the total of 11310 entries, 1861 are unique videos.
- On average, videos are commented 0.3% of the time i.e. around every 307 views
- Most of the videos trend for less than 5 days and similarly, they usually become trending after <= 5 days after being published. This suggest that Youtube's top trending list is fast-changing and newly published videos are most popular
- Trending video titles vary a lot in lenght - although usually their lenght is between 20 and 100 long
- Various articles and symbols from the Cyrillic script like | , в, -, и, were common in trending video titles. Excluding these symbols, the words 'Alexey', 'Arestovych' and 'Game' were the most common words in the trending video titles
- The category that has the largest number of trending videos is 'News & Politics' with 395 videos, followed by 'Entertainment' with 388 videos.

## License
This project is licensed under the BSD 2-Clause License - see the LICENSE.md file for details
