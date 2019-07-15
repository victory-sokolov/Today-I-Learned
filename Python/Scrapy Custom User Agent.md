# Custom User-Agent in Scrapy


middleware.py
```python
class UserAgentRotatorMiddleware(UserAgentMiddleware):
    user_agents_list = [
        'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/74.0.3729.169 Safari/537.36',
        'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/60.0.3112.113 Safari/537.36',
        'Mozilla/5.0 (Windows NT 6.1; WOW64; rv:54.0) Gecko/20100101 Firefox/54.0',
        'Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:67.0) Gecko/20100101 Firefox/67.0'
    ]

    def __init__(self, user_agent=''):
        self.user_agent = user_agent

    def process_request(self, request, spider):
        try:
            self.user_agent = random.choice(self.user_agents_list)
            request.headers.setdefault('User-Agent', self.user_agent)
        except IndexError:
            logging.error("Couldn't fetch the user agent")
```

settings.py

```python
DOWNLOADER_MIDDLEWARES = {
    'parser_name.middlewares.UserAgentRotatorMiddleware' : 400,
}
```
