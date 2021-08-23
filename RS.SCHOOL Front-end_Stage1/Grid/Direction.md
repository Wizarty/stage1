#grid

## grid-auto-flow
If you have grid items that you don’t explicitly place on the grid, the _auto-placement algorithm_ kicks in to automatically place the items. This property controls how the auto-placement algorithm works.

Values:

-   **`row`** – tells the auto-placement algorithm to fill in each row in turn, adding new rows as necessary (default)
-   **`column`** – tells the auto-placement algorithm to fill in each column in turn, adding new columns as necessary
-   **`dense`** – tells the auto-placement algorithm to attempt to fill in holes earlier in the grid if smaller items come up later