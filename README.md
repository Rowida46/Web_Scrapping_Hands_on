



## Requests

<img width = 150 align= "left" src= "https://docs.python-requests.org/en/latest/_static/requests-sidebar.png">

[Requests](https://docs.python-requests.org/en/master/) is the most straightforward HTTP library that supports the entire restful API with all its methods `PUT`, `GET`, `DELETE`, and `POST`. It allows the user to sent requests to the HTTP server and GET response back in the form of HTML or JSON response. It also allows the user to send POST requests to the server to modify or add some content.


It's a good idea to maintaine and use __web scraping seesion__ with requests, to persist the cookies and other parameters. It can result into a performance improvment and reuses the underlying TCP connection to a host.

```python

import requests

with requests.Session() as session:
	# Set Cookies
	session.get('http://httpbin.org/cookies/set?key=value')
	# Get Cookies
	response = session.get('http://httpbin.org/cookies')
	print(response.text)


```


Overview and installation

```console
pip install requests
```



## Beautiful

<img width = 150 align= "left" src ="https://cdn.analyticsvidhya.com/wp-content/uploads/2020/03/ws3.png">
Beautiful Soup automatically converts incoming documents to __Unicode__ and outgoing documents to **UTF-8**.
It has a limited support for css selectors, but converts the most commenly used ones. 

```python 

from bs4 import BeautifulSoup
data = """
	<ul>
		<li class ="item"> l1 </li>
		<li class ="item"> l2 </li>
		<li class ="item"> l3 </li>
	</ul>
"""
soup = BeautifulSoup(data , 'html.parser')

for l in soup.select("li.item"):
	print(l.get_text())



```



Overview and installation

```console
pip install beautifulsoup4
```


## Selenuim

<img width = 150 align= "left" src ="https://cdn.analyticsvidhya.com/wp-content/uploads/2020/03/ws4-768x188.png">
Selenium is a Python library originally made for automated testing of web applications. Selenium works as we pretend like an actuall user,It simulates a real user as some websites don't like to be scraped. Selenuim launches and controls a web browser.
> Selenuim can modify browser cookies, fill in forms and take screenshots of web browsr.


Overview and installation

```console
pip install selenium
```
However, you need additional drivers for it to be able to interface with a chosen web browser.

## Urllib

[Urllib](https://docs.python.org/3/library/urllib.html) Urllib is a Python library that allows the developer to open and parse information from HTTP or FTP protocols. Urllib offers some functionality to deal with and open URLs, namely:

- `urllib.request`: opens and reads URLs.
- `urllib.error`: catches the exceptions raised by urllib.request.
- `urllib.parse`: parses URLs.
- `urllib.robotparser` : parses robots.txt files.


Overview and installation

```console
pip install urllib
```

## Scrapy

Try to avoid using Scrapy if you have a small project or you want to scrape one or just a few webpages. In this case, Scarpy will overcomplicate things and won’t add and benefits.

> I don't get my hand dirty orplay with scrapy yet



## Resources 

- [Python-urllib-module eeks4geeks](https://www.geeksforgeeks.org/python-urllib-module/)

- [5 Popular Python Libraries to Perform Web Scraping](https://www.analyticsvidhya.com/blog/2020/04/5-popular-python-libraries-web-scraping/)

- [Beginner’s guide to Web Scraping in Python using Beautiful Soup](https://www.analyticsvidhya.com/blog/2015/10/beginner-guide-web-scraping-beautiful-soup-python/?utm_source=blog&utm_medium=5-popular-python-libraries-web-scraping)

- [Choose the Best Python Web Scraping Library for Your Application](https://medium.com/m/global-identity?redirectUrl=https%3A%2F%2Ftowardsdatascience.com%2Fchoose-the-best-python-web-scraping-library-for-your-application-91a68bc81c4f)

- [Python-requests-and-persistent-sessions stackowerflow](https://stackoverflow.com/questions/12737740/python-requests-and-persistent-sessions)

- [Session-objects-python-requests](https://www.geeksforgeeks.org/session-objects-python-requests/)