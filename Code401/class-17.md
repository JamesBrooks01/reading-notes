# Reading Assignment 17

## Web Scraping

---

### Web Scrape with Python in 4 minutes

- Web scraping is a technique to access and extract large amount of data from a website, often saving time and effort.
- Two important things to keep in mind;
  - Read the Terms and Conditions to ensure you legally can use the data, often commercial use is prohibited
  - Don't download data at too rapid a pace as it could break the website or you could be blocked from the site.
- The first step is to inspect the website to determine where in the HTML is the information you want.
- Next, you import the relevant libraries, `requests`, `urllib.request`, `time`, and `BeautifulSoup` from `bs4`
- Next you set the URL for the website and use the requests library to access it.
- Then parse it with BeautifulSoup and use soup to find all the tags you need.

---

### How to scrape websites without getting blocked

- Web Scraping is a task to be done responsibly to avoid having a detrimental effect on the site.
- The computer can retrieve data faster and in greater depth than a human so it can have an impact on the performance of the site.
- Some sites have anti-scraping mechanisms and some have measures to block scraping because an a closed data access belief.
- The best practices for scraping are;
  - Respect Robots.txt
  - Make the crawling slower, do not slam the server, treat websites nicely
  - Do not follow the same crawling pattern
  - Make requests through Proxies and rotate them as needed
  - Rotate User Agents and corresponding HTTP Request Headers between requests
  - Use a headless browser like Puppeteer, Selenium or Playwright
  - Beware of Honey Pot Traps
  - Check if Website is Changing Layouts
  - Avoid scraping data behind a login
  - Use Captcha Solving Services
  - How can websites detect web scraping?
  - How do you find out if a website has blocked or banned you?
- The most basic rule is to "Be Nice"

---

### Track Amazon Prices

- A basic app that checks the price of an amazon item and sends an email if the price falls to a certain point.
- Has some interesting ideas and implements a real-world usage for it that other people can use.
