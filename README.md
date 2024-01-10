# Imdb Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Imdb Scraper](https://oxylabs.io/products/scraper-api/web/imdb?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Imdb website effortlessly. This brief guide showcases how Imdb Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Imdb results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Imdb page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.imdb.com/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/imdb-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-US\" xmlns:og=\"http://opengraphprotocol.org/schema/\" xmlns:fb=\"http://w ... </html>",
      "created_at": "2024-01-10 09:34:26",
      "updated_at": "2024-01-10 09:34:28",
      "page": 1,
      "url": "https://www.imdb.com/",
      "job_id": "7150781926540843009",
      "status_code": 200
    }
  ]
}
```
With our Imdb Scraper, you can effortlessly extract public data from any Imdb webpage. Collect the required movie or TV series information, such as ratings, cast details, plot summaries or reviews, to analyze the entertainment market and stay ahead of your competitors. If you have any questions, contact our support team via live chat or email us at hello@oxylabs.io.