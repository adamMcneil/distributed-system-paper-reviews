# Sprinter: Speeding Up High-Fidelity Crawling of the Modern Web
## Summary
This paper is about a more efficient way to crawl the internet.
Web crawl refers to programmatically looking at web pages for a task.
The paper says that research in this area has decreased, but they point out that there is still a lot of room for improvement in the field.
There are two ways to crawl the internet.
There is a browserless method and a browser method.
The browser method is good for ui and users but it is slow when crawling the web.
Sprinter combines both browser and browserless versions of searching the web.
They also backup their claim for more research with the fact that web search engines, smart assistants, generative AI and web archives all rely on a for of webcrawling.

The traditional way of crawling the web would be downloading the html of the website and searching for imbed links to other web pages.
The algorithm would then recursively search all of the other links.
This could be deployed across multiple machines.
The speed of this approach is limited by the network bandwidth of the machines.
A limitation of this approach would be that it only works on static web pages.
However many webpages are dynamically generated and web browsers are needed to search the dynamically generated links.
This version of web crawling with browsers is an order of magnitude slower than static crawling.
- 1. It tries to minimize the amount of JS code that is executed. It does this by reusing the output of the script on a previous run file.
- 2. It combines browser and browserless methods and has checked it ensure that the page can be read in a browserless fashion.
- 3. It careful picks what order to search the web pages to increase the number it can read staticatically.
It was implemented in Go.


## Pros
- able to crawl 50000 webpages across 100 sites.
- it was also able to crawl 5 times faster than typically dynamic crawlers.
- compares network CPU and Disk usage

## Cons
- web browsers are very complex and difficult to maintain.

## Other Comments
I am courisos how these researches meet to do their research becausre they are four authors and three schools repesent all across the country.
This is a well-written paper with a lot of practical applications.

