# Box model

## Box model

"layers" of block elements from innermost to outermost:

- content
- padding
- border
- margin

## Box model

example: two boxes

## Box model

sizing the content:

- `height` / `width`
- `min-height` / `min-width`
- `max-height` / `max-width`

if we specify a percentage amount (e.g. `width: 50%`) the size is relative to the parent element

## Box model

By default the attributes `height`, `width`, ... apply to the content (without padding or border)

In modern CSS we often set:

```css
* {
  box-sizing: border-box;
}
```

This means these attributes will refer to the total size (including padding and border, not including margin)

## Setting padding and margin

- setting all four margins to the same value:  
  `margin: 10px;`
- setting all four margins individually:  
  `margin: 10px 20px 30px 40px` (top - right - bottom - left)
- setting vertical and horizontal margins:  
  `margin: 10px 20px;` (top and bottom - left and right)
- setting horizontal margin automatically (horizontal centering):
  `margin: 10px auto;`
- setting margins individually:  
  `maring: 10px; margin-left: 20px;`

## Box model

border (example): `border: 10px solid blue`

rounded corners: `border-radius: 5px`

## Margin and padding on inline elements

Note: vertical margin and padding will not influence the positioning of inline elements (and may cause overlaps)

## Example: horizontal centering

```css
div {
  width: 800px;
  margin: auto;
}
```

```css
div {
  max-width: 800px;
  margin: auto;
}
```

## Example: full height body

By default the document body will be ass tall as its content

If the body should take up the entire screen height:

```css
body {
  height: 100vh;
}
```

## Tables and cell borders

By default every cell in a table has its own border

"collapsing" the borders of adjacent cells:

```css
table {
  border-collapse: collapse;
}
```
