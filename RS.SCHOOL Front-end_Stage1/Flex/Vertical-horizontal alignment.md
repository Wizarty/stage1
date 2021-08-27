#flex #align

#### justify-content: center;  - center items vertically, in this case 

#### align-items: center;     - center items horizontally, in this case 

------------

## justify-content
 for container
** main axis**
 
```css
justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe;
```

![image](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)

-   `flex-start` (default): items are packed toward the start of the flex-direction.
-   `flex-end`: items are packed toward the end of the flex-direction.
-   `start`: items are packed toward the start of the `writing-mode` direction.
-   `end`: items are packed toward the end of the `writing-mode` direction.
-   `left`: items are packed toward left edge of the container, unless that doesn’t make sense with the `flex-direction`, then it behaves like `start`.
-   `right`: items are packed toward right edge of the container, unless that doesn’t make sense with the `flex-direction`, then it behaves like `end`.
-   `center`: items are centered along the line
-   `space-between`: items are evenly distributed in the line; first item is on the start line, last item on the end line
-   `space-around`: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
-   `space-evenly`: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

<details> 
	<summary>same local image</summary>
	![image](images/justify-content.svg) 
</details>

#### align-content
for container
**cross-axis**

```css
align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;
```

![](https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg)

-   `normal` (default): items are packed in their default position as if no value was set.
-   `flex-start` / `start`: items packed to the start of the container. The (more supported) `flex-start` honors the `flex-direction` while `start` honors the `writing-mode` direction.
-   `flex-end` / `end`: items packed to the end of the container. The (more support) `flex-end` honors the `flex-direction` while end honors the `writing-mode` direction.
-   `center`: items centered in the container
-   `space-between`: items evenly distributed; the first line is at the start of the container while the last one is at the end
-   `space-around`: items evenly distributed with equal space around each line
-   `space-evenly`: items are evenly distributed with equal space around them
-   `stretch`: lines stretch to take up the remaining space

The `safe` and `unsafe` modifier keywords can be used in conjunction with all the rest of these keywords (although note [browser support](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)), and deal with helping you prevent aligning elements such that the content becomes inaccessible.

#### align-items
 for container
 **cross-axis**
 
````css
align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
````

![](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)

-   `stretch` (default): stretch to fill the container (still respect min-width/max-width)
-   `flex-start` / `start` / `self-start`: items are placed at the start of the cross axis. The difference between these is subtle, and is about respecting the `flex-direction` rules or the `writing-mode` rules.
-   `flex-end` / `end` / `self-end`: items are placed at the end of the cross axis. The difference again is subtle and is about respecting `flex-direction` rules vs. `writing-mode` rules.
-   `center`: items are centered in the cross-axis
-   `baseline`: items are aligned such as their baselines align