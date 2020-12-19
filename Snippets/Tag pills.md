# Tag pills
```css
/* Tag pills in edit mode */
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-hashtag-end:before {
    content: '#';
}
.tag, div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-hashtag-end {
  background-color: var(--text-accent);
  border: none;
  color: white !important;
  font-size: 13px;
  padding: 1px 8px;
  text-align: center;
  text-decoration: none !important;
  display: inline-block;
  margin: 1px 1px;
  cursor: pointer;
  border-radius: 14px;
}
.tag:hover {
color: white;
background-color: var(--text-accent-hover);
}
.tag[href^="#obsidian"] {
  background-color: #4d3ca6;
}

/* Tag pills in tag pane */
.tag-pane-tag-count {
  background-color: var(--text-accent);
  border: none;
  color: white;
  font-size: 11px;
  padding: 1px 8px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 0px 0px;
  cursor: pointer;
  border-radius: 14px;
}

.tag-pane-tag-text {
  background-color: var(--text-accent);
  border: none;
  color: white;
  font-size: 11px;
  padding: 1px 8px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 0px 0px;
  cursor: pointer;
  border-radius: 14px;
}

/* Change color of tag count pill when hovering */
.tag-pane-tag:hover .tag-pane-tag-count {
  color: white;
  background-color: var(--base2);
}
```
