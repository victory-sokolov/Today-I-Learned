# Fixed footer


HTML

```html
<body>
  <header>Header</header>
  <article>Content</article>
  <footer>Footer</footer>
</body>
```

## Flexbox

CSS

```css
header{ 
	min-height:50px; 
	background:lightcyan; 
}

footer{ 
	min-height:50px; 
	background:PapayaWhip; 
}


body{ 
  display:flex; 
  flex-direction:column; 
}
```


## Grid

CSS

```css
body{ 
  min-height: 100vh; 
  display: grid;
  grid-template-rows: auto 1fr auto;
}

header{ 
  min-height:50px;
  background:lightcyan; 
}

footer{ 
  min-height:50px; 
  background:PapayaWhip; 
}
```


