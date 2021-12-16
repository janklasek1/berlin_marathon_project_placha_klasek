# Berlin marathon 2021 - results analysis
Final project of the IES Python course, which scrapes and analyses data from the 2021 Berlin Marathon.

In addition to the basic analysis of participants (by gender, age, nationality etc.), we get inspired by the paper from Berry (available here: https://content.iospress.com/articles/journal-of-sports-analytics/jsa205) and we look whether the difference in paces at the beginning and the end of the race differ across "performance groups". In other words we try to answer the question: "Can endurance athletes keep their pace throughout the race better than the "hobby" runners?"

This project is divided into three files:

* Scraper
  - this file aims to scrape information about each runner from his/her own result page
  - firstly, we build a list of all the pages where the results table is displayed (website allows max. of 100 results per page), then we obtain a unique link to the page of every single participant; finally we loop through each link (over 23,000) to scrape the desired data

* Cleaner
  - we extract the nationality from the name column, gender and age range (exact age is not available) from the Category and tranform times into feasible formats for the analysis (seconds/minutes)

* Analyser
  - all the final analysis, both numerical and graphical will be done in this Jupyter notebook 
