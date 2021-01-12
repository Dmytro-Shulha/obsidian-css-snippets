# Tag pills
```css
/* Tag pills in edit mode - thanks to Whyl */
.CodeMirror-line span.cm-hashtag-begin {
  background-color: var(--text-accent);
  color: white;
  border-top-left-radius:15px;
  border-bottom-left-radius:15px;
  padding-left:8px;
  border-right:none;
  display: inline-block;
  text-decoration: none !important;
}

.CodeMirror-line span.cm-hashtag-end {
  background-color: var(--text-accent);
  color: white;
  border-top-right-radius:15px;
  border-bottom-right-radius:15px;
  padding-right:8px;
  border-left:none;
  display: inline-block;
  text-decoration: none !important;
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
