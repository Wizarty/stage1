#grid #align

| horizontally(main axis)|vertically(cross-axis) | mix(main and cross axis) |
|----- |----- |----- |
|justify-content | align-items   | place-items|


----------

### Short grid


A shorthand for setting all of the following properties in a single declaration: `grid-template-rows`, `grid-template-columns`, `grid-template-areas`, `grid-auto-rows`, `grid-auto-columns`, and `grid-auto-flow` (Note: You can only specify the explicit or the implicit grid properties in a single grid declaration).

Values:

-   **`none`** – sets all sub-properties to their initial values.
-   **`<grid-template>`** – works the same as the `[grid-template](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-grid-template)` shorthand.
-   **`<grid-template-rows> / [ auto-flow && dense? ] <grid-auto-columns>?`** – sets `[grid-template-rows](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-grid-template-columns-rows)` to the specified value. If the `auto-flow` keyword is to the right of the slash, it sets `[grid-auto-flow](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-grid-auto-flow)` to `column`. If the `dense` keyword is specified additionally, the auto-placement algorithm uses a “dense” packing algorithm. If `[grid-auto-columns](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-grid-auto-columns-rows)` is omitted, it is set to `auto`.
-   **`[ auto-flow && dense? ] <grid-auto-rows>? / <grid-template-columns>`** – sets `[grid-template-columns](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-grid-template-columns-rows)` to the specified value. If the `auto-flow` keyword is to the left of the slash, it sets `[grid-auto-flow](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-grid-auto-flow)` to `row`. If the `dense` keyword is specified additionally, the auto-placement algorithm uses a “dense” packing algorithm. If `[grid-auto-rows](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-grid-auto-columns-rows)` is omitted, it is set to `auto`.

Examples:

The following two code blocks are equivalent:

```css
.container {
  grid: 100px 300px / 3fr 1fr;
}

.container {
  grid-template-rows: 100px 300px;
  grid-template-columns: 3fr 1fr;
}
```

The following two code blocks are equivalent:

```css
.container {
  grid: auto-flow / 200px 1fr;
}

.container {
  grid-auto-flow: row;
  grid-template-columns: 200px 1fr;
}
```

The following two code blocks are equivalent:

```css
.container {
  grid: auto-flow dense 100px / 1fr 2fr;
}

.container {
  grid-auto-flow: row dense;
  grid-auto-rows: 100px;
  grid-template-columns: 1fr 2fr;
}
```

And the following two code blocks are equivalent:

```css
.container {
  grid: 100px 300px / auto-flow 200px;
}

.container {
  grid-template-rows: 100px 300px;
  grid-auto-flow: column;
  grid-auto-columns: 200px;
}
```

It also accepts a more complex but quite handy syntax for setting everything at once. You specify `grid-template-areas`, `grid-template-rows` and `grid-template-columns`, and all the other sub-properties are set to their initial values. What you’re doing is specifying the line names and track sizes inline with their respective grid areas. This is easiest to describe with an example:

```css
.container {
  grid: [row1-start] "header header header" 1fr [row1-end]
        [row2-start] "footer footer footer" 25px [row2-end]
        / auto 50px auto;
}
```

That’s equivalent to this:

```css
.container {
  grid-template-areas: 
    "header header header"
    "footer footer footer";
  grid-template-rows: [row1-start] 1fr [row1-end row2-start] 25px [row2-end];
  grid-template-columns: auto 50px auto;    
}
```

-----------------
--------------------
-------------------

#### justify-items
row

Aligns grid items along the _inline (row)_ axis (as opposed to `align-items` which aligns along the _block (column)_ axis). This value applies to all grid items inside the container.

Values:

-   **`start`** – aligns items to be flush with the start edge of their cell
-   **`end`** – aligns items to be flush with the end edge of their cell
-   **`center`** – aligns items in the center of their cell
-   **`stretch`** – fills the whole width of the cell (this is the default)

```css
.container {
  justify-items: start | end | center | stretch;
}
```

Examples:

```css
.container {
  justify-items: start;
}
```

