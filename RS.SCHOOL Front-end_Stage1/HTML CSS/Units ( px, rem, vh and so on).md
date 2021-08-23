#html/css

For some CSS properties, negative lengths are allowed.

There are two types of length units: **absolute** and **relative**.

## Absolute Lengths

| Unit  |	Description |
| ------|----------------|
| cm	| centimeters |
| mm	| millimeters |
| in	| inches (1in = 96px = 2.54cm) |
| px *  |	pixels (1px = 1/96th of 1in) |
| pt	| points (1pt = 1/72 of 1in) |
| pc	| picas (1pc = 12 pt) |

\* Pixels (px) are relative to the viewing device. For low-dpi devices, 1px is one device pixel (dot) of the display. For printers and high resolution screens 1px implies multiple device pixels.

## Relative Lengths

| Unit 	| Description 	|
|---	|---	|
| em 	| Relative to the font-size of the element (2em means 2 times the size of the current font) 	|
| ex 	| Relative to the x-height of the current font (rarely used) 	|
| ch 	| Relative to the width of the "0" (zero) 	|
| rem 	| Relative to font-size of the root element 	|
| vw 	| Relative to 1% of the width of the viewport* 	|
| vh 	| Relative to 1% of the height of the viewport* 	|
| vmin 	| Relative to 1% of viewport's* smaller dimension 	|
| vmax 	| Relative to 1% of viewport's* larger dimension 	|
| % 	| Relative to the parent element 	|

**Tip:** The em and rem units are practical in creating perfectly scalable layout!  
\* Viewport = the browser window size. If the viewport is 50cm wide, 1vw = 0.5cm.