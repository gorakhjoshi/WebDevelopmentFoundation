# Quiz.....

### Q1.What is one limitation of named CSS colors that hexadecimal and RGB colors do not have?

- [ ] A. Named CSS colors are obsolete.
- [ ] B. Named colors have no limitations compared with RGB or hexadecimal colors.
- [ ] C. Named colors are only supported by some browsers.
- [ ] D. Named CSS colors are limited to a specific set and cannot represent the full color palette.

### Q2.How could this code be re-written but guarantee the same appearance in the browser?

```css
body h1 {
  color: #bb44ff;
}
```

- [ ] A.

```css
body h1 {
  color: rgb("#BB44FF");
}
```

- [ ] B.

```css
body h1 {
  background-color: #bb44ff;
}
```

- [ ] C.

```css
body h1 {
  color: #b4f;
}
```

- [ ] D.

```css
h1 {
  color: #bb44ff;
}
```

### Q3.The following CSS code attempts to set the color of a paragraph using an HSL color, but fails to do so. Why?

```css
p {
  color: hsl(65, -5, -4);
}
```

- [ ] A. The `hsl()` property should be set to `rgb()`.
- [ ] B. The saturation and lightness value must be positive percentages.
- [ ] C. The foreground color of an element cannot be set using an HSL color.
- [ ] D. The `hsl` characters must be capitalized `HSL()`.

### Q4.The following CSS code attempts to set the text color of a paragraph using a named color, but fails to do so. Why?

```css
p {
  color: bold;
}
```

- [ ] A. The `color` property only accepts HEX or RGB color values.
- [ ] B. `bold` is not a valid color keyword in CSS.
- [ ] C. The `color` property should be changed to `background-color`.
- [ ] D. The `color` property should be changed to `foreground-color`.

### Q5.The following CSS code attempts to set the color of a paragraph using an RGB color, but fails to do so. Why?

```css
p {
  color: rgb(277, 56, FF);
}
```

- [ ] A. The three parameters of the `rgb()` property must be numbers between 0 and 255.
- [ ] B. The `rgb` characters must be capitalized `RGB()`.
- [ ] C. No `()` are required for `rgb()`.
- [ ] D. The `rgb()` property should be set to `hex()`.

### Q6.Which of the following two CSS properties are used to set an HTML element’s foreground color and background color, respectively?

- [ ] A. `color-foreground` and `color-background`
- [ ] B. `color-front` and `color-back`
- [ ] C. `color` and `background-color`
- [ ] D. `foreground-color` and `background-color`

### Q7.What does the fourth value inside rgba() control?

```css
body {
  background-color: rgba(212, 34, 99, 0.75);
}
```

- [ ] A. `Opacity`, or `alpha value`.
- [ ] B. How close or far away the element appears.
- [ ] C. Saturation.
- [ ] D. The code includes invalid syntax.
