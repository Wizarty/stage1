#grid #align

#### justify-self

Aligns a grid item inside a cell along the _inline (row)_ axis (as opposed to `align-self` which aligns along the _block (column)_ axis). This value applies to a grid item inside a single cell.

Values:

-   **`start`** – aligns the grid item to be flush with the start edge of the cell
-   **`end`** – aligns the grid item to be flush with the end edge of the cell
-   **`center`** – aligns the grid item in the center of the cell
-   **`stretch`** – fills the whole width of the cell (this is the default)

```css
.item {
  justify-self: start | end | center | stretch;
}
```

Examples:

```css
.item-a {
  justify-self: start;
}
```

![Example of justify-self set to start](https://css-tricks.com/wp-content/uploads/2018/11/justify-self-start.svg)

```css
.item-a {
  justify-self: end;
}
```

![alt="Example](https://css-tricks.com/wp-content/uploads/2018/11/justify-self-end.svg)

```css
.item-a {
  justify-self: center;
}
```

![Example of justify-self set to center](https://css-tricks.com/wp-content/uploads/2018/11/justify-self-center.svg)

```css
.item-a {
  justify-self: stretch;
}
```

![Example of justify-self set to stretch](https://css-tricks.com/wp-content/uploads/2018/11/justify-self-stretch.svg)

To set alignment for _all_ the items in a grid, this behavior can also be set on the grid container via the `justify-items` property.