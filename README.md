# Shopee-crawler

This is a light crawling tool.

High performance.

Easy to use.
***
## Requirement
```env
python>=3.7
```

## Sponsor

SadCaptcha has paid to be here and I have no affiliation with them.

<div align="center">
  <a href="https://www.sadcaptcha.com/shopee-captcha-solver?ref=letrong" target="_blank">
    <img src="https://sadcaptcha.b-cdn.net/shopee-image-crawl-captcha.webp" width="150" alt="Shopee Captcha Solver">
    <img src="https://sadcaptcha.b-cdn.net/shopee-puzzle-slide-captcha.webp" width="150" alt="Shopee Captcha Solver">
    <br/>
    <div>
         <b>Shopee Captcha Solver: </b> Bypass any Shopee captcha code-free.<br> Scale your Shopee automation and get unblocked with SadCaptcha.
    </div>
  </a>
</div>

## Install

* Using `setup.py`
```
git clone https://github.com/lthoangg/shopee-crawler
python/python3 setup.py install
```

* Using `pip`
```
pip install shopee-crawler
```

## How to use
Examples:
```python
from shopee_crawler import Crawler

crawler = Crawler()
crawler.set_origin(origin="shopee.vn") # Input your root Shopee website of your country that you want to crawl

data = crawler.crawl_by_shop_url(shop_url='shop_url')

data = crawler.crawl_by_cat_url(cat_url='cat_url')

data = crawler.crawl_by_search(keyword='keyword')

data = crawler.crawl_cat_list()
# print(data)
```

## Usage
- About 12.000 rows (products) in 2-3 seconds (32 workers)

- About 12.000 rows (products) in 5-6 seconds (16 workers)

## Test yourself

```python
import time
from shopee_crawler import Crawler

crawler = Crawler()
crawler.set_origin(origin="shopee.vn")

keyword = 'điện thoại samsung'

# Start time
start = time.time()

# Crawl
data = crawler.crawl_by_search(keyword=keyword)

# End time
end = time.time()

# Time crawling
print("Time : ",end - start, "seconds")

```