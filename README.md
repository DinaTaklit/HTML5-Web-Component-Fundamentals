# HTML5 Web Component Fundamentals

- Learn how HTML5 Web Components give us the power to extend the web with our own rich, standards-based components.
- Web developers have been struggling for years to create truly **reusable components**.
- We struggle with styling, bundling, defining templates, and encapsulating our markup and styles from accidental manipulation.
- But HTML5 Web Components provide the power to finally define standards-based, reusable web components through four(04) new technologies.
- Learn how to use the **Shadow DOM** to encapsulate the DOM and styling for your components.
- Define **inert templates** with the template tag.
- Extend HTML by **registering your custom elements**.
- And bundle this all together in a simple **reusable package** using HTML5 **imports**.

## Web Developers Have Problems

1. Undescriptive Markup
2. Style Conflicts
    - Avoiding style conflicts requires highly specific CSS selectors
    - Use of !important to force styles
    - No guarantee another style won’t conflict
  
3. No Native Templates
    - We slap HTML in `<script type="text/html">`
    - We store HTML in hidden DOM elements and manually extract
    - We use iframe’s to get separate scope and styling
  
4. No Bundling
    - What if you want to bundle some CSS, JS, and HTML together?
  
5. No Standard

## The Solution => Web Componenets

- Templates: Inert, reusable markup
- Custom Elements: Define our own Elements
- Shadow DOM: Encapsulated Markup & Styling
- Imports: Bundle HTML, JS, & CSS
  
## Why Learn Native Web Components First

Learn the foundation (like JS) before learn the abstraction over foundation (ex: JQuery). => Learn Web Components (foundation) before learn Plymer for ex (abstraction over foundation).

## Why Web Components

- Descriptive markup
- Don't start at square zero
- Easily replaced & upgraded
- Fewer integration mistakes
- Clearer interface / API

![Why Web Components][why-web-componenets]

[why-web-componenets]: Images/why-web-components.PNG "Why Web Components"

## Credits

All credits goes for pluralsight course HTML5 Web Component Fundamentals by by Cory House.
