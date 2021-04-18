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

/* Change color of note spine (Andy mode) */
/* this is for Light theme; for Dark theme change words "theme-light" to "theme-dark" in the rule */
body.theme-light.plugin-sliding-panes .view-header {
    background-color: #f2f8fd;
}
```

```css
/* Wrap long title in the title bar of a note
courtsey of SIRvb https://discord.com/channels/686053708261228577/702656734631821413/829852938763370546 */
.view-header-title {
    margin-top: 5px;
    margin-bottom: 5px;
    white-space: pre-wrap;
    line-height: 25px;
}
.view-header {
    height: auto;
}
```
