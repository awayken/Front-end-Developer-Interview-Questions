# HTML Questions:

*Question:* What does a `doctype` do?

*Answer:* It tells the browser what type of document it's rendering. This determines the parsing and rendering rules it will follow.

*Question:* How do you serve a page with content in multiple languages?

*Answer:* You can use the `lang` attribute to define the language of text in an element.

*Question:* What are `data-` attributes good for?

*Answer:* They allow you to easily associate data with an HTML element in a semantic and programmatically feasible way.

*Question:* Consider HTML5 as an open web platform. What are the building blocks of HTML5?

*Answer:* Layout elements, better semantics, new JavaScript and DOM APIs.

*Question:* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.

*Answer:* Cookie is the oldest data store. String-based and usually passed in HTTP requests. It's prone to abuse and misuse. sessionStorage data lasts for the session of the user but unreliable. localStorage has a nice api and is async so writing and reading from it won't block your main thread, and it also doesn't get passed around so it's more private.

*Question:* Describe the difference between `<script>`, `<script async>` and `<script defer>`.

*Answer:* Script alone just allows you to download and parse an external JS file or some inline scripting. When the browser sees that tag, it'll stop to download that file and parse it immediately. `async` tells the browser that the file can be downloaded in the background and parsed after download. `defer` tells the browser to download now but defer parsing until the document is loaded.

*Question:* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?

*Answer:* When the browser encounters a linked CSS file, it will block to download it and parse it. CSS files also incur paint and layout, so you want to get that all out of the way as soon as possible to prevent re-layout and re-paint as much as possible. Script tags do the same thing. The browser will block to download and parse the script, but script files don't usually cause layout or paint so we want to wait until the end to incur that cost and we don't have to worrk about undoing all the work we've just done.

*Question:* What is progressive rendering?

*Answer:* Process of using various techniques to render the page as quickly as possible, deferring extraneous visual enhancements for later. Lazy loading images, for instance.

*Question:* Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.

*Answer:* It defines a set of image sources that the browser can choose between when rendering that element. It is usually used in conjunction with the `sizes` attribute to provide responsive images for the user.

*Question:* Have you used different HTML templating languages before?

*Answer:* I've used Pug a little and Mustache a bit. They're fine.
