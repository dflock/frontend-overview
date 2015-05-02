# Front End Development Overview

### In The Beginning Was The Word

- HTML = Documents
- CSS = Presentation
- HTTP = Protocol

### Eating The Forbidden Fruit

- JS = Behaviour
- What is the DOM?
- Documents vs Applications

### On the Seventh day, He RESTed.

- Server vs Client side templating - tornado/jinja & handlebars.js
- REST & stateless applications, client/server side state, cookies

---

# In The Beginning Was The Word

## Declarative Bliss

- Simplest thing that could possibly work
- All declarative
- All server side

---

# HTML ~ Documents

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Example 1 - Page Title</title>
  </head>
  <body>
    <article>
      <header>
        <h1>A Heading</h1>
      </header>
      <figure>
        <img src="img/pattern-1.svg">
        <figcaption>Hmmmm... triangly....</figcaption>
      </figure>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit.
        Id laboriosam eligendi necessitatibus distinctio eius veritatis
        non nulla nostrum rem, neque sequi aut accusamus eaque
        voluptate ipsa, omnis, totam iste veniam!
      </p>
    </article>
  </body>
</html>
```

Examples & More:
- [Example 1](http://frontend-overview.test/examples/1.html)
- [First ever Web Page](http://frontend-overview.test/examples/TheProject.html)

---

# CSS ~ Presentation

```css
body {
    width: 70%;
    margin: 0 auto;
}
h1 {
    font-size: 4em;
    margin: 0.25em 0;
}
p {
    font-size: 1.5em;
}
img {
    float: left;
    padding: 4px;
    margin: 0 0.5em 0.5em 0;
    border: 1px solid #ccc;
    box-shadow: 2px 2px 2px #ccc;
}
img.caption {
  margin-bottom: 2em;
}
```

**Selectors** select which bits of HTML get their style **rules** applied to them.

Examples & More:
- [Example 2](http://frontend-overview.test/examples/2.html)

---

# The Cascade

- ⇣ User Agent Stylesheets
- ⇣ Site Supplied Stylesheets
- ⇣ Users Stylesheets
- = Final Styles

## Specificity

- All matching selectors, from all stylesheets, are applied to an element - in specificity order.
- The 'most specific' selector 'wins':

**[style=""] ➜ [#id] ➜ [.class|:pseudo-class|[attribute]] ➜ [element]**

- Each one gets its own column in the final number: **(0,0,0,0)**
- For example, 3 classes like `.list .item .active { ... }`, gets you (0,0,**+3**,0)
- Read left-to-right, ∴ no amount of classes can override an id.

Examples & More:

- [Example 3](http://frontend-overview.test/examples/3.html)
- https://css-tricks.com/specifics-on-css-specificity/

---

# HTTP ~ Protocol

Hypertext Transfer Protocol

- 1989, v0.1: GET
- 1995, v1.0: GET, POST & HEAD
- 1996, v1.1: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE & CONNECT

### A Protocol == a structured conversation

- User Agent makes a **Request**
  - Verbs: GET, POST, HEAD...
  - With appropriate `Accept:` header
- Server sends a **Response**
  - Sends back response in a format you said you could `Accept`

``` bash
$ telnet frontend-overview.test 80
```
---

# HTTP ~ Protocol

```bash
$ http -v GET http://frontend-overview.test/examples/2.html
```

```http
GET /examples/2.html HTTP/1.1
Accept: */*
Accept-Encoding: gzip, deflate
Connection: keep-alive
Host: frontend-overview.test
User-Agent: HTTPie/0.9.2

HTTP/1.1 200 OK
Connection: keep-alive
Content-Encoding: gzip
Content-Type: text/html
Date: Tue, 14 Apr 2015 00:59:17 GMT
Last-Modified: Tue, 17 Mar 2015 02:28:17 GMT
Server: nginx/1.4.1 (Ubuntu)
Transfer-Encoding: chunked

<!DOCTYPE html>
<html>
  <head>
    <title>Example 2 - Page Title</title>
    <link rel="stylesheet" href="css/2.css">
  </head>
  ...
```

---

# Eating The Forbidden Fruit

> But of the fruit of the tree which is in the midst of the garden, God hath said, Ye shall not eat of it, neither shall ye touch it, lest ye die. And the serpent said unto the woman, Ye shall not surely die: For God doth know that in the day ye eat thereof, then your eyes shall be opened, and ye shall be as gods, knowing good and evil.

- JavaScript: 1995, Netscape Navigator 2.0
- JScript: 1996, Internet Explorer 3.0
- ECMAScript: 1997

---

# JS ~ Behaviour

- Sent to browser like any other file
- Evaluated client-side

---

# What is the DOM?

- Document Object Model
- HTML ➭ JS ORM

Examples & More:

- [Example 4](http://frontend-overview.test/examples/4.html)

---

# Documents vs Applications

- Single page vs. multi-page
- XMLHttpRequest (XHR) - IE5, March 1999
- Internet round-trips are slow, so do them async
- Allows DOM Mutation, rather than reload

---

# On the Seventh day, He RESTed.


---

### Odds & Ends

- LESS vs CSS
- Bootstrap & jQuery
