# G2_scraper
Scrap company information from g2.com, given a list of companies

## Instructions
Run g2_scraper.ipynb

## Logic
Use selenium to mimic a real user's behavior, and scrap from g2.com.
To retrieve the information needed, I maily used the XPath of the elements on g2. I simulated some behaviors to retrieve hidden information. I cleaned some unwanted information that come with that ('show less').
I saved the scraped information to a list, and transformed it to a dataframe. Then joined it with the original file.

## Known Problems
- I only got to scrape around 20 companies, before CloudFlare blocked me. I tried to bypass it using [undetected_chromedriver](https://github.com/ultrafunkamsterdam/undetected-chromedriver), but it has its own problems.
- It takes me around half an hour to scrape these 20 companies, so I didn't try to scrape all the companies from the file.
- I first scraped all the information but pricing and alternatives, the optional info. This proved to be a bad decision, because once I finished coding for scraping pricing and alternatives, CloudFlare has got his eyes on me. This caused some inconsistency in the code, but it's mainly on the output of the functions.
- Some company's 'pricing' page requires clicking on multiple 'show more' buttons, I didn't deal with this problem.
- Even though I clicked the 'show more' button on 'alternative' page, I still can't scrape all the alternatives. Besides, I chose the easy top8 alternatives over the harder top20 ;)
- Last but certainly not least, I can't find most of the companies on g2.com, and I know some of the companies I scraped from g2 are not the same companies listed in the file. I believe I can refine the solution by using only the first word of the company name, for example. But I don't think I can fix this problem.
