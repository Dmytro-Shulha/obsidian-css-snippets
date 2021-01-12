# Yaml
```css
/* remove the yaml metadata from embed */

/* Remove embed yaml first separator */
.markdown-embed-content > hr:first-child {
  display: none;
}

/* Remove embed yaml content */
.markdown-embed-content > hr:first-child + p {
  display: none;
}

/* Remove embed yaml second separator (if empty) */
.markdown-embed-content > hr:first-child + hr {
  display: none;
}

/* Remove embed yaml second separator */
.markdown-embed-content > hr:first-child + p + hr {
  display: none;
}
```
