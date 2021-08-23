#grid

The `fr` unit (a “fraction”) can be used when defining grids like any other [CSS length](https://css-tricks.com/the-lengths-of-css/) such as `%`, `px` or `em`. Let’s quickly refactor the code above to use this peculiar new value:

```css
.grid { 
display: grid; 
grid-template-columns: repeat(4, 25%); 
grid-column-gap: 10px; 
}
```

Result:
![[Pasted image 20210824001528.png]]

```css
.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-column-gap: 10px;
}
```

Result:
![[Pasted image 20210824001425.png]]


the width of each column = ((width of viewport - width of nav) / number of columns) \* 1%

```css 
.grid { 
display: grid; 
grid-template-columns: 250px repeat(12, 1fr); 
grid-column-gap: 10px; 
}
```

Result:
![[Pasted image 20210824001938.png]]

Mixed used:
![](https://i2.wp.com/css-tricks.com/wp-content/uploads/2017/06/alligator-grid.png?ssl=1)