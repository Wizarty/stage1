#grid

#### grid-column-start  
#### grid-column-end  
#### grid-row-start  
#### grid-row-end

Determines a grid item’s location within the grid by referring to specific grid lines. `grid-column-start`/`grid-row-start` is the line where the item begins, and `grid-column-end`/`grid-row-end` is the line where the item ends.

Values:

-   **`<line>`** – can be a number to refer to a numbered grid line, or a name to refer to a named grid line
-   **`span <number>`** – the item will span across the provided number of grid tracks
-   **`span <name>`** – the item will span across until it hits the next line with the provided name
-   **`auto`** – indicates auto-placement, an automatic span, or a default span of one

```css
.item {
  grid-column-start: <number> | <name> | span <number> | span <name> | auto;
  grid-column-end: <number> | <name> | span <number> | span <name> | auto;
  grid-row-start: <number> | <name> | span <number> | span <name> | auto;
  grid-row-end: <number> | <name> | span <number> | span <name> | auto;
}
```

Examples:

```css
.item-a {
  grid-column-start: 2;
  grid-column-end: five;
  grid-row-start: row1-start;
  grid-row-end: 3;
}
```

![Example of grid-row/column-start/end](https://css-tricks.com/wp-content/uploads/2018/11/grid-column-row-start-end-01.svg)

```css
.item-b {
  grid-column-start: 1;
  grid-column-end: span col4-start;
  grid-row-start: 2;
  grid-row-end: span 2;
}
```

![Example of grid-row/column-start/end](https://css-tricks.com/wp-content/uploads/2018/11/grid-column-row-start-end-02.svg)

If no `grid-column-end`/`grid-row-end` is declared, the item will span 1 track by default.

Items can overlap each other. You can use `z-index` to control their stacking order.

#### grid-column  
#### grid-row

Shorthand for `grid-column-start` + `grid-column-end`, and `grid-row-start` + `grid-row-end`, respectively.

Values:

-   **`<start-line>` / `<end-line>`** – each one accepts all the same values as the longhand version, including span

```css
.item {
  grid-column: <start-line> / <end-line> | <start-line> / span <value>;
  grid-row: <start-line> / <end-line> | <start-line> / span <value>;
}
```

Example:

```css
.item-c {
  grid-column: 3 / span 2;
  grid-row: third-line / 4;
}
```

![Example of grid-column/grid-row](https://css-tricks.com/wp-content/uploads/2018/11/grid-column-row.svg)

If no end line value is declared, the item will span 1 track by default.

#### grid-area

Gives an item a name so that it can be referenced by a template created with the `grid-template-areas` property. Alternatively, this property can be used as an even shorter shorthand for `grid-row-start` + `grid-column-start` + `grid-row-end` + `grid-column-end`.

Values:

-   **`<name>`** – a name of your choosing
-   **`<row-start>` / `<column-start>` / `<row-end>` / `<column-end>`** – can be numbers or named lines

```css
.item {
  grid-area: <name> | <row-start> / <column-start> / <row-end> / <column-end>;
}
```

Examples:

As a way to assign a name to the item:

```css
.item-d {
  grid-area: header;
}
```

As the short-shorthand for `grid-row-start` + `grid-column-start` + `grid-row-end` + `grid-column-end`:

```css
.item-d {
  grid-area: 1 / col4-start / last-line / 6;
}
```

![Example of grid-area](https://css-tricks.com/wp-content/uploads/2018/11/grid-area.svg)