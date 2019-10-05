---
layout: post
title:      "CLI Travel Gem..."
date:       2019-10-04 22:43:27 -0400
permalink:  cli_travel_gem
---

![](http://media.giphy.com/media/FTELxTvVLJqRq/giphy.gif)

It's finally time to use the skills I have learned to build a project from scratch. 

The details of the CLI would include the following: 
1. Provide data from website via scraping 
2. Have a workable user interface (Welcome message) 
3. Have the ability to go two levels 
4. Refractured code 

From the moment I heard about this, I wanted to start my first project based off of travel. 

![](http://media.giphy.com/media/BpUf33t5khgVq/giphy.gif)

This CLI interface would provide the user all the top attractions in New York City.(The-Big-Apple) 
The user would be able to pick which attraction they want to travel to. 
The interface would include the following: 
1. Highlights 
2. Location
3. Contact information

One of the biggest obstacles in this project was finding a website that was not javascript heavy and that had lots of classes. After searching I finally found citypass.com! The website had exactly what I was looking for in terms of classes and even had listed items making my job easier. 



![](http://media.giphy.com/media/YTbZzCkRQCEJa/giphy.gif)

**Scraping**

Scraping at first can be challenging. I found that the more that I practiced it the easier that it got. Also, learning a bit of html helped me to understand the layout and scructure of a webpage. I'm going to say this time and time again "PRY" is your bestfriend! The ability to be able to pull on specific information and find out what index they are at made my work less stressful.  

After I ran my tests what I found was that my CLI gem was pulling more information than I needed. A bit stressful at first until I realized I could check the indexes to figure out which exact piece of data I was looking for. Below is a brief example of me using the index to gather the correct information and refracturing my code. 



	html = open(CITYPASS_URL+attraction.url)
	doc = Nokogiri::HTML(html)
	attraction.highlights = doc.css(".accordion-content.js-accordion-content")[0].text
				attraction.location = doc.css(".indent-block.icon-location").text
	attraction.contact = doc.css(".indent-block.icon-phone").text
	end 
	

This was grabbing the information from my second scraper that gathered the individual information out of my webpage.
After hours of figuring out which site to scrap, debugging with pry, countless error messages and pulling the wrong data! I can officially say I have completed my first project!. 

![](http://media.giphy.com/media/FZKg2f6KjzkhW/giphy.gif)

I want to thank all the instructors including my cohort leads that have been amazing! They continued to help me when I hit roadblocks. Thank you all for pushing me to my limits and making me a better programmer. Next stop Sinatra!













