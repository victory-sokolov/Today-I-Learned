# AOS animation library with Gatsby

AOS is using window global object and while building gatsby for production `gatsby build` you will get following error

```"document" is not available during server side rendering.```

## Init AOS
```js

let AOS;
  useEffect(() => {
    /**
     * Server-side rendering does not provide the 'document' object
     * therefore this import is required either in useEffect or componentDidMount as they
     * are exclusively executed on a client
     */
    const AOS = require("aos");
    AOS.init({
      once: true,
    });
  }, []);

  useEffect(() => {
    if (AOS) {
      AOS.refresh();
    }
  });
```
