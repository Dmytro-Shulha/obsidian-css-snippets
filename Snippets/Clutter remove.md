# Clutter remove
```css
/* Remove markdown clutter */
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-string.cm-url,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-link
{ display: none; }

/* except list markers */ span.cm-formatting-list,
/*code block backticks */ span.cm-formatting-code-block.cm-hmd-codeblock,
/* optionally header hashes */ span.cm-formatting-header
{ display: inline !important; }

/* and task checkboxes */
span.cm-formatting-task { display: inline !important; font-family: monospace; }

/* highlight == markdown not visible anymore if not active line */
div:not(.CodeMirror-activeline) > .CodeMirror-line .cm-formatting-highlight.cm-highlight {
  font-size: 0;
}
```
