# Best Horror Movies Scraper

## Project Overview
This project is a web scraping application designed to extract details about the **best horror movies of all time** from the Rotten Tomatoes website. The data includes information such as the movie title, release year, ratings, director, cast, and genre. The extracted data is then stored in CSV and Excel file formats for further analysis or use.

---

## Features

1. **Web Scraping**:
   - Extracts information about top horror movies from a specific webpage.
   - Utilizes BeautifulSoup for parsing HTML content.
   
2. **Extracted Data**:
   - Movie Title
   - Release Year
   - Ratings (%)
   - Director
   - Cast
   - Genre (default set as "Horror").

3. **Data Storage**:
   - Saves the extracted data into CSV and Excel formats for accessibility and analysis.

---

## Technologies Used

- **Python Libraries**:
  - `requests`: For sending HTTP requests and fetching webpage content.
  - `beautifulsoup4`: For parsing HTML and XML documents.
  - `pandas`: For creating and managing structured data in tabular form.

---

## Workflow

### 1. Webpage Access
- The script sends a GET request to the Rotten Tomatoes editorial page for the **best horror movies**.

### 2. Data Extraction
- Parses the HTML content of the page using BeautifulSoup.
- Extracts relevant details:
  - **Title**: Extracted from the `<h2>` tag within each movie's section.
  - **Year**: Extracted from the `<span>` tag with the class `subtle start-year`.
  - **Ratings**: Extracted from the `<span>` tag with the class `tMeterScore`.
  - **Director**: Extracted from the `info director` div tag.
  - **Cast**: Extracted from the `info cast` div tag.

### 3. Data Transformation
- Cleans and organizes the extracted data:
  - Strips unnecessary characters from text.
  - Converts ratings to integers.
  - Combines cast names into a single comma-separated string.

### 4. Data Storage
- The cleaned and organized data is saved as:
  - A CSV file (`movies_info.csv`).
  - An Excel file (`movies_info.xlsx`).

---

## Usage Instructions

### Prerequisites
Ensure you have Python installed and the following libraries available:
- `requests`
- `beautifulsoup4`
- `pandas`

Install any missing dependencies using pip:
```bash
pip install requests beautifulsoup4 pandas
