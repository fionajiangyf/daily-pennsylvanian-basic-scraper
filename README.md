# Basic Git Scraper Template

**Author: Fiona Jiang**

This is a basic scraper for [The Daily Pennsylvanian]](https://www.thedp.com/). \

The changes I made are for extracting headlines from the News, Sports, and Opinion sections of The Daily Pennsylvanian website.  
The approach I used is to study the structure of the website and locate every section first using Inspect. Then, I coded each part separately.  

First, the script locates the News section by searching for a `<div>` with the class `"col-sm-6 section-news"`. If found, it extracts the first article link and saves it under `"News"`.  
Next, it searches for additional sections with the class `"col-sm-6"`, retrieving all possible Sports and Opinion sections.  

For each section, the script identifies its title (e.g., "Sports" or "Opinion") by looking for an `<h3>` tag with the class `"frontpage-section"`. If a match is found, it extracts the first article link from a `<div>` with the class `"article-summary"`. The link is then stored under the appropriate category in the dictionary.  

## Schedule Explanation
The initial cron expression `0 5,22 * * *` means my job runs at **5:00 AM and 10:00 PM UTC every day**. The five fields are:  

- **Minute (`0`)** → The job runs at the start of the hour (0 minutes past).  
- **Hour (`5,22`)** → The job runs at **5 AM and 10 PM UTC**.  
- **Day of Month (`*`)** → The job runs **every day** of the month.  
- **Month (`*`)** → The job runs **every month**.  
- **Day of Week (`*`)** → The job runs on **every day of the week**.  