![Example of justify-items set to start](https://css-tricks.com/wp-content/uploads/2018/11/justify-items-start.svg)

```css
.container {
  justify-items: end;
}
```

![Example of justify-items set to end](https://css-tricks.com/wp-content/uploads/2018/11/justify-items-end.svg)

```css
.container {
  justify-items: center;
}
```

![Example of justify-items set to center](https://css-tricks.com/wp-content/uploads/2018/11/justify-items-center.svg)

```css
.container {
  justify-items: stretch;
}
```

![Example of justify-items set to stretch](https://css-tricks.com/wp-content/uploads/2018/11/justify-items-stretch.svg)

This behavior can also be set on individual grid items via the `justify-self` property.


#### align-items
column

Aligns grid items along the _block (column)_ axis (as opposed to `justify-items` which aligns along the _inline (row)_ axis). This value applies to all grid items inside the container.

Values:

-   **`start`** – aligns items to be flush with the start edge of their cell
-   **`end`** – aligns items to be flush with the end edge of their cell
-   **`center`** – aligns items in the center of their cell
-   **`stretch`** – fills the whole height of the cell (this is the default)

```css
.container {
  align-items: start | end | center | stretch;
}
```

Examples:

```css
.container {
  align-items: start;
}
```

![Example of align-items set to start](https://css-tricks.com/wp-content/uploads/2018/11/align-items-start.svg)

```css
.container {
  align-items: end;
}
```

![Example of align-items set to end](https://css-tricks.com/wp-content/uploads/2018/11/align-items-end.svg)

```css
.container {
  align-items: center;
}
```

![Example of align-items set to center](https://css-tricks.com/wp-content/uploads/2018/11/align-items-center.svg)

```css
.container {
  align-items: stretch;
}
```

![Example of align-items set to stretch](https://css-tricks.com/wp-content/uploads/2018/11/align-items-stretch.svg)

This behavior can also be set on individual grid items via the `align-self` property.

#### place-items

`place-items` sets both the `align-items` and `justify-items` properties in a single declaration.

Values:

-   **`<align-items>` / `<justify-items>`** – The first value sets `align-items`, the second value `justify-items`. If the second value is omitted, the first value is assigned to both properties.

All major browsers except Edge support the `place-items` shorthand property.

For more details, see `align-items` and `justify-items`.

This can be very useful for super quick multi-directional centering:

```css
.center {
  display: grid;
  place-items: center;
}
```


#### justify-content

Sometimes the total size of your grid might be less than the size of its grid container. This could happen if all of your grid items are sized with non-flexible units like `px`. In this case you can set the alignment of the grid within the grid container. This property aligns the grid along the _inline (row)_ axis (as opposed to `[align-content](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-align-content)` which aligns the grid along the _block (column)_ axis).

Values:

-   **`start`** – aligns the grid to be flush with the start edge of the grid container
-   **`end`** – aligns the grid to be flush with the end edge of the grid container
-   **`center`** – aligns the grid in the center of the grid container
-   **`stretch`** – resizes the grid items to allow the grid to fill the full width of the grid container
-   **`space-around`** – places an even amount of space between each grid item, with half-sized spaces on the far ends
-   `**space-between**` – places an even amount of space between each grid item, with no space at the far ends
-   **`space-evenly`** – places an even amount of space between each grid item, including the far ends

```css
.container {
  justify-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}
```

Examples:

```css
.container {
  justify-content: start;
}
```

![Example of justify-content set to start](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-start.svg)

```css
.container {
  justify-content: end;    
}
```

![Example of justify-content set to end](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-end.svg)

```css
.container {
  justify-content: center;    
}
```

![Example of justify-content set to center](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-center.svg)

```css
.container {
  justify-content: stretch;    
}
```

![Example of justify-content set to stretch](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-stretch.svg)

```css
.container {
  justify-content: space-around;    
}
```

![Example of justify-content set to space-around](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-space-around.svg)

```css
.container {
  justify-content: space-between;    
}
```

![Example of justify-content set to space-between](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-space-between.svg)

```css
.container {
  justify-content: space-evenly;    
}
```

![Example of justify-content set to space-evenly](https://css-tricks.com/wp-content/uploads/2018/11/justify-content-space-evenly.svg)

#### align-content

Sometimes the total size of your grid might be less than the size of its grid container. This could happen if all of your grid items are sized with non-flexible units like `px`. In this case you can set the alignment of the grid within the grid container. This property aligns the grid along the _block (column)_ axis (as opposed to `justify-content` which aligns the grid along the _inline (row)_ axis).

Values:

-   **`start`** – aligns the grid to be flush with the start edge of the grid container
-   **`end`** – aligns the grid to be flush with the end edge of the grid container
-   **`center`** – aligns the grid in the center of the grid container
-   **`stretch`** – resizes the grid items to allow the grid to fill the full height of the grid container
-   **`space-around`** – places an even amount of space between each grid item, with half-sized spaces on the far ends
-   **`space-between`** – places an even amount of space between each grid item, with no space at the far ends
-   **`space-evenly`** – places an even amount of space between each grid item, including the far ends

```css
.container {
  align-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}
```

Examples:

```css
.container {
  align-content: start;    
}
```

![Example of align-content set to start](https://css-tricks.com/wp-content/uploads/2018/11/align-content-start.svg)

```css
.container {
  align-content: end;    
}
```

![Example of align-content set to end](https://css-tricks.com/wp-content/uploads/2018/11/align-content-end.svg)

```css
.container {
  align-content: center;    
}
```

![Example of align-content set to center](https://css-tricks.com/wp-content/uploads/2018/11/align-content-center.svg)

```css
.container {
  align-content: stretch;    
}
```

![Example of align-content set to stretch](https://css-tricks.com/wp-content/uploads/2018/11/align-content-stretch.svg)

```css
.container {
  align-content: space-around;    
}
```

![Example of align-content set to space-around](https://css-tricks.com/wp-content/uploads/2018/11/align-content-space-around.svg)

```css
.container {
  align-content: space-between;    
}
```

![Example of align-content set to space-between](https://css-tricks.com/wp-content/uploads/2018/11/align-content-space-between.svg)

```css
.container {
  align-content: space-evenly;    
}
```

![Example of align-content set to space-evenly](https://css-tricks.com/wp-content/uploads/2018/11/align-content-space-evenly.svg)

#### place-content

`place-content` sets both the `align-content` and `justify-content` properties in a single declaration.

Values:

-   **`<align-content>` / `<justify-content>`** – The first value sets `align-content`, the second value `justify-content`. If the second value is omitted, the first value is assigned to both properties.

All major browsers except Edge support the `place-content` shorthand property.

For more details, see `align-content` and `justify-content`.