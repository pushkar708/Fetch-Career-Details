# 💼 Naukri.com Job Scraper

This Python script automates the process of scraping job listings from [Naukri.com](https://www.naukri.com), specifically targeting **Software Developer** roles with 2 years of experience and salary expectations between 6–10 LPA.

The collected data includes job titles, companies, experience, salary, location, descriptions, qualifications, post date, and job URLs — all stored in a structured Excel file.

---

## 📌 Features

- 🔎 Automatically scrapes multiple pages of job results.
- 💾 Saves detailed job information in a clean Excel spreadsheet.
- 🔗 Collects direct job URLs for easy access.
- ♻️ Appends new data to existing Excel file if already present.
- ✨ Clean and maintainable code with XPath-based element location.

---

## 📂 Output: `job_information.xlsx`

The data is saved with the following columns:

| Job Name | Provider | Experience Required | Salary | Location | Description | Qualifications | Posted On | Job URL |
|----------|----------|----------------------|--------|----------|-------------|----------------|-----------|---------|

---

## ⚙️ Requirements

### 🐍 Python Packages

Install the required libraries using pip:

```bash
pip install selenium openpyxl pyautogui
```

### 🌐 Setup Browser & WebDriver

- **Google Chrome** – Install the latest version.
- **ChromeDriver** – Must match your Chrome version  
  [Download ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads)

Ensure `chromedriver` is added to your system's **PATH** or placed in the script's directory.

---

## 🚀 How to Run

1. Clone or download this script.
2. Ensure all dependencies are installed.
3. Run the script:

```bash
python naukri_job_scraper.py
```

4. The script will:
   - Visit multiple pages of job listings.
   - Extract relevant job details.
   - Save or update `job_information.xlsx` in the current directory.

5. ✅ Done! Open the Excel file to view the scraped data.

---

## 🔧 Customization

- To modify the search filters (like job role, experience, salary, or freshness), edit the URL in this line:

```python
temp_url = f"https://www.naukri.com/software-developer-jobs?k=software%20developer&nignbevent_src=jobsearchDeskGNB&experience=2&ctcFilter=6to10&jobAge=15"
```

- To run without opening a browser window, enable **headless mode**:

```python
chrome_options.add_argument("--headless")
```

- To scrape more or fewer pages, adjust this line:

```python
for page_number in range(1, 7):  # Change 7 to desired number of pages + 1
```

---

## 🛑 Disclaimer

- This script is for **educational and personal use only**.
- Frequent scraping may violate the terms of service of Naukri.com.
- Use responsibly and avoid spamming the platform.

---

## 📃 License

This project is open-source and available under the **MIT License**.

---

## 🙋‍♂️ Author

**Wolfie Crypto**  
Built using Python, Selenium & Excel automation
