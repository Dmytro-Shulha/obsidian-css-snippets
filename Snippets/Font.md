# Font
```css
/* Font for the markdown source panel */
div.markdown-source-view {
    font-family: var(--font-family-editor);
    font-size: 0.9em;
}

/* Font for the markdown preview panel */
div.markdown-preview-view {
    font-family: var(--font-family-preview);
    font-size: 0.9em;
}

/* Editor font: make thicker */
.cm-s-obsidian .CodeMirror-line * {
    -webkit-font-smoothing: auto;
}

.cm-s-obsidian .cm-header {
    -webkit-font-smoothing: antialiased;
}

/* Coloring fonts - from Lithou on forum */
/* of italics in Edit mode all notes in a vault */
.cm-em {
    color: red;
}

/* of italics in Preview  all notes in a vault */
em {
    color: red;
}

/* Note 1: the color can be different in Edit and Preview
/* Note 2: for bold use `cm-strong` and `strong` respectively

/* Color of italics in 1 note only */
div.test em {
    color: red;
}

/* And in the note itself add to the top:
`---`
cssclass: test
`---`
```
```

```css
/* Set color of bold text */
.cm-s-obsidian .cm-strong, strong {
  color: var(--bright-red);
}
  
/* Set color of italic text */
.cm-em, em {
  color: goldenrod;
}
```
