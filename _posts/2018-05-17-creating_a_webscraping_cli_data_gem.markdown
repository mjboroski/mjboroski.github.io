---
layout: post
title:      "Creating a Webscraping CLI Data Gem"
date:       2018-05-17 17:14:19 +0000
permalink:  creating_a_webscraping_cli_data_gem
---


This project was my largest undertaking thus far. I found out where my weaknesses were and gained clarity on the creation process. I had to get more familiar with Github before i could really gain any ground. The programming method I used was initially inside-out, but I found that I preferred working outside-in.  

First, I scaffolded out a new ruby gem project and pushed it to github. I then proceeded to build a basic file structure. From there, I began creating a rudimentary CLI. I chose to categorize the Articles by Website and the Websites within the main CryptoNews class. Once the CLI was up and running, i had to begin scraping.

Using Nokogiri to scrape these webpages proved more challenging than I thought it would be. I learned to be very specific in my scraping criteria, as I got hung up on a slight detail in my search parameter. I ended up putting site-specific methods in my Website class to scrape the respective webpages. I then directed each webpage to identify itself and use only the appropriate method for that site. This way, I could structure the scraper directly inside the Website class to collect from each website with specific instructions.

Overall, I found this project led me to find a groove in my coding. I developed a workflow and learned to keep moving, one step at a time. I began using the "rake console" command the way I should have been using it all along, as the information gleaned is invaluable to efficient progress. I took a page from Avi and put a "reload!" command in my rakefile to save time. I look forward to learning many more useful tricks like this as I journey ahead.
