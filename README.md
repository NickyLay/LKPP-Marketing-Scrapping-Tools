Here’s the `README.md` formatted for GitHub:

---

# e-Katalog LKPP Scraper

A Python-based scraper designed for extracting product information from the [e-Katalog LKPP](https://e-katalog.lkpp.go.id/), streamlining shopping documentation and enabling easy access to product data. This script utilizes Selenium and BeautifulSoup to collect product details like name, price, supplier, image URL, and other attributes.

## Requirements

- Python Version: 3.7.3
- Installation:
  Install dependencies using the following command:
  ```bash
  pip install -r requirements.txt
  ```

Contents of `requirements.txt`:
```plaintext
csvkit==1.3.0
selenium==4.8.0
future==0.17.1
requests==2.28.2
m2w64-libwinpthread-git==5.0.0.4634.697f757
bs4==0.0.1
beautifulsoup4==4.11.1
```

## Setup

1. Prepare URL File:
   - Create a file named `url.txt` with each URL you want to scrape on a new line.
   - Example:
   https://e-katalog.lkpp.go.id/id/search-produk?authenticityToken=ee1e759079d2efde329e95f85d133c09dab8dd52&q=cpr+simulator&prid=&pid=&gt=&lt=&mid=&kbid=&order=&cat=, cprsimulator
   https://e-katalog.lkpp.go.id/id/search-produk?authenticityToken=ee1e759079d2efde329e95f85d133c09dab8dd52&q=vein+viewer&prid=&pid=&gt=&lt=&mid=&kbid=&order=&cat=, veinviewer
   https://e-katalog.lkpp.go.id/id/search-produk?authenticityToken=ee1e759079d2efde329e95f85d133c09dab8dd52&q=spine+system&prid=&pid=&gt=&lt=&mid=&kbid=&order=&cat=, spinesystem
   
2. Download ChromeDriver:
   - Download ChromeDriver compatible with your Chrome version from the [ChromeDriver official page](https://sites.google.com/chromium.org/driver/downloads?authuser=0).
   - Specify the path to `chromedriver.exe` in the `chromedriver_path` variable in the script.

3. Run the Scraper:
   Execute the script with:
   ```bash
   python ch6.py
   ```

## Script Overview

The script performs the following steps:

1. Data Extraction:
   - Collects product details using BeautifulSoup to parse HTML content. .

2. CSV Output:
   - Saves extracted data into `output.csv` with the following columns:
     - `Nama Produk`: Product name
     - `Harga`: Price
     - `TKDN`: TKDN
     - `BMP`: BMP
     - `TKDN+BMP`: TKDN + BMP
     - `Nomor Izin Edar`: Product name
     - `Supplier`: Supplier name
     - `URL`: Product page URL
     - `URL Gambar`: Image URL
     - `Headings and Descriptions`: Product attributes and descriptions
     - `Produk ID`: Unique product identifier
