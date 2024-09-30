# Amazon web scrapper 
 
This notebook is designed to scrape product details from Amazon, process the collected data, and merge multiple CSV files into one. It uses Selenium to interact with the Amazon web pages, extracting various product attributes, and then processes the data using Pandas.

## Prerequisites

1. **Python 3.x**
2. **Selenium WebDriver**: Used to automate browser actions.
   - Install with: `pip install selenium`
   - Requires a compatible web driver (e.g., ChromeDriver for Chrome).
3. **Pandas**: Used for data manipulation and processing.
   - Install with: `pip install pandas`
4. **Web Driver**: Ensure you have the appropriate web driver installed and accessible in your system's PATH.

## Notebook Overview

### Sections

1. **Setup and Initialization**:
   - Importing necessary libraries like `Selenium`, `Pandas`, and others.
   - Configuring the WebDriver for browser automation.

2. **Scraping Product Details**:
   - The notebook uses XPaths and CSS selectors to scrape Amazon product information.
   - Key attributes scraped include:
     - Product title
     - Description
     - Reviews
     - Ratings
     - Price (before and after any promotions)
     - Available colors
     - Number of purchases in the last month
     - Other specific details like embellishments, water resistance, etc.

3. **Error Handling**:
   - If an element is not found (due to variations in product pages), the script handles `NoSuchElementException` and logs `None` for that attribute.

4. **Saving Data**:
   - Each product's data is stored in a dictionary and later written into CSV files for further analysis.

5. **Merging CSV Files**:
   - The notebook includes functionality to merge CSV files (like `smartphones.csv`, `chargers.csv`, `headphones.csv`, and `cases.csv`) into a single file called `combined_products.csv`.

6. **Closing Browser**:
   - The notebook ensures that the browser is properly closed at the end of the scraping process to free resources.

### Output

- The primary output is a CSV file `combined_products.csv` that contains merged data from different product categories.

## How to Use

1. **Run the Notebook**:
   - Ensure all prerequisites are installed.
   - Set up the appropriate web driver (like `ChromeDriver` or `GeckoDriver`).
   - Start the notebook and execute the cells sequentially.

2. **Adjusting the Scraper**:
   - You can modify the XPath or CSS selectors if the structure of Amazon product pages changes.
   - Update the list of product categories or files you wish to scrape and merge in the relevant sections.

3. **Merging Data**:
   - If you add more product categories or CSV files, ensure the filenames are included in the list under the merging section.
  
## Potential problems while running

- Amazon's html structure regularly changes thus any code using Xpath may break to fix this problem try and locate the element which is causing the problem using your browser's element inspector and copy the new Xpath in the place of the old one
