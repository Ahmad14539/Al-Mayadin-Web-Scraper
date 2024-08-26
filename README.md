# Al Mayadeen News Scraper and API

This project is a web scraping and API development solution for scraping news articles from the Al Mayadeen website, storing them in a MongoDB database, and exposing the data through a RESTful API built with Flask.

## Project Overview

The project consists of three main components:

1. **Web Scraper (`web_scraper.py`)**: This script fetches article URLs from a sitemap, scrapes content from those articles, and saves the data in JSON format.
2. **Data Storage (`data_storage.py`)**: This script loads the scraped JSON data into a MongoDB database.
3. **Flask API (`app.py`)**: This Flask application exposes various endpoints to query and analyze the stored articles.

## File Structure

- `web_scraper.py`: Contains the logic for scraping the Al Mayadeen website, processing the sitemaps, and storing articles as JSON files.
- `data_storage.py`: Connects to a MongoDB database and inserts the scraped articles from the JSON files.
- `app.py`: Implements a Flask web server with multiple endpoints to interact with the data stored in MongoDB.

## Setup and Installation

### Prerequisites

- Python 3.x
- MongoDB server running locally on `mongodb://localhost:27017/`
- Required Python packages listed in `requirements.txt`
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Running the Project:

**1. Scrape Articles**: Run the web_scraper.py script to scrape articles from Al Mayadeen.
``` python web_scraper.py ```

**2. Store Data in MongoDB:** 
Run the **data_storage.py** script to load the scraped JSON data into MongoDB.
```python data_storage.py```

**3. Start the Flask API:**
Run the **app.py** script to start the API server.
```python app.py```

The API will be accessible at **http://127.0.0.1:5000/**

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
# API Endpoints
**Here are some of the available API endpoints:**

**/top_keywords:** Get the top 10 most frequent keywords.
**/top_authors:** Get the top 10 most frequent authors.
**/articles_by_date:** Group articles by their published date.
**/articles_by_language:** Group articles by language.
**/articles_by_keyword/<keyword>:** Get articles containing a specific keyword.
**/articles_by_author/<author_name>:** Get articles written by a specific author.
**/articles_with_video:** Get articles that have a video attached.
**/articles_by_year/<year>:** Get articles published in a specific year.

Refer to the app.py file for more available endpoints and their usage.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Example Usage

**1. Fetching top keywords:**
```curl http://127.0.0.1:5000/top_keywords```

**2. Fetching articles by a specific keyword:**
```curl http://127.0.0.1:5000/articles_by_keyword/economy```

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Contributing**
Contributions are welcome! Please fork the repository and submit a pull request for review.

**License**
This project is licensed under the MIT License. See the LICENSE file for more details.

