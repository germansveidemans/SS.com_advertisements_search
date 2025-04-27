---

# SS.com Car Listings Scraper

This Python script automatically searches for car listings on [ss.com](https://www.ss.com/) based on user-defined parameters from a CSV file, extracts key data from the listings, and saves the results into an Excel file.

---

## Features

Fills in search fields on ss.com using input from `options.csv`.

Extracts:
- Car brand and model
- Year of manufacture
- Engine displacement
- Mileage
- Price
- Direct link to the listing

Handles missing mileage values gracefully.

Saves results into a well-structured Excel file (`result.xlsx`), with separate sheets for each search query.

---

## Project Structure

- `options.csv` — A CSV file containing search parameters (price range, year range, engine size, etc.)
- `result.xlsx` — The resulting Excel file containing the scraped listings.
- `scraper.py` — The main script.

---

## Requirements

- Python 3.x
- Google Chrome browser
- ChromeDriver (compatible with your Chrome version)

### Python Libraries:

Install the required libraries using:

```bash
pip install selenium openpyxl pandas
```

---

## Usage

1. Prepare your `options.csv` file with the following columns:
   ```
   Price Range (e.g., 1000-5000), Year Range (e.g., 2005-2015), Engine Size (e.g., 1.6-2.0), Engine Type, Gearbox Type, Body Type, Color
   ```

2. Make sure you have the correct version of ChromeDriver installed and added to your system PATH.

3. Run the script:

```bash
python scraper.py
```

4. The script will:
   - Open ss.com
   - Perform searches based on each row in `options.csv`
   - Collect the data
   - Save the results in `result.xlsx`, with one sheet per query.

---

## Notes

- **Delays**: There is a 2-second delay (`time.sleep(2)`) between searches to avoid being blocked by the website.
- **Website Structure**: If ss.com updates their website layout, the script might require updates in element locators.
- **Language**: The website is in Latvian; the script uses the site's Latvian field IDs.

---

## Example

Sample `options.csv`:

| Price Range | Year Range | Engine Size | Engine Type | Gearbox Type | Body Type | Color |
|-------------|------------|-------------|-------------|--------------|-----------|-------|
| 2000-5000   | 2005-2012   | 1.6-2.0     | Benzīns     | Mehāniska    | Sedans    | Melns |


---

## Author
-Developer: German Veideman

---
