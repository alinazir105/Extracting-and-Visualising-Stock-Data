# Extracting and Visualizing Stock Data

## Project Overview

This Jupyter Notebook, which is part of an assignment from IBM/Skills Network, focuses on the essential data science task of extracting, cleaning, and visualizing financial data. The project specifically extracts historical stock prices and quarterly revenue data for **Tesla (TSLA)** and **GameStop (GME)**, then displays this information in a comparative plot.

The primary goal is to extract key data from various sources and present it in a comprehensive graph to aid in data-driven decision-making.

## Key Features & Methodology

The notebook performs the following key steps:

1. **Data Extraction (Stock Prices):** Historical stock data (Date, Open, High, Low, Close, Volume) for **Tesla (TSLA)** and **GameStop (GME)** is extracted using the `yfinance` library.


2. **Data Extraction (Revenue):** Quarterly revenue data for both companies is scraped from specific financial web pages using the `requests` and `BeautifulSoup` libraries.


* The raw revenue data is cleaned by removing commas and dollar signs, and dropping null/empty values.



3. **Visualization:** A custom Python function, `make_graph`, is defined to create a two-row subplots figure.


* **Row 1:** Displays the Historical Share Price for the stock.
* **Row 2:** Displays the Historical Revenue for the company.
* The function combines the stock price data (from `yfinance`) and the revenue data (from web scraping) into a single visual dashboard.




4. **Final Output:** The `make_graph` function is invoked for both Tesla and GameStop to generate and display the final stock price and revenue dashboards.



## Data Sources

The notebook uses a combination of API access and web scraping:

| Data Type | Source | Tool Used |
| --- | --- | --- |
| **Tesla (TSLA) Stock Data** | Yahoo! Finance | <br>`yfinance`|
| **Tesla Revenue Data** | IBM Hosted Webpage (`revenue.htm`) | <br>`requests` and `BeautifulSoup` |
| **GameStop (GME) Stock Data** | Yahoo! Finance | <br>`yfinance` |
| **GameStop Revenue Data** | IBM Hosted Webpage (`stock.html`) | <br>`requests` and `BeautifulSoup` |

## Technologies & Dependencies

The project relies on the following Python libraries. If running locally, you must ensure these are installed:

* **`yfinance`**: For extracting historical stock data.


* **`pandas`**: For data manipulation and DataFrame operations.


* **`requests`**: For downloading the HTML content of the revenue pages.


* **`beautifulsoup4` (`bs4`)**: For parsing HTML and extracting table data.


* **`plotly`**: For generating the interactive, dashboard-style visualizations.


* **`warnings`**: To ignore future warnings.



#### Installation

(If running this notebook locally, the following packages are required):

```bash
# Recommended installations based on notebook content
!pip install yfinance
!pip install bs4
!pip install nbformat
!pip install --upgrade plotly

```
