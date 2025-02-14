AZ Product Scraper

Overview

This Python script automates searching for products on AZ.com, extracts product details, and saves the data in CSV format. It uses Selenium for browser automation and BeautifulSoup for parsing the HTML content of the search results.

Features

Automates AZ searches for multiple keywords.

Extracts product details including:

ASIN (AZ Standard Identification Number)

Brand Name

Product Title

Price

Sponsored Status

Average Rating

Number of Ratings

Quantity Bought in the Past Month

Saves extracted data into CSV files.

Supports location setting via ZIP code.

Uses WebDriverManager to handle ChromeDriver installation automatically.

Prerequisites

Ensure you have the following installed on your system:

Python 3.x

Google Chrome

Required Python packages (install using the command below):

pip install selenium webdriver-manager beautifulsoup4

How It Works

The script opens AZ.com and sets the delivery location using a specified ZIP code.

It searches for each keyword in the search_keywords list.

It extracts product details from the search results.

The data is saved as a CSV file with the search keyword and the current date in the filename.

Usage

1. Update Search Keywords

Modify the search_keywords list in the script to specify the products you want to search for:

search_keywords = [
    "example keyword 1", "example keyword 2"
]

2. Set ZIP Code (Optional)

Modify us_zip_code if you want to specify a different location:

us_zip_code = "02118"  # Change this to your desired ZIP code

3. Run the Script

Execute the script using the following command:

python AZ_scraper.py

4. Check the Output

CSV files will be generated in the same directory as the script, named in the format:

<search_keyword>_<YYYY-MM-DD>.csv

Notes

AZ may block frequent automated searches. Use delays (time.sleep()) to avoid detection.

If AZ changes its website structure, XPath or class names may need updating.

Ensure Chrome is up-to-date for best compatibility with Selenium.

License

This project is free to use and modify. No official affiliation with AZ.

Author

[Your Name]
