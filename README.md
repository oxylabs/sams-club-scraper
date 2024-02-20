# Sams-Club Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Sams-Club Scraper](https://oxylabs.io/products/scraper-api/ecommerce/sams-club?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Sams-Club website effortlessly. This brief guide showcases how Sams-Club Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Sams-Club results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Sams-Club page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.samsclub.com/content/home-services#home'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/sams-club-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><link rel=\"preload\" as=\"style\" href=\"/js/desktop.app.d9a0505af3 ... </html>",
      "created_at": "2024-02-20 12:52:28",
      "updated_at": "2024-02-20 12:52:29",
      "page": 1,
      "url": "https://www.samsclub.com/content/home-services#home",
      "job_id": "7165689665696039937",
      "status_code": 200
    }
  ]
}
```
With our Sams-Club Scraper, you can easily extract public data from any Sams-Club web page. Obtain relevant product information like promotions, customer feedback, detailed product specifications, and more to gain insight into market trends and outperform your competition. For any queries, reach out to our support team via live chat, or drop us a line at hello@oxylabs.io.