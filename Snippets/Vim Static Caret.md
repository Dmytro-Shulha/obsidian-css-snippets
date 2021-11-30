# Vim Static Caret

Changes the Vim caret from a blinking one to a static one in the editor to reflect a more realistic Vim experience.

```css
.cm-fat-cursor .CodeMirror-cursor {
  visibility: visible !important;
}

.cm-animate-fat-cursor {
  animation: none;
}

div.CodeMirror-cursors, div.CodeMirror-dragcursors, div.CodeMirror-secondarycursor {
  visibility: visible !important;
}
```
