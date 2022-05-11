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

## 4.Multiple Classes

We can use CSS to select an HTML element’s `class` attribute by name. And so far, we’ve selected elements using only one class name per element. If every HTML element had a single class, all the style information for each element would require a new class.

Luckily, it’s possible to add more than one class name to an HTML element’s class attribute.

For instance, perhaps there’s a heading element that needs to be green and bold. You could write two CSS rulesets like so:

```css
.green {
  color: green;
}

.bold {
  font-weight: bold;
}
```

Then, you could include both of these classes on one HTML element like this:

```html
<h1 class="green bold">...</h1>
```

We can add multiple classes to an HTML element’s `class` attribute by separating them with a space. This enables us to mix and match CSS classes to create many unique styles without writing a custom class for every style combination needed.

## 5. ID

Oftentimes it’s important to select a single element with CSS to give it its own unique style. If an HTML element needs to be styled uniquely, we can give it an ID using the `id` attribute.

```html
<h1 id="large-title">...</h1>
```

In contrast to `class` which accepts multiple values, and can be used broadly throughout an HTML document, an element’s `id` can only have a single value, and only be used once per page.

To select an element’s ID with CSS, we prepend the id name with a number sign `(#)`. For instance, if we wanted to select the HTML element in the example above, it would look like this:

```css
#large-title {
}
```

The `id` name is `large-title`, therefore the CSS selector for it is `#large-title`.

## 6. Attribute

You may remember that some HTML elements use `attributes` to add extra detail or functionality to the element. Some familiar attributes may be `href` and `src`, but there are many more—including `class` and `id`!

The `attribute` selector can be used to target HTML elements that already contain attributes. Elements of the same type can be targeted differently by their attribute or attribute value. This alleviates the need to add new code, like the `class` or `id` attributes.

Attributes can be selected similarly to types, classes, and IDs.

```css
[href] {
  color: magenta;
}
```

The most basic syntax is an attribute surrounded by square brackets. In the above example: `[href]` would target all elements with an `href` attribute and set the `color` to `magenta`.

And it can get more granular from there by adding type and/or attribute values. One way is by using `type[attribute*=value]`. In short, this code selects an element where the attribute contains any instance of the specified value. Let’s take a look at an example.

```html
<img src="/images/seasons/cold/winter.jpg" />
<img src="/images/seasons/warm/summer.jpg" />
```

The HTML code above renders two `<img>` elements, each containing a `src` attribute with a value equaling a link to an image file.

```css
img[src*="winter"] {
  height: 50px;
}

img[src*="summer"] {
  height: 100px;
}
```

Now take a look at the above CSS code. The attribute selector is used to target each image individually.

- The first ruleset looks for an img element with an attribute of `src` that contains the string `'winter'`, and sets the `height` to `50px`.
- The second ruleset looks for an img element with an attribute of `src` that contains the string `'summer'`, and sets the `height` to `100px`.

Notice how no new HTML markup (like a `class` or `id`) needed to be added, and we were still able to modify the styles of each image independently. This is one advantage to using the attribute selector!

## 7. Pseudo-class

You may have observed how the appearance of certain elements can change, or be in a different state, after certain user interactions. For instance:

- When you click on an `<input>` element, and a blue border is added showing that it is in focus.
- When you click on a blue `<a>` link to visit to another page, but when you return the link’s text is purple.
- When you’re filling out a form and the submit button is grayed out and disabled. But when all of the fields have been filled out, the button has color showing that it’s active.

These are all examples of pseudo-class selectors in action! In fact, `:focus`, `:visited`, `:disabled`, and `:active` are all pseudo-classes. Factors such as user interaction, site navigation, and position in the document tree can all give elements a different state with pseudo-class.

A pseudo-class can be attached to any selector. It is always written as a colon `:` followed by a name. For example` p:hover`.

```css
p:hover {
  background-color: lime;
}
```

In the above code, whenever the mouse hovers over a paragraph element, that paragraph will have a lime-colored background.

## 8. Classes and IDs

CSS can select HTML elements by their type, class, and ID. CSS classes and IDs have different purposes, which can affect which one you use to style HTML elements.

CSS classes are meant to be reused over many elements. By writing CSS classes, you can style elements in a variety of ways by mixing classes. For instance, imagine a page with two headlines. One headline needs to be bold and blue, and the other needs to be bold and green. Instead of writing separate CSS rules for each headline that
repeat each other’s code, it’s better to write a `.bold` CSS rule, a `.green` CSS rule, and a `.blue` CSS rule. Then you can give one headline the `bold green` classes, and the other the `bold blue` classes.

While classes are meant to be used many times, an ID is meant to style only one element. As you’ll learn in the next exercise, IDs override the styles of types and classes. Since IDs override these styles, they should be used sparingly and only on elements that need to always appear the same.

## 9. Specificity

Specificity is the order by which the browser decides which CSS styles will be displayed. A best practice in CSS is to style elements while using the lowest degree of specificity so that if an element needs a new style, it is easy to override.

IDs are the most specific selector in CSS, followed by classes, and finally, type. For example, consider the following HTML and CSS:

```html
<h1 class="headline">Breaking News</h1>
```

```css
h1 {
  color: red;
}

.headline {
  color: firebrick;
}
```

In the example code above, the color of the heading would be set to `firebrick`, as the class selector is more specific than the type selector. If an ID attribute (and selector) were added to the code above, the styles within the ID selector’s body would override all other styles for the heading.

Over time, as files grow with code, many elements may have IDs, which can make CSS difficult to edit since a new, more specific style must be created to change the style of an element.

To make styles easy to edit, it’s best to style with a type selector, if possible. If not, add a class selector. If that is not specific enough, then consider using an ID selector.

## 10. Chaining

When writing CSS rules, it’s possible to require an HTML element to have two or more CSS selectors at the same time.

This is done by combining multiple selectors, which we will refer to as chaining. For instance, if there was a `special` class for `<h1>` elements, the CSS would look like below:

```css
h1.special {
}
```

The code above would select only the `<h1>` elements with a class of `special`. If a `<p>` element also had a class of `special`, the rule in the example would not style the paragraph.

## 11. Descendant Combinator

In addition to chaining selectors to select elements, CSS also supports selecting elements that are nested within other HTML elements, also known as descendants. For instance, consider the following HTML:

```html
<ul class="main-list">
  <li>...</li>
  <li>...</li>
  <li>...</li>
</ul>
```

The nested `<li>` elements are descendants of the `<ul>` element and can be selected with the descendant combinator like so:

```css
.main-list li {
}
```

In the example above, `.main-list` selects the element with the `.main-list` class (the `<ul>` element). The descendant `<li>`‘s are selected by adding `li` to the selector, separated by a space. This results in `.main-list` `li` as the final selector.

Selecting elements in this way can make our selectors even more specific by making sure they appear in the context we expect.

## 12. Chaining and Specificity

In the last exercise, instead of selecting all `<h5>` elements, you selected only the `<h5>` elements nested inside the `.description` elements. This CSS selector was more specific than writing only `h5`. Adding more than one tag, class, or ID to a CSS selector increases the specificity of the CSS selector.

For instance, consider the following CSS:

```css
p {
  color: blue;
}

.main p {
  color: red;
}
```

Both of these CSS rules define what a `<p>` element should look like. Since `.main` `p` has a class and a `p` type as its selector, only the `<p>` elements inside the `.main` element will appear `red`. This occurs despite there being another more general rule that states `<p>` elements should be `blue`.
