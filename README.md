# Web_Scraper
🌐 Zimbabwe Job Scraper
This project is a Python web scraper that automatically collects job postings from vacancymail.co.zw daily and stores them in a CSV file for further analysis or tracking.

📋 Features
Fetches job listings from vacancymail.co.zw

Parses and extracts:

Job Title

Company Name

Job Description

Appends results to a CSV file

Logs errors and actions for debugging

Runs automatically every day at midnight

🛠️ Requirements
Python 3.x

Install required packages:

bash
Copy
Edit
pip install -r requirements.txt
requirements.txt
txt
Copy
Edit
requests
beautifulsoup4
pandas
schedule
🧠 How It Works
Fetches the webpage using the requests library.

Parses HTML using BeautifulSoup.

Extracts job details such as title, company, and description.

Saves job data into a CSV file named scraped_data.csv.

Logs activity and errors in scraper.log.

Schedules the scraping to run every day at midnight.

🚀 Usage
To run the scraper once:

bash
Copy
Edit
python your_script_name.py
To run the scheduled scraper daily:

bash
Copy
Edit
python your_script_name.py
⚠️ Make sure the script stays running (e.g., use a task scheduler like cron, pm2, or a long-running environment).

📁 Output Files
scraped_data.csv – Contains all scraped job data.

scraper.log – Tracks script activity and logs any errors.

📝 Customization
You can change the scraping schedule by modifying this line in the code:

python
Copy
Edit
schedule.every().day.at("00:00").do(scrape_jobs)
For example, to scrape at 6 AM:

python
Copy
Edit
schedule.every().day.at("06:00").do(scrape_jobs)
🔒 Disclaimer
This scraper is for educational and personal use. Please ensure you follow the website’s terms of service and robots.txt file.

