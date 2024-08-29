Google Maps Data Scraper
Overview
This project is a Python script that uses Playwright to scrape business information from Google Maps. It extracts the following data points for each business:

Name: The name of the business.
Address: The address of the business.
Website: The website of the business (if available).
Phone Number: The phone number of the business (if available).
Reviews Count: The number of reviews the business has received.
Reviews Average: The average star rating of the business.
Latitude: The latitude coordinates of the business.
Longitude: The longitude coordinates of the business.
Working Hours: The working hours of the business.
Plus Code: The Plus Code of the business (if available).
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/google-maps-scraper.git
cd google-maps-scraper
Create and activate a virtual environment (optional but recommended):

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Make sure your requirements.txt includes:

text
Copy code
playwright
pandas
Install Playwright browsers:

bash
Copy code
python -m playwright install
Usage
Command-Line Arguments
-s, --search: The search term to query in Google Maps. This is mandatory unless you provide an input.txt file.
-t, --total: The total number of businesses to scrape per search term. Default is 3.
Running the Script
You can run the script in two ways:

Using command-line arguments:

bash
Copy code
python main.py -s "Unites States Boston dentist" -t 3
Using an input file:

Create an input.txt file in the same directory with search terms, one per line.
Run the script without the -s argument:
bash
Copy code
python main.py -t 5
Output
The scraped data is saved in the output directory in both CSV and Excel (.xlsx) formats. The files are named based on the search term used, e.g., google_maps_data_Unites_States_Boston_dentist.csv.
Example
If you want to scrape data for dentists in New York and Boston, you can use the following commands:

bash
Copy code
python main.py -s "Unites States New York dentist" -t 5
python main.py -s "Unites States Boston dentist" -t 5
This will create two files in the output directory:

google_maps_data_Unites_States_New_York_dentist.xlsx
google_maps_data_Unites_States_Boston_dentist.xlsx
Notes
The script uses a headless Chromium browser by default. You can modify the script to run in headful mode (with a visible browser window) by changing the headless option in the main.py script to False.
Be aware of Google's terms of service regarding scraping.
License
This project is licensed under the MIT License. See the LICENSE file for more details
