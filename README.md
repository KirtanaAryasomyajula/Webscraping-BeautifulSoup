# Webscraping-BeautifulSoup
Used Car Data Web Scraping Project
Overview
This project scrapes used car data from the Cars24 website for Mumbai, focusing on five car brands: Hyundai, Tata, Honda, Renault, and Ford. The goal is to collect 25 data points (5 models per brand) with details such as car name, model year, kilometers driven, fuel type, transmission type, price, and location. The data is processed, cleaned, visualized, and saved as a CSV file for analysis.
Objectives

Scrape car data from Cars24 using web scraping techniques.
Clean and structure the data into a pandas DataFrame.
Visualize key insights (e.g., price vs. kilometers driven, location distribution).
Save the cleaned data as a CSV file.

Tools and Libraries

Python: Programming language used for scripting.
BeautifulSoup: For parsing HTML content from web pages.
requests: To fetch web pages via HTTP requests.
pandas: For data manipulation and storage.
seaborn/matplotlib: For data visualization.
Jupyter Notebook: For interactive development and documentation.

Data Description
The dataset includes 25 entries with the following columns:

CarName: Model name (e.g., Hyundai Xcent, Tata Tiago).
Model_Year: Year of manufacture (e.g., 2014).
Kilometers_Driven: Distance driven in thousands of kilometers (e.g., 90.17).
Fuel_Type: Petrol, Diesel, or CNG.
Transmission_Type: Manual or Auto.
Price: Price in lakhs (e.g., 3.15).
Location: Specific location in Mumbai (e.g., Goregaon).

Methodology

Web Scraping:
URLs for each brand are defined for Mumbai listings on Cars24.
The requests library fetches HTML content, and BeautifulSoup parses it to extract car details.


Data Cleaning:
Numerical columns (Kilometers_Driven, Price) are converted to float.
Missing or invalid data is handled (if any).


Data Visualization:
Bar plot for location distribution.
Scatter plot for Price vs. Kilometers Driven.


Data Storage:
The cleaned DataFrame is saved as cars.csv.



Files

Webscrape(cars24).ipynb: Jupyter Notebook with the scraping, cleaning, and visualization code.
cars.xls/cars.csv: Input and output datasets containing the scraped car data.

Setup and Installation

Install required libraries:pip install requests beautifulsoup4 pandas seaborn matplotlib


Run the Jupyter Notebook:jupyter notebook Webscrape(cars24).ipynb


Ensure internet access for web scraping.

Usage

Open the notebook and execute cells sequentially to scrape data, clean it, generate visualizations, and save the CSV.
Modify URLs in the notebook to scrape data for other cities or brands.

Results

Dataset: 25 cars (5 per brand) with details like model, year, price, etc.
Visualizations:
Location distribution shows popular areas like Goregaon and Dombivli East.
Scatter plot indicates no strong correlation between price and kilometers driven.


Output: cars.csv contains the cleaned dataset.

Limitations

The code does not handle dynamic content (e.g., JavaScript-rendered pages), which may require selenium.
Pagination is not implemented, limiting data to the first page of listings.
Error handling for failed requests or missing data is minimal.

Future Improvements

Use selenium for dynamic content scraping.
Implement pagination to collect more data.
Add error handling and data validation.
Include additional attributes (e.g., number of owners, car features).

Author
Developed as part of an internship project for web scraping and data analysis.
