# Tag pills
```css
/* Tag pills in edit mode - thanks to Whyl */
/* to make rectangular tag pills w/ rounded corners change radii to 4 px */


.CodeMirror-line span.cm-hashtag{
  background-color: var(--text-accent);
  color: white;
  display: inline-block;
  text-decoration: none !important;
}


.CodeMirror-line span.cm-hashtag-begin {
  border-top-left-radius:15px; /* change to 4px for rectangular pills */
  border-bottom-left-radius:15px; /* change to 4px for rectangular pills */
  padding-left:8px;
  border-right:none;
}

.CodeMirror-line span.cm-hashtag-end {
  border-top-right-radius:15px; /* change to 4px for rectangular pills */
  border-bottom-right-radius:15px; /* change to 4px for rectangular pills */
  padding-right:8px;
  border-left:none;
}

/* Tag pills in Preview mode */
.tag:not(.token) {
  border: none;
  color: white !important;
  font-size: 12px;
  padding: 1px 8px 3px;
  text-align: center;
  text-decoration: none;
  margin: 0px 0px;
  cursor: pointer;
  border-radius: 15px; /* change to 4px for rectangular pills */
  background-color: var(--text-accent) !important;
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
  border-radius: 14px; /* change to 4px for rectangular pills */
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
  border-radius: 14px; /* change to 4px for rectangular pills */
}

/* Change color of tag count pill when hovering */
.tag-pane-tag:hover .tag-pane-tag-count {
  color: white;
  background-color: var(--base2);
}
```
