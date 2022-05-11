## 1.Type

Remember that declarations are a fundamental part of CSS because they apply a style to a selected element. But how do you decide which elements will get the style? With a selector.

A selector is used to target the specific HTML element(s) to be styled by the declaration. One selector you may already be familiar with is the type selector. Just like its name suggests, the type selector matches the type of the element in the HTML document.

In the previous lesson, you changed the color of a paragraph element.

```css
p {
  color: green;
}
```

This is an instance of using the type selector! The element type is `p`, which comes from the HTML `<p>` tag.

Some important notes on the type selector:

- The type selector does not include the angle brackets.
- Since element types are often referred to by their opening tag name, the type selector is sometimes referred to as the tag name or element selector.

## 2.Universal

You learned how the type selector selects all elements of a given type. Well, the universal selector selects all elements of any type.

Targeting all of the elements on the page has a few specific use cases, such as resetting default browser styling, or selecting all children of a parent element. Don’t worry if you don’t understand the use cases right now—we will get to them later on in our Learn CSS journey.

The universal selector uses the \* character in the same place where you specified the type selector in a ruleset, like so:

```css
* {
  font-family: Verdana;
}
```

In the code above, every text element on the page will have its font changed to `Verdana`.

## 3.Class

CSS is not limited to selecting elements by their type. As you know, HTML elements can also have `attributes`. When working with HTML and CSS a class attribute is one of the most common ways to select an element.

For example, consider the following HTML:

```css
<p class='brand'>Sole Shoe Company</p>
```

The paragraph element in the example above has a `class` attribute within the opening tag of the` <p>` element. The `class` attribute is set to `'brand'`. To select this element using CSS, we can create a ruleset with a class selector of .brand.

```css
.brand {
}
```

To select an HTML element by its class using CSS, a period `(.)` must be prepended to the class’s name. In the example above, the class is `brand`, so the CSS selector for it is `.brand`.
