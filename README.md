# Automated-Web-Scraper-for-Tasiş-

# Tasiş Auction (e-ihale) Data Scraper

A specialized web automation tool designed to monitor and filter listings on the Turkish Government's e-ihale (Tasiş) platform. The bot streamlines the process of finding specific "niche" opportunities based on category and budget constraints.

## Key Features
- **Smart Filtering:** Targets specific categories and price ceilings directly via dynamic URL parameters.
- **Bot Detection Bypass:** Implements custom Chrome options and User-Agents to mimic human behavior and bypass automation flags.
- **Automated Pagination:** Systematically crawls through multiple result pages without manual input.
- **Formatted Reporting:** Exports all found listings into a professional Excel (.xlsx) file with auto-adjusted columns and text wrapping for easy analysis.

## Tech Stack
- **Python 3.x**
- **Selenium:** For dynamic web crawling and DOM interaction.
- **Pandas:** For data structuring and management.
- **Openpyxl:** For advanced Excel formatting and styling.

## How It Works
1. The script initializes a headless-capable Chrome instance with anti-detection arguments.
2. It calculates pagination based on the `skipCount` and `maxResultCount` parameters.
3. For each listing found, it visits the detail page to extract titles, starting bids, and description bodies.
4. Finally, it cleans the data and generates a formatted report (`tasis_nis_firsatlar.xlsx`).

## Usage
- Configure your target `KATEGORI_ID` and `MAX_FIYAT` in the script.
- Ensure you have the corresponding `chromedriver` installed.
- Run the script: `python main.py`

*Note: This tool is intended for personal data analysis purposes only.*
