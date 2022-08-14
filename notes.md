# Selectors
There are different selectors in CSS. To select all of a particular tag, just use the tag name. e.g. if you want to select all <p> then use
```css
p {
    ...
}
```

To select by ID, use the `#` character. To select something with the id `para1` use
```css
#para1 {
    ...
}
```

To select everything of a given class, use the `.` character.
```css
.className {
    ...
}
```

You can combine the element with the class selector. e.g. if you want to select all <p class="center"> tags
```css
p.center {
    ...
}
```

This will select any element with the class name of `one` OR `two`
```css
.one,.two{
    ...
}
```

This will select any element with the class name of `one` AND `two`.
```css
.one.two {
    background-color: chocolate;
}
```

# comments
CSS uses c-style comments of
```
/* comment text */
```

# The box model

outlines take place outside the border, in the same space as the margin. Your 
outline can fill your entire margin. Although you can add space inbetween the border and the outline using the outline-offset

The order from outside in is: 
- outline/margin
- border
- padding
- content


# buttons
You can fuzz the border around a button and make it hazy by adding a drop-shadow

Buttons have three states:
- hover - when a user hovers the mouse over the button without clicking it. This only works on desktops.
- focus - when a user gets keyboard focus over the button. Browsers have default styling for this 
- active - when the button actually gets clicked. When activiated, a button is also in focus.

Use the pseudoclass selector `:hover` fo style it. e.g.
```css
.button.hover {
    background-color
}
```

You should style each differently so you can tell the difference.
You can also make the result more blended by adding a transition time.


# Fonts

There are 5 generic font families

    1. Serif fonts have a small stroke at the edges of each letter. They create a sense of formality and elegance.
    1. Sans-serif fonts have clean lines (no small strokes attached). They create a modern and minimalistic look.
    1. Monospace fonts - here all the letters have the same fixed width. They create a mechanical look. 
    1. Cursive fonts imitate human handwriting.
    1. Fantasy fonts are decorative/playful fonts.

You can't gaurantee that the fonts are installed on your users computer, so you should always specify multiple, similar fonts.

https://www.w3schools.com/css/css_font_fallbacks.asp

If you specifiy an absolute text size in pixels, then some users may not be able to resize them which is bad for accessibility.

`1em` is equal to the default font size. On most browsers that is 16px so 1em=16px.

Google fonts offer 1000 free fonts you can choose from.

Add this in your HTML head to use the font `sofia`.
```html
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
<style>
body {
  font-family: "Sofia", sans-serif;
}
</style>
</head>
```

To use multiple
```html
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide|Sofia|Trirong">
<style>
h1.a {font-family: "Audiowide", sans-serif;}
h1.b {font-family: "Sofia", sans-serif;}
h1.c {font-family: "Trirong", serif;}
</style>
</head>
```

# Display

Display determines how elements are displayed? 

**Block** starts on a new line and takes up all the room available
**Inline** does not start on a new line and only takes as much space as necessary
**None** used to hide elements. When this happens the page will display as if the element did not exist and did not take any space. This is different than the `visibility: hidden` property which makes an element invisible, but it still occupies space.

# Position
There are five possible position values:
**static** The default for all elements. Nothing special, just done according to the flow of the page.
**relative** adjusted relative to it's `static` position. 
**fixed** positioned relative to the viewport meaning it always stays in the same place even if the page is scrolled. 
**absolute** positioned relative to the nearest ancestor. absolute are removed from the normal flow and can overlap.
**sticky** based on the user's scroll position. it toggles between relative and fixed.

# Flexbox


# Interesting HTML tags I didn't know about

**main** - strictly informative to mark the main, unique content of the page
**navbar** - way to group links, good for screen readers to skip
**header**

# Tailwind
```bash
npm install -D tailwindcss

npx tailwindcss init
```

You create a css src file and then use tailwind to convert that to your public file.

```bash
tailwindcss build src/styles.css -o public/styles.css
```
By default tailwind strips all default browser styles out of everything.



# Questions:
What is 
```css
:root {
    ...
}
```
