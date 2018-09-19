# Week 2 Cool Down

**Read [How CSS Works](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works) and answer the following questions below.**

### Questions

Example Question: This article explains what CSS is, how the browser turns HTML into a Document Object Model (___), how CSS is applied to parts of the DOM, some very basic syntax examples, and what code is used to actually include our CSS in our web page.

1. Name the two other markup languages (other than HTML) mentioned in the article.

2. In technical terms, what does it mean to present a document. **Quote the article.**

3. Explain what a CSS rule is formed from. 

4. Summarize the two steps for how CSS actually works.

5. In your own words, explain the three ways to apply your CSS to your HTML.

**Read [CSS Syntax](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Syntax) and answer the following questions below.**

6. *"CSS is a declarative language, which makes its syntax fairly easy and straightforward to understand. In addition, it also has a very nice error recovery system that allows you to make mistakes without breaking everything — for example declarations that aren't understood are generally just ignored."* But what is the downside (quote the article)?

7. Define the two building blocks of CSS.

8. Type an example of a CSS Declaration.

9. *True or False* - A declaration block may be empty — this is perfectly valid.

10. Summarize the ***CSS Selectors and Rules*** section of the article.

11. Identify and explain in your own words the three ways to make CSS readable.

**Read [Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Selectors) and answer the following question below.**

12. Identify and explain in your own words the six categories of selectors.

**Read [Simple Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Simple_selectors) and answer the following questions below.**

13. ____ Selectors aka Element Selectors

14. What does a class selector consist of?

15. Why must an ID name be unique in the document?

16. The _________ selector (`*`) is the ultimate joker. It allows selecting all elements in a page. As it is rarely useful to apply a style to every element on a page, it is often used in combination with other selectors.

**Read [Cascade and Inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance) and answer the following questions below.**

17. ___ is an acronym for Cascading Style Sheets, which indicates that the notion of the cascade is important. At its most basic level it indicates that the order of CSS rules matter, but it's more complex than that. 

18. What selectors win out in the cascade depends on what three factors (these are listed in order of weight — earlier ones will overrule later ones)?

19. *In CSS, there is a special piece of syntax you can use to make sure that a certain declaration will always win over all others* - what is it?

20. ___________ is basically a measure of how specific a selector is — how many elements it could match.

21. What is the simple seven-word definition of *source order*?

22. CSS ___________ is the last piece we need to investigate to get all the information and understand what style is applied to an element. The idea is that some property values applied to an element will be inherited by that element's children, and some won't.

**Read [The Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Box_model) and answer the following questions below.**

23. *Every element within a document is structured as a rectangular box inside the document layout, the size and "onion layers" of which can be tweaked using some specific CSS properties.* What is this describing?

### Answers

Type your answers here:

Example Answer: *DOM*

1. SVG and XML

2. Presenting a document to a user means converting it into a usable form for your audience. Browsers, like Firefox, Chrome or Internet Explorer, are designed to present documents visually, for example, on a computer screen, projector or printer.

3. A set of properties, which have values set to update how the HTML content is displayed, for example I want my element's width to be 50% of its parent element, and its background to be red. A selector, which selects the element(s) you want to apply the updated property values to. For example, I want to apply my CSS rule to all the paragraphs in my HTML document.

4. The browser converts HTML and CSS into the DOM (Document Object Model). The DOM represents the document in the computer's memory. It combines the document's content with its style.
The browser displays the contents of the DOM.

5. (1) You've already seen external stylesheets in this article, but not by that name. An external stylesheet is when you have your CSS written in a separate file with a .css extension, and you reference it from an HTML <link> element. This method is arguably the best, as you can use one stylesheet to style multiple documents, and would only need to update the CSS in one place if changes were needed. (2) An internal stylesheet is where you don't have an external CSS file, but instead place your CSS inside a <style> element, contained inside the HTML head. This can be useful in some circumstances (maybe you're working with a content management system where you can't modify the CSS files directly), but it isn't quite as efficient as external stylesheets — in a website, the CSS would need to be repeated across every page, and updated in multiple places if changes were required. (3) Inline styles are CSS declarations that affect one element only, contained within a style attribute. Please don't do this, unless you really have to! It is really bad for maintenance (you might have to update the same information multiple times per document), and it also mixes your presentational CSS information with your HTML structural information, making the CSS harder to read and understand. Keeping your different types of code separated and pure makes for a much easier job for all who work on the code. The only time you might have to resort to using inline styles is when your working environment is really restrictive (perhaps your CMS only allows you to edit the HTML body.)

