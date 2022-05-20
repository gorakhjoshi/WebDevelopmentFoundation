# Selectors: Quiz
### Q1. Which of the following statements is correct?

- [ ] A. Multiple classes are more specific than ID's and tags.
- [ ] B. Tags are more specific than ID's and classes.
- [ ] C. Classes are more specific than ID's and tags.
- [ ] D. ID's are more specific than classes and tags.

### Q2. What does the `<style> HTML` tag allow?

- [ ] A. Writing one or more CSS rules in CSS syntax inside an HTML file.
- [ ] B. It is the only way to apply styles inside an HTML file.
- [ ] C. It links external CSS files to the HTML document.
- [ ] D. It automatically adds common styles to your webpage.

### Q3. What is the purpose of the HTML `<link>` tag when it comes to styling a page?

- [ ] A. To make sure that all links are styled correctly on the page.
- [ ] B. To make sure that your inline styles are applied correctly.
- [ ] C. To determine the specificity of CSS rules.
- [ ] D. To link a specific stylesheet file to an HTML file so that the styles get applied on the page.

### Q4. What is the correct syntax to select an element inside another element?

- [ ] A.

```css
.main-list_li {
}
```

- [ ] B.

```css
.main-list li {
}
```

- [ ] C.

```css
.main-list,
li {
}
```

- [ ] D.

```css
li.main-list {
}
```

### Q5. What is the correct syntax to style multiple unrelated selectors?

- [ ] A.

```css
p.nav-menu {
}
```

- [ ] B.

```css
.nav-menu;
p {
}
```

- [ ] C.

```css
.nav-menu,
p {
}
```

- [ ] D.

```css
.nav-menu p {
}
```

### Q6. Which of the following best describes the concept of CSS selector specificity?

- [ ] A. Specificity refers to how a browser decides which styles to display when there are multiple styles defined that could apply to the same element.
- [ ] B. Specificity refers to how descriptively you write your class or ID names.
- [ ] C. Specificity refers to the order in which HTML elements appear in the browser immediately after rendering.
- [ ] D. Specificity refers to whether you style multiple selectors for the same rule.

### Q7. The following code attempts to style a paragraph using the `<style>` tag, but fails to do so. Why?

```html
<head>
  <style>
    <p style="color:red;">I'm learning to code!</p>
  </style>
</head>
```

- [ ] A. - The `color` attribute must be changed to `color-style`.
- [ ] B. - The contents of the `<style>` tag must be CSS code, not HTML code. The `<p>` will not appear at all.
- [ ] C. - You must use either inline styles or the `<style>` tag but not both.
- [ ] D. - The style attribute of the `<p>` element can be removed because the `<style>` tag replaces it.

### Q8. Complete the code below to link a CSS file called main.css to an HTML file.

`<link ______ = ______ ______ = _______ >`

- [ ] A. `'stylesheet'`
- [ ] B. `type`
- [ ] C. `text/css`
- [ ] D.` rel`
- [ ] E. `href`
- [ ] F. `'main.css'`

### Q9. What is the most specific selector in the code below?

```css
p {
}

#side-bar {
}

.main-content {
}

.main-content p {
}
```

- [ ] A. `#side-bar`
- [ ] B. `.main-content`
- [ ] C. `p`
- [ ] D. `.main-content p`

### Q10. What is the main difference between inline styles and the `<style>` tag?

- [ ] A. Inline styles directly modify individual HTML elements using a `style` attribute, whereas the `<style>` tag allows you to write CSS in a dedicated section of the HTML file.
- [ ] B. There is no difference between inline styles and the `<style>` tag.
- [ ] C. The `<style>` tag allow you to write CSS in a separate file, whereas inline styles embed CSS directly within HTML opening tags.
- [ ] D. Inline styles allow you to write CSS in a separate file, whereas the `<style>` tag embeds CSS directly within HTML opening tags.

### Q11. Separating HTML and CSS into their own files helps accomplish which of the following?

- [ ] A. More specific CSS selectors.
- [ ] B. Better-looking CSS styles.
- [ ] C. Enhances webpage load time.
- [ ] D. Separating HTML structure from CSS style makes the code in both languages easier to read and maintain.
