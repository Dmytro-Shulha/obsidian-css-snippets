```css
/* Sidenote in line with the main text */
aside {
  float: right;
  border: 1px solid lightgrey;
  padding: 8px;
  padding-top: 0px;
  position: relative;
  left: 10px;
  top: 5px;
  width: 300px; /*PB changed from 155px */
  box-shadow: 5px 10px 10px 2px rgba(119, 119, 119, 0.3);
  color: var(--text-accent);
  font-size: 14px;
  border-radius: 4px;
}
```

```css
/* to put the sidenote in the right gutter, add this rule to the code above */
margin-right: -20em;
```
