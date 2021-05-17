# Sidebar
```css
/* BOTH SIDEBARS */
/* Collapsible ribbon */
.side-dock-ribbon { flex: 0; }
.workspace-ribbon { width: 0; }
```

OR

```css
.side-dock-ribbon {
    flex: 0 0 0;
}
```

```css
/* Vert. resize handle to change pane width: change color */
.workspace-leaf-resize-handle:hover {
  background-color: var(--base2);
}
```

```css
/* LEFT SIDEBAR */
/* clean up side bar empty state (e.g. unlinked mentions) */
.search-empty-state {
    width: auto;
    padding-left: 15px;
    padding-right: 15px;
    line-height: normal;
}

/* Connectining lines for files and folders in File Explorer*/
.nav-folder-children .nav-folder-children {
  margin-left: 20px;
  padding-left: 0;
  border-left: 1px solid rgba(118,158,165,0.7);
  border-radius: 4px;
  transition:all 0.5s ease-in-out;
}
.nav-folder-children .nav-folder-children:hover {
  border-left-color: rgba(118,158,165,0.7);
}

/* RIGHT SIDEBAR */
/* outliner for the outline */
.outline .collapsible-item-children {
    margin-left: 20px;
    border-left: 1px solid var(--text-muted);
    border-radius: 4px;
    transition:all 0.5s ease-in-out;
  }
.outline .collapsible-item-children:hover {
    border-left-color: var(--text-normal);
}
```
