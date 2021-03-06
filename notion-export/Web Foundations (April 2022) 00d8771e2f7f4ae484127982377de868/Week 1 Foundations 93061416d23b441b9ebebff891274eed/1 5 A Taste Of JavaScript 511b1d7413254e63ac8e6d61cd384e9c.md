# 1.5 A Taste Of JavaScript

*Estimated Time: 15 minutes*

---

JavaScript lets you control the **action** on a page. It’s also a super powerful programming language you can use for all kinds of other applications.

Today, you’re just going to see how to link a JavaScript file to your HTML.

## Script tag

We write our JavaScript in separate files, which in this course we’ll name `script.js`. To connect the JavaScript to the HTML page, we’ll use a `<script>` tag.

```html
<script src="script.js"></script>
```

- We use the `src` attribute to say where to find the JavaScript file.
    - **Note:** It’s called `src` for `<script>` tags. It’s called `href` attribute for `link` and `a` tags.
- We usually place the script tag at the end of the `<body>` tag, so that the rest of the page has loaded before the script is run.
- The `<script>` tag is not self-closing, it needs the closing tag `</script>`.

## Practice: Link the JavaScript using the <script> tag

<aside>
👉🏿 Add the `<script>` tag to connect the JavaScript file to the HTML page.

</aside>

[https://replit.com/team/tk5-web/Practice-Link-the-Script](https://replit.com/team/tk5-web/Practice-Link-the-Script)

## Deeper Connections: CSS Selectors in JS

<aside>
👀 Take a look at the JavaScript file `script.js` in the Practice. In week 3, we’ll talk more about how the code works.

</aside>

In particular, look at all the places it uses CSS Selectors:

```jsx
document.querySelector('#gross')
document.querySelector('.reaction')
document.querySelector('#yum')
```

`#gross`, `.reaction`, and `#yum` are all CSS Selectors! When you learn to use JavaScript to create interactions, you’ll still use concepts from HTML and CSS. 

The same CSS selectors that you use for styles will also let you pick HTML elements in your JS code.

---

<aside>
<img src="../Lesson%200%20Learning%20With%20Kibo%206427d2f5f1ae4576a3b083dd8476d915/man-in-hike.png" alt="../Lesson%200%20Learning%20With%20Kibo%206427d2f5f1ae4576a3b083dd8476d915/man-in-hike.png" width="40px" /> Next up: [Practice](Practice%205cba1a0d96db482d9c68572be4f0a579.md)

</aside>