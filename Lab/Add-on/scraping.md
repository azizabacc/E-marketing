# Scraping

* Type : Solo
* Duration : Tbd...

![](https://media.giphy.com/media/3osxYc2axjCJNsCXyE/giphy.gif)

## What

So what is scraping?

Data scraping, content scraping, web scraping, you've probably already heard these terms, so what does it mean?

If we stick to the literal translation of the word, it is data extraction.

You can extract any type of data, search engines, rss feeds, public information, many sites make their data available to be collected.

This data is not always available.
Generally, scraping can be done simply by using an api, when it is available, you can use it to collect this data, it's like having a direct bridge to get there.

But, this is not always the case, some websites do not have an api available and sometimes, even if it does, you can't always get the data in the right format.

This is where scraping comes in.

### Legal

So, it brings some questions, is it legal ? Are there any restrictions?

From a certain point of view, scraping can look like stealing, nevertheless, it's a bit of a grey area, there is nothing completely illegal with scraping, when a site publishes data, they are generally available to the public and therefore, they are free to be exploited.

There are many tools or extensions, which use Amazon for example to retrieve data related to certain products to retrieve their price and find the best deals for example.

But, because there is a but, not all data is intended for the public, personal data, intellectual property, scraping can quickly become malicious.

![](https://pix4free.org/assets/library/2021-07-20/originals/law.jpg)

### The framework

Malicious scraping is a web extraction of data that the publisher did not intend to share or did not consent to. This can lead to sanctions as with the DMCA (https://en.wikipedia.org/wiki/Digital_Millennium_Copyright_Act) for example.

But there is a grey area, indeed, many data are protected by the rgpd, the various laws for the protection of consumers, but not all, which means that there is no illegality to extract them, after all, they have been made public by the host and there is therefore nothing illegal to dispose of them.

Nevertheless, even if it is technically legal and even if it is often due to the lack of supervision of the host, it can quickly be used in a malicious way or in any case, not very ethical. This is why scraping has a somewhat dubious reputation.

In another perspective, over-scraping is also a malicious practice, the principle is simple, you send too many requests in a given time and the hosts do not appreciate that their resources are dedicated to scraping robots rather than to these users.

Scraping is therefore not illegal, but the reuse of scraped data, as is or after transformation, may have a more complex legal context.

So, in concrete terms, for the use of scraping, remember 2 things:

- You have to be sure that the data is for public use
- Do it sparingly

## How

Web scraping may seem complicated, but it is actually very simple.

Even though methods and tools may vary, there are only 2 steps, find a way to automatically crawl the targeted websites (**crawlers**) and extract the data once done (**scrapers**).

### Basic process

Ok, in practice and in a very basic way, here is the breakdown: 

Crawl: 
- Specify Url with HTML request

Scrap: 
- Use a tool (like regex) to extract the info
- Store the info (json, csv, xml...)

### Challenge

**Make your own tool (project) to understand the mechanics of scraping**

I won't insult you by describing each of these steps, as you will have understood, there is nothing very complicated about it.

If needed, you will find a lot of resources to help you.

- Python : [How to use scraping with python, geeksforgeeks](https://www.geeksforgeeks.org/what-is-web-scraping-and-how-to-use-it/)
- Node.js : [Scraping with node.js, freecodecamp](https://www.freecodecamp.org/news/how-to-scrape-websites-with-node-js-and-cheerio/)
- PHP : [Web scraping php, welovedevs](https://welovedevs.com/fr/articles/web-scraping-php/)

### Limits

Of course the above examples are very simple to set up and will serve you to make a small sample, nevertheless, in reality, you will quickly be confronted with certain limits if you want to use scraping on a large scale.

**Keeping the scraper up to date:** This seems obvious but it is much more restrictive than you might think, websites often change their presentation and therefore their structure, you have to consult your targets and modify your calls quite often or adopt anti-scraping measures which we will talk about now

**Anti-scraping measures:** As we have seen before, whether it is for justified reasons or not, web hosts will tend to limit scraping (sometimes too much), here is a small check of the measures used to block extractors and the solutions to bypass them, when possible or necessary.

- IP blocking: the first and most commonly used measure is IP blocking.
- User agent filtering: apart from IP, hosting companies can also filter user agents, they can block certain versions, certain locations, certain types of requests...
- Traps: Captcha, Honeypot, ..., the techniques are different but the goal is the same, filter humans and robots to derive the navigation and / or collect the ip / agents to block them.
- Robots.txt config: if the content is not indexed, it is because the host does not want to share this data publicly.

As a countermeasure, for the IPs, you will inevitably quickly understand that you can use a [Vpn](https://en.wikipedia.org/wiki/Virtual_private_network) or a [proxy](https://en.wikipedia.org/wiki/Proxy_server) to bypass the problem.

For filtering and traps, there are some solutions ([Captcha check](https://www.octoparse.fr/blog/comment-resoudre-les-captcha-lors-du-web-scraping), [Headless](https://fr.wikipedia.org/wiki/Navigateur_headless),...), however, they all require you to visit your targets regularly in order to identify the blocking (structure change, traps, link...) and the way to bypass it.

For robots.txt, we are in another context, if the host does not want to index this content and make the data public, then you should not use them and by extension, I remind you that if you use scraping responsibly and ethically, you will not need to bypass these measures too often... Stay ethical! (parsimony & public use)

If for some **good** reason you are facing some kind of limitation (content generated in javascript, for example), I advise you to use a tool like [puppeteer](https://pptr.dev/) (simple and efficient) for all strat with a headless browser, I also add some links to alternatives below.

Same as in the previous chapter :

**Make your own tool (project) to understand the use of a tool like puppeteer**.

### Other tools

If you don't have time or not immediately, or if you want to check a new tool, I also propose you some "fast and serious" to test, you will find other alternatives in the part "resources and tools" if needed.

- Framework Scrapy : https://scrapy.org/
- Selenium : https://www.selenium.dev/
- Zapier : https://zapier.com
- Extension : [Data Scraper](https://chrome.google.com/webstore/detail/data-scraper-easy-web-scr/nndknepjnldbdbepjfgmncbggmopgden), ...

**That's it !**
