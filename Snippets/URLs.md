# URLs
```css
/* Hide URLs in Edit mode - source death_au @ https://forum.obsidian.md/t/hide-or-truncate-urls-in-editor-using-css/359/2*/
div:not(.CodeMirror-activeline) > .CodeMirror-line .cm-string.cm-url:not(.cm-formatting) {
    font-size: 0;
}
div:not(.CodeMirror-activeline) > .CodeMirror-line .cm-string.cm-url:not(.cm-formatting)::after {
    content: '🔗';
    font-size: 1rem;
}
```
