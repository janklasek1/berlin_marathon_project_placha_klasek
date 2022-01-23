### Scraper
This notebook downloads all the required info about each runner. BeatifulSoup package together with Pandas tools is used.

The code proceeds in the following way:

- Builds a set of links that each displays a table of 100 runners (maximum per page)

- From the list of links created above get all the links directing to the unique result page of each runner

- Loop through the links (over 23,000, expected download time of about 3 hours) to get scrape all the required fields

- Transform the table created above as the Pandas dataframe and save it as .csv file for the future use

