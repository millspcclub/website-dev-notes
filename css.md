# CSS Notes:
- Cascading Style Sheets!
  - CSS basically allows you to mass add attributes to html tags
- CSS format:
```css
selector {
   property: value;
   property: value;
}
```
## There are 3 basic selectors:

1. type selectors: used to select HTML elements by element name. This is like your h1, p, a, etc. Your selector will simply be the name of the tag.
2. class selectors: used to select HTML elements by a specific class value. classes can be added to html tags by using the class attribute. html tags may have as many classes as you want. Your selector will be a `.` followed by the class name, like `.blueBackground`
3. id selectors: used to select an HTML element associated with a specific id value. IDs can be added to html tags by using the id attribute. You may only use an id once, and you can only assign one id to each tag! Your selector will be a `#` followed by the id name, like `#blueButton`
Type selectors will be applied first, then class, then id. Within each group, the *most specific* group gets applied. If you have the following css:
```css
body {
    background: red;
}
.myText {
    background: blue;
}
h1 {
    background: green;
}
```
a `p` tag with myText class will be colored blue, a `p` tag within the body but not a `.myText` class will color the background green as it is more specific, and everywhere else on the page will be red as neither the `.myText` class nor the `h1` or `body` tag applies.

New properties:

- `background` - background color like `red`
- `color` - color of text like `white`
- `font-family` - font of text, like `Arial`
- `text-align` - align left, right, center.
