# Gutter line numbers
```css
/* Make subtler folding gutter arrows */
.CodeMirror-foldgutter-folded:after, .CodeMirror-foldgutter-open:after {
  opacity: 0.2;
  font-size: 70%;
}

  /*=== From Obsdn-Dark-Rmx: line nos. smaller and less bright ===*/
/*== Section name in O-D-R: codemirror line numbers gutter edit mode ====*/
.cm-s-obsidian .CodeMirror-linenumber {
    color: var(--text-accent);
    opacity : 0.8;
    font-size: 14px;
    font-family: Consolas,monospace;
}
.CodeMirror-gutter-elt {
    position: absolute;
    cursor: default;
    z-index: 4;
}
.CodeMirror-linenumber {
    padding: 0 3px 0 0px;
    min-width: 20px;
    text-align: right;
    white-space: nowrap;
}
```
