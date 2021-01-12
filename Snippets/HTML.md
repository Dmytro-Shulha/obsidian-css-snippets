# HTML
```css
/* HTML in editor */
/* html tags in editor */
.cm-s-obsidian span.cm-tag {
  color: var(--base4);
}

/* html comments in editor */
.cm-s-obsidian span.cm-comment {
  color: var(--base4);
}

/* Disclosure widget for a block ot text */
/* Source: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details#Providing_a_summary */
details {
  font: 16px "Open Sans", Calibri, sans-serif;
  width: 620px;
}

details > summary {
  padding: 2px 6px;
  width: 15em;
  background-color: #ddd;
  border: none;
  box-shadow: 3px 3px 4px black;
  cursor: pointer;
}

details > p {
  border-radius: 0 0 10px 10px;
  background-color: #ddd;
  padding: 2px 6px;
  margin: 0;
  box-shadow: 3px 3px 4px black;
}

/* Note: to include a clickable external link in the block, use
/* `<a href="https://your-site.com">Some text</a>` */
```
