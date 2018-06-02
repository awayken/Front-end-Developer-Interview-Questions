# CSS Questions:

*Question:* What is CSS selector specificity and how does it work?

*Answer:* a selector defines which HTML elements your rules should apply to. The way you phrase your selector determines how specific it is. CSS, through its cascading, let's you apply layers of rules, but the more specific a rule is, the more strongly it will be applied.

* Selector part: score
* element/psuedo-element: 00001
* class/psuedo-class: 00010
* id: 00100
* inline styling: 01000
* !important: 10000

*Question:* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

*Answer:* Resetting is an effort to eliminate nearly all browser-imposed styling on elements that fall outside semantic interface requirements. Margins, paddings, font-sizes, it all gets brought down to zero. Normalizing allows browsers to impose more styling but still aims to iron out minor style differences between the engines.

*Question:* Describe Floats and how they work.

*Answer:* Floats take an element out of the verticle flow of a document while maintaining the horizontal flow, usually aligning the element in a certain direction (left or right). It's best used to float an image along the right side of an article of text, but the technique has been most frequently used to afford basic web layout functionality.

*Question:* Describe z-index and how stacking context is formed.

*Answer:* z-index allows an element to stack in z-space given certain values of `position`. z-index is a unitless number, and the higher number will be considered closer to the viewer. Stacking context is determined by a number of browser rules, but essentially anything that would cause an element to place above other elements or to allow other elements to be seen through the element will probably establish a stacking context for that element.

*Question:* Describe block formatting context and how it works.

*Answer*: A block formatting context is a part of a visual CSS rendering of a Web page. It is the region in which the layout of block boxes occurs and in which floats interact with other elements. The rules for positioning and clearing of floats apply only to things within the same block formatting context.

*Question:* What are the various clearing techniques and which is appropriate for what context?

*Answer*: You can clear by using using a `clear` declaration on a sibling element. That sibling will then clear the float that comes before it. You can also establish a new block formatting context via the rules it sets forth.

*Question:* How would you approach fixing browser-specific styling issues?

*Answer:* Whenever possible, I try to use the natural fall-back capability of CSS. There are some resources out there for "hacking" styles that apply to a single browser. I general prefer to think of browsers as having features or not, rather than target the browser by version or name. 

*Question:* How do you serve your pages for feature-constrained browsers? What techniques/processes do you use?

*Answer:* Feature queries are also a great way of ensuring that your styles are applied to browser that support that feature. You can then firmly control how your site will look for browsers that don't support that feature, instead of relying on side-effects.

*Question:* What are the different ways to visually hide content (and make it available only for screen readers)?

*Answer:* You can position absolutely and move off the screen. That's an easy one but it can backfire for users that increase their text font zoom. Alternative, you can use a combination of absolute positioning, resizing and clipping.

*Question:* Have you ever used a grid system, and if so, what do you prefer?

*Answer:* I've used Bootstrap. It's fine. I think the advent of grid and flexbox really elminates most of the need for layout/grid systems.

*Question:* Have you used or implemented media queries or mobile specific layouts/CSS?

*Answer:* Yes. I prefer to work mobile-first, enhancing and updating the layout for larger screen sizes with media queries.

*Question:* Are you familiar with styling SVG?

*Answer:* Not really.

*Question:* Can you give an example of an `@media` property other than `screen`?

*Answer:* `print`

*Question* What are some of the "gotchas" for writing efficient CSS?

*Answer:* Being overly specific is a gotcha in a number of ways: it can break if HTML changes, it can prevent nice cascading by its specificity score, it can discourages reuse.

*Question:* What are the advantages/disadvantages of using CSS preprocessors? Describe what you like and dislike about the CSS preprocessors you have used.

*Answer:* Can improve developer efficiency with mixins, variables, custom fuctions and more. Some people like the alternate syntaxes to CSS. It's much easier to break a CSS file into parts that stitch together to make one download. The disadvantages are that they require processing before the browser can use those files. It's another language to learn and maintain. Since output is generated, it can lead to potentially bloated files.

*Question:* How would you implement a web design comp that uses non-standard fonts?

*Answer:* Use web fonts. Purchase the font with a web license and use the `@font-face` rule to define a font face using the font files you've uploaded to your web server.

*Question:* Explain how a browser determines what elements match a CSS selector.

*Answer:* Browsers start at the right-most part of the selector and begin to filter out DOM elements as they cease to match the selector. Another reason to prefer shallow selectors.

*Question:* Describe pseudo-elements and discuss what they are used for.

*Answer:* These are not literal elements in the DOM but can be made to act and display like real elements even though they are created in CSS. `::before` and `::after` are two examples.

*Question:* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

*Answer:* The box model defines how CSS renders boxes. All HTML elements for some sort of box, although not every display type renders every box property. Width, height, padding, border and margin are all part of this model.

*Question:* What does `* { box-sizing: border-box; }` do? What are its advantages?

*Answer:* A common gotcha is setting a width and height on an element and then sizing it and finding that it doesn't quite render at the size you expected. The default value for `box-sizing` is `content-box`. This means that width and height are applied to the content, then padding and border applied on top. `border-box` ensures that your overall box width and height match the declarations you set.

*Question:* What is the CSS `display` property and can you give a few examples of its use?

*Answer:* Determines how to display the element. `inline` renders like a character in a word. `inline-block` renders like a word in a sentence. `block` renders like a paragraph of sentences. There are also `display` values for the new flexbox and grid capabilities (`flex` and `grid` respectively).

*Question:* What's the difference between inline and inline-block?

*Answer:* `inline` renders like a character in a word. `inline-block` renders like a word in a sentence. `inline-block` allows for more of the box model to be modified (top/bottom margins and paddings, for instance) and vertical alignment options.

*Question:* What's the difference between a relative, fixed, absolute and statically positioned element?

*Answer:* The different values determine the rules for how setting top, bottom, left and right all work. Absolute is (usually) positioned relative to the upper left corner of the HTML document. Fixed is relative to the viewport. Relative is relative to where the element was drawn statically. And statically is not affected and renders in place.

*Question:* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

*Answer:* Bootstrap

*Question:* Have you played around with the new CSS Flexbox or Grid specs?

*Answer:* Yes. Mostly with Flexbox, but I'd love a chance to try out grid. Both specs have pretty good modern support (or fallback strategies) and really improve layout styling. No more complicated floats!

*Question:* Can you explain the difference between coding a web site to be responsive versus using a mobile-first strategy?

*Answer:* Mobile-first means that the rules outside of `@media` rules are geared toward small screens. `@media` queries are used to apply styles to larger and larger screen sizes. This is a type of responsive styling. You can also style the other way, starting for large screens and using `@media` queries to target small screens. That is still responsive but not mobile-first.

*Question:* Have you ever worked with retina graphics? If so, when and what techniques did you use?

*Answer:* Not as much in CSS, although I know you can specify pixel density in `@media` queries.

*Question:* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

*Answer:* `translate()` can take advantage of GPU rendering which makes it more performant than absolute positioning if you know you'll be moving the element around.
