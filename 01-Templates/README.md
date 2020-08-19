# Templates

- Existing template strategies
- Defininf Templates
- Activating Templates
- Injecting Date
- Nested Templates
  
## You Already Use Templates Today

- RAILS: HAML
- ASP.NET: Razor
- Python: Django
- Node Js: Jade
  
=> We need Native HTML Templates

## Todays's Common Approaches to Templates

1. HTML in Script Tags
   - `<script type="text/custom-name-here">`
   - pros: Nothing inside runs or renders
   - cons: Not DOM Elments => XSS risk from using .innerHTML

2. Hidden DOM elements
   - `<div style="display:none;" id="my-template"></div>`
   - pros: Easy to clone - just DOM elemnts
   - cons: Everything inside still runs. May throw 404's, `<script>` runs, etc.

> The Solution? ===> `<template>`

## Template Characteristics

- **Inert**: Does nothing until cloned
  
## Template Activation

1. `var template = document.querySelector("#mytemplate");`
2. `var clone = document.importNode(template.content,true);`
3. `document.body.appendChild(clone);`

## Inject Data Into Template

Inject data before cloning by manipulating the template clone.

1. Get a reference to the template
`var template = document.querySelector("template");`
2. Use document.importNode to clone the template
`var clone = document.importNode(template.content, true);`
3. Chnage the target element within the template
`clone.querySlector('.verb').textContent = 'awesome';`
4. Append element to page
`document.body.appendChile(clone);`

## Nested Templates

Must manually clone both the parent and child templates

```html
<template id="header">
<div>Header</div>
<template id="body">
<div>Body</div>
</template>
</template>
```

## Summay

- We've been getting by with hacks for HTML templates `<template>` gives us a standar
- All content inside does nothing until activated via cloning
- No native data interpolation/logic, but hey, it's just DOM!
