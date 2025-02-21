# Basic Git Scraper Template

**Author: Fiona Jiang**

This is a basic scraper for [The Daily Pennsylvanian]](https://www.thedp.com/). \

The changes I made are for extracting headlines from the News, Sports, and Opinion sections of The Daily Pennsylvanian website.  
The approach I used is to study the structure of the website and locate every section first using Inspect. Then, I coded each part separately.  

First, the script locates the News section by searching for a `<div>` with the class `"col-sm-6 section-news"`. If found, it extracts the first article link and saves it under `"News"`.  
Next, it searches for additional sections with the class `"col-sm-6"`, retrieving all possible Sports and Opinion sections.  

For each section, the script identifies its title (e.g., "Sports" or "Opinion") by looking for an `<h3>` tag with the class `"frontpage-section"`. If a match is found, it extracts the first article link from a `<div>` with the class `"article-summary"`. The link is then stored under the appropriate category in the dictionary.  