6. The downside is that it can be harder to understand where errors are coming from.

7. Properties: Human-readable identifiers that indicate which stylistic features (e.g. font, width, background color) you want to change. Values: Each specified property is given a value, which indicates how you want to change those stylistic features (e.g. what you want to change the font, width or background color to.)

8. `p {  font-size: 12px; }`

9. True

10. We are missing one part of the puzzle — we need to discuss how to tell our declaration blocks which elements they should be applied to. This is done by prefixing each declaration block with a selector — a pattern that matches some elements on the page. The associated declarations will be applied to those elements only. The selector plus the declaration block is called a ruleset, or often simply just a rule. Selectors can get very complicated — you can make a rule match multiple elements by including multiple selectors separated by commas (a group,) and selectors can be chained together, for example I want to select any element with a class of "blah", but only if it is inside an <article> element, and only while it is being hovered by the mouse pointer. An element may be matched by several selectors, therefore several rules may set a given property multiple times. CSS defines which one has precedence over the others and must be applied: this is called the cascade algorithm.

11. (1) White space means actual spaces, tabs and new lines. You can add white space to make your style sheets more readable. In the same manner as HTML, the browser tends to ignore much of the whitespace inside your CSS; a lot of the whitespace is just there to aid readability. In our first example below we have each declaration (and rule start/end) on its own line — this is arguably a good way to write CSS, as it makes it easy to maintain and understand. The code layout you choose is usually a personal preference, although when you start to work in teams, you may find that the existing team has its own styleguide that specifies an agreed convention to follow. The whitespace you do need to be careful of in CSS is the whitespace around the properties and their values. (2) As with HTML, you are encouraged to make comments in your CSS, to help you understand how your code works when coming back to it after several months, and to help others understand it. Comments are also useful for temporarily commenting out certain parts of the code for testing purposes, for example if you are trying to find which part of your code is causing an error. Comments in CSS begin with `/*` and end with `*/`. (3) Some properties like font, background, padding, border, and margin are called shorthand properties — this is because they allow you to set several property values in a single line, saving time and making your code neater in the process.

12. (1) Simple selectors: Match one or more elements based on element type, `class`, or `id`. (2) Attribute selectors: Match one or more elements based on their attributes/attribute values. (3) Pseudo-classes: Match one or more elements that exist in a certain state, such as an element that is being hovered over by the mouse pointer, or a checkbox that is currently disabled or checked, or an element that is the first child of its parent in the DOM tree. (4) Pseudo-elements: Match one or more parts of content that are in a certain position in relation to an element, for example the first word of each paragraph, or generated content appearing just before an element. (5) Combinators: These are not exactly selectors themselves, but ways of combining two or more selectors in useful ways for very specific selections. So for example, you could select only paragraphs that are direct descendants of divs, or paragraphs that come directly after headings. (6) Multiple selectors: Again, these are not separate selectors; the idea is that you can put multiple selectors on the same CSS rule, separated by commas, to apply a single set of declarations to all the elements selected by those selectors.

13. Type

14. The class selector consists of a dot, '.', followed by a class name. 

15. An ID name must be unique in the document. Behaviors regarding duplicated IDs are unpredictable. For example, in some browsers, only the first instance is counted, and the rest are ignored.

16. Universal

17. CSS

18. (1) Importance, (2) specificity, and (3) source order.

19. `!important`

20. Specificity 

21. Later rules will win over earlier rules.

22. Inheritance

23. Box properties

**Copyright &copy; 2018 Riyaad Azad. Free to copy and distribute as per the [official license on GitHub](https://github.com/ra-coding-club/coding-club/blob/master/LICENSE). All other rights reserved.** 
