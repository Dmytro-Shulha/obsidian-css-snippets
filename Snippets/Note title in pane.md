# Note title in pane
```css
/* Change the colour or the font-weight of the note title in a pane */
.view-header-title {
    /*color: red; */
    font-weight: 300; /** this range from 1 - 1000 **/
}

/* Change color of note title active pane - Obsidianite */
.workspace-leaf.mod-active .view-header-title {
  color: var(--base2);
}

/* Change icon above  vert. note title on title spine - from Obsidianite */
.view-header-icon {
    color: rgb(31, 178, 129); /* PB changed from var(--text-accent) */
}

/* Change color of line next to note title in Andy Mode - Obsidianite */
.workspace-leaf.mod-active .view-header {
  border-right: 2px solid var(--base2) !important; /* change to border-bottom in non-AM */
}
```
