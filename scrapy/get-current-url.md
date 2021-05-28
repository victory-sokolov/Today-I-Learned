
`response.meta` - dict that contains metadata about request, as well you can pass custom information to meta dict.

```python
for link in rows:
  yield SplashRequest(
      url=link[0],
      callback=self.parse,
      meta={'original_url': link[0]},
  )

  def parse():
    yield {
      'url': response.meta['original_url']
    }
```
---
## Refences:
[Request meta](https://docs.scrapy.org/en/latest/topics/request-response.html#topics-request-meta)