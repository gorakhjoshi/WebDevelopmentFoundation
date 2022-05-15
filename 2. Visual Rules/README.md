# Introduction To Visual Rules

The purpose of CSS is to add style to web page, and each element on the page can have many style properties. Some of the basic properties relate to the size, style, and color of the element. In this lesson, you’ll learn some fundamental CSS visual rules that you can use to start styling web page elements!

## 1. Font Family

If you’ve ever used word processing software, like Microsoft Word or Google Docs, chances are that you probably also used a feature that allowed you to change the font you were typing in. Font refers to the technical term typeface, or `font family`.

To change the typeface of text on your web page, you can use the font-family property.

```css
h1 {
  font-family: Garamond;
}
```

In the example above, the `font family` for all main heading elements has been set to Garamond.

When setting typefaces on a web page, keep the following points in mind:

- The font specified must be installed on the user’s computer or downloaded with the site.
- Web safe fonts are a group of fonts supported across most browsers and operating systems.
- Unless you are using web safe fonts, the font you choose may not appear the same between all browsers and operating systems.
- When the name of a typeface consists of more than one word, it’s a best practice to enclose the typeface’s name in quotes, like so:

```css
h1 {
  font-family: "Courier New";
}
```

## 2. Font Size

Changing the typeface isn’t the only way to customize the text. Oftentimes, different sections of a web page are highlighted by modifying the font size.

To change the size of text on your web page, you can use the font-size property.

```css
p {
  font-size: 18px;
}
```

In the example above, the `font-size` of all paragraphs was set to `18px`. `px` means pixels, which is one way to measure font size.

## 3. Font Weight

In CSS, the `font-weight` property controls how bold or thin text appears.

```css
p {
  font-weight: bold;
}
```

In the example above, all paragraphs on the web page would appear bolded.

The `font-weight` property has another value: `normal`. Why does it exist?

If we wanted all text on a web page to appear bolded, we could select all text elements and change their font weight to `bold`. If a certain section of text was required to appear `normal`, however, we could set the font weight of that particular element to normal, essentially shutting off bold for that element.

## 4. Text Align

No matter how much styling is applied to text (typeface, size, weight, etc.), the text always appears on the left side of the container in which it resides.

To align text we can use the `text-align` property. The `text-align` property will align text to the element that holds it, otherwise known as its parent.

```css
h1 {
  text-align: right;
}
```

The `text-align` property can be set to one of the following commonly used values:

- `left` — aligns text to the left side of its parent element, which in this case is the browser.
- `center` — centers text inside of its parent element.
- `right` — aligns text to the right side of its parent element.
- `justify` — spaces out text in order to align with the right and left side of the parent element.

## 5. Color and Background Color

Before discussing the specifics of color, it’s important to make two distinctions about color. Color can affect the following design aspects:

- Foreground color
- Background color

Foreground color is the color that an element appears in. For example, when a heading is styled to appear green, the foreground color of the heading has been styled. Conversely, when a heading is styled so that its background appears yellow, the background color of the heading has been styled.

In CSS, these two design aspects can be styled with the following two properties:

`color`: this property styles an element’s foreground color
`background-color`: this property styles an element’s background color

```css
h1 {
  color: red;
  background-color: blue;
}
```

In the example above, the text of the heading will appear in `red`, and the background of the heading will appear `blue`.

## 6. Opacity

Opacity is the measure of how transparent an element is. It’s measured from 0 to 1, with 1 representing 100%, or fully visible and opaque, and 0 representing 0%, or fully invisible.

Opacity can be used to make elements fade into others for a nice overlay effect. To adjust the opacity of an element, the syntax looks like this:

```css
.overlay {
  opacity: 0.5;
}
```

In the example above, the `.overlay` element would be 50% visible, letting whatever is positioned behind it show through.

## 7. Background Image

CSS has the ability to change the background of an element. One option is to make the background of an element an image. This is done through the CSS property `background-image`. Its syntax looks like this:

```css
.main-banner {
  background-image: url("https://www.example.com/image.jpg");
}
```

1. The `background-image` property will set the element’s background to display an image.
2. The value provided to `background-image` is a `url`. The `url` should be a `URL` to an image. The url can be a file within your project, or it can be a link to an external site. To link to an image inside an existing project, you must provide a relative file path. If there was an image folder in the project, with an image named `mountains.jpg`, the relative file path would look like below:

```css
.main-banner {
  background-image: url("images/mountains.jpg");
}
```

## 8. Important

`!important` can be applied to specific declarations, instead of full rules. It will override any style no matter how specific it is. As a result, it should almost never be used. Once `!important` is used, it is very hard to override.

The syntax of `!important` in CSS looks like this:

```css
p {
  color: blue !important;
}

.main p {
  color: red;
}
```

Since `!important` is used on the `p` selector’s `color` attribute, all `p` elements will appear `blue`, even though there is a more specific `.main p` selector that sets the `color` attribute to `red`.

One justification for using `!important` is when working with multiple stylesheets. For example, if we are using the `Bootstrap` CSS framework and want to override the styles for one specific HTML element, we can use the `!important` property.
