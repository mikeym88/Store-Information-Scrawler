# Store Info Web Crawler

This crawler fetches data from the websites of various chains in order to get information about their store locations.
Information such as store name, phone number, operating hours, etc.

This crawler was **last run successfully in June 2020**. The crawler would need to be tested and changed on a regular 
interval to make sure it still works.

See the `results` folder for the output of the

## Notes

* For t1 was not working because the `robots.txt` was being misread. While `robots.txt` allowed the specific URL to be accessed by scrawlers, scapy did not read that correctly.
    * Workaround: set `ROBOTSTXT_OBEY` to `False` in `settings.py`
    * Further investigation needed. 

## Running the crawlers

Use the following commands to run the crawlers.

### Crawler 1:

Output as JSON file:
```
scrapy crawl towncaredental -o towncaredental.json
```

Output as CSV file:
```
scrapy crawl towncaredental -o towncaredental.csv -t csv
```

### Crawler 2

Output as JSON file:
```
scrapy crawl rickysalldaygrillcanada -o rickysalldaygrillcanada.json
```

Output as CSV file:
```
scrapy crawl rickysalldaygrillcanada -o rickysalldaygrillcanada.csv -t csv
```

### Crawler 3

Output as JSON file:
```
scrapy crawl jockey -o jockey.json
```

Output as CSV file:
```
scrapy crawl jockey -o jockey.csv -t csv
```


### Crawler 4

Output as JSON file:
```
scrapy crawl rentking -o rentking.json
```

Output as CSV file:
```
scrapy crawl rentking -o rentking.csv -t csv
```

## Resources

1.	ScraPy module for Python: <https://docs.scrapy.org/en/latest/>. Quick start-to-finish example: <https://www.codementor.io/andy995/writing-a-simple-web-scraper-using-scrapy-myb7vrmgx>
2.	XPath syntax: <https://devhints.io/xpath>. Use Google Chrome Inspector (Dev tools) to test XPath to access HTML nodes of a website; example: <https://yizeng.me/2014/03/23/evaluate-and-validate-xpath-css-selectors-in-chrome-developer-tools/>
3.	Network Log details/demo: <https://developers.google.com/web/tools/chrome-devtools/network/>
