# webscrapping-flipkart-reviews

Process to extract all the reviews for Iphone 11 mobile from Flipkart

Install the required packages 

*Try to Fetch Website Content using lxml as it's much faster as compared to html.parser*

> Using Beautifulsoup have fetched all the elements of the Site

 ```
 URL = 'https://www.flipkart.com/apple-iphone-11-white-64-gb/product-reviews/itmfc6a7091eb20b?pid=MOBFWQ6BVWVEH3XE&lid=LSTMOBFWQ6BVWVEH3XESAHPTP&sortOrder=MOST_HELPFUL&certifiedBuyer=false&aid=overall&page=1'

 page = requests.get(URL)

/*soup = BeautifulSoup(page.content, 'html.parser') */

soup = BeautifulSoup(page.content, 'lxml')  
```

*Try to fetch number of pages used to display the reviews present in the site. In other words to maximum number of pages in pagination*

Gather information present in span within parent div class

```
  page_details = soup.find('div', class_='_2MImiq _1Qnn1K').find('span').text  
 ``` 


