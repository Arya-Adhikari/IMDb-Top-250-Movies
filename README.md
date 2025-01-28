IMDb Top 250 Movies Scraper

This script scrapes the IMDb Top 250 movies list, extracts movie details such as titles, ratings, genres, and durations, and stores them in a Pandas DataFrame. The data is then saved into a CSV file for further analysis.

Requirements
Before running this script, make sure the following Python libraries are installed:
•	requests: For sending HTTP requests to fetch web page content.
•	beautifulsoup4: For parsing the HTML content of the web page.
•	pandas: For organizing the scraped data into a DataFrame and saving it as a CSV.
•	json: For parsing the structured JSON data embedded in the page.

To install the required libraries, run the following command:
pip install requests beautifulsoup4 pandas

Overview

This script performs the following tasks:
1.	Fetch IMDb Top 250 Movies:
o	Sends an HTTP GET request to the IMDb Top 250 movies page using the requests library.
o	Handles potential blockages by setting a User-Agent header to mimic a browser visit.

2.	Parse HTML:
o	Parses the HTML content using BeautifulSoup to extract relevant movie data.

3.	Extract JSON-LD Data:
o	Extracts the structured JSON-LD data containing movie details like name, genre, duration, and ratings.

4.	Store Data:
o	Stores the extracted movie information (title, URL, description, best/worst ratings, genres, duration) in a Pandas DataFrame.

5.	Save to CSV:
o	Saves the DataFrame into a CSV file named Top250IMDbmovies.csv.

How to Use
1.	Run the Script:
o	Ensure that you have installed the required libraries (requests, beautifulsoup4, and pandas).
o	Simply run the Python script, and it will scrape the IMDb Top 250 movies page and save the results to a CSV file.
python imdb_top_250_scraper.py

2.	Output:
o	After execution, a CSV file named Top250IMDbmovies.csv will be saved in the working directory containing the following columns:
	Title: The movie title.
	URL: IMDb URL of the movie.
	Description: Short description of the movie.
	Best Rating: The best possible rating for the movie.
	Worst Rating: The worst possible rating for the movie.
	Rating: The actual rating of the movie (out of 10).
	Genre: The genre(s) of the movie.
	Duration: The duration of the movie.

3.	Sample CSV Data: The CSV file will contain data similar to this:
mathematica
Title,URL,Description,Best Rating,Worst Rating,Rating,Genre,Duration
"The Shawshank Redemption","https://www.imdb.com/title/tt0111161/","Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.",10,1,9.3,"Drama",142 minutes
"The Godfather","https://www.imdb.com/title/tt0068646/","The aging patriarch of an organized crime dynasty transfers control of his clandestine empire to his reluctant son.",10,1,9.2,"Crime, Drama",175 minutes
...
Notes
•	The script uses the IMDb Top 250 movies page, so it is subject to changes in the website’s layout. In case of failures, check the IMDb page for any structure changes.
•	The CSV file is saved to the current working directory. You can modify the script to change the file name or location as needed.
Conclusion
This script provides an easy way to gather data on the top-rated movies from IMDb and store it in a convenient format (CSV) for further analysis or personal reference.
