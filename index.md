## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/brzTudor/newSite/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/brzTudor/newSite/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.


<body> 
  
  Bine ai venit la lab <button onclick="alertCookie()">Show cookies</button> 
  
  <br>
  
  <button onclick="resetOnce()">Reset only once cookie</button>

  <button onclick="clearOutputResetOnce()">
    Clear
  </button>

<div>
  <code id="reset-once"></code>
</div>
  
  <br>
  
  <button onclick="checkACookieExists()">
  Check a cookie exists
</button>

<button onclick="clearOutputACookieExists()">
  Clear
</button>

<div>
  <code id="a-cookie-existence"></code>
</div>
  
  <br>
  
  <button onclick="checkCookieHasASpecificValue()">
  Check that a cookie has a specific value
</button>

<button onclick="clearASpecificValueOfTheCookie()">
  Clear
</button>

<div>
  <code id="a-specific-value-of-the-cookie"></code>
</div>
  
  <br>
  
  
</body>

<script>
  document.cookie = "session=test GDPR"; 
  document.cookie = "favorite_task=collect Data"; 
  function alertCookie() { 
    alert(document.cookie); 
  }
  
  function resetOnce() {
  // Note that we are setting `SameSite=None;` in this example because the example
  // needs to work cross-origin.
  // It is more common not to set the `SameSite` attribute, which results in the default,
  // and more secure, value of `SameSite=Lax;`
  document.cookie = "doSomethingOnlyOnce=; expires=Thu, 01 Jan 1970 00:00:00 GMT; SameSite=None; Secure";

  const output = document.getElementById('reset-once')
  output.textContent = '> Reset!'
}

function clearOutputResetOnce() {
  const output = document.getElementById('reset-once')
  output.textContent = ''
}
  
  document.cookie = "reader=1; SameSite=None; Secure";

function checkACookieExists() {
  if (document.cookie.split(';').some((item) => item.trim().startsWith('reader='))) {
    const output = document.getElementById('a-cookie-existence')
    output.textContent = '> The cookie "reader" exists'
  }
}

function clearOutputACookieExists() {
  const output = document.getElementById('a-cookie-existence')
  output.textContent = ''
}
  
  function checkCookieHasASpecificValue() {
  if (document.cookie.split(';').some((item) => item.includes('reader=1'))) {
    const output = document.getElementById('a-specific-value-of-the-cookie')
    output.textContent = '> The cookie "reader" has a value of "1"'
  }
}

function clearASpecificValueOfTheCookie() {
  const output = document.getElementById('a-specific-value-of-the-cookie')
  output.textContent = ''
}
</script>

