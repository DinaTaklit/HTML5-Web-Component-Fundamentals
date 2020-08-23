# Custom Elements

## Problem: Undescriptive Markup

- Generic

```html
<div>
My do list<br/>
1. Take out trash<br/>
2. Walk the dog<br/>
3. Brush my teeth<br/>
</div>
```

- Descriptive

```html 
<h1>My do list</h1>
<ol>
<li>Take out trash</li>
<li>Walk the dog</li>
<li>Brush my teeth</li>
</ol>
```

### Descriptive markup

- Conveys additional information
- Improves SEO
- Enhances accessibility
- Speeds development
- Aids Maintenance

> The HTML `<div>` element is the generic container for flow
content, which does not inherently represent anything. It
can be used to group elements for styling purposes…or
because they share attribute values…It should be used
only when no other semantic element is appropriate. “
Mozilla Developer Network

### Which Would You Rather Read

```html
<div>
    <div>
        <div>
        </div>
        <div>
        </div>
    </div>
</div>
```

```html
<div class="forum-thread">
    <div class="forum-comment">
        <div class="user-avatar">
        </div>
        <div class="user-comment">
        </div>
    </div>
</div>
```

```html
<forum-thread>
    <forum-comment>
        <user-avatar>
        </user-avatar>
        <user-comment>
        </user-comment>
    </forum-comment>
</forum-thread>
```

## Create a Custom Elements

1. Define your own HTML elements. Name must have a dash (-)
2. Extend existing elements

    ```html
    <input type="text" is="search">
    ```

### Registering Elements

1. Create prototype

    ```html
    var SlickTabs = Object.create(HTMLElement.prototype);
    // Add properties and functions to protoype here.
    ```

2. Register the new element via registerElement

    ```html
    document.registerElement('slick-tabs');
    ```

3. Use it! (Add to DOM or place tag on page)

    ```html
    document.body.appendChild(new SlickTabs());
    ```

### You Can Extend Custom Elements Too

```html
var XFooProto = Object.create(HTMLElement.prototype);
...

var XFooExtended = document.registerElement('x-foo-extended', {
prototype: XFooProto,
extends: 'x-foo'
});
```

### Four Ways To Instantiate

1. Markup
  
    ```html
    <pluralsight-comment />
    ```

2. new Operator

    ```html
    var comment = new PluralsightComment();
    ```

3. createElement

   ```html
   var comment = document.createElement('pluralsight-comment');
   ```

4. innerHTML

    ```html
    el.innerHTML = '<pluralsight-comment />';
    ```
