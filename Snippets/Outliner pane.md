# Outliner pane
```css
/* connecting lines outliner */
.outline .collapsible-item-children {
    margin-left: 20px;
    border-left: 1px solid var(--text-muted);
    border-radius: 4px;
    transition:all 0.5s ease-in-out;
}

.outline .collapsible-item-children:hover {
    border-left-color: var(--text-normal);
}

/* change font color outline */
div.collapsible-item-inner {
  color: var(--base3);
}

/* indent wrapped titles outliner*/
  .outline .collapsible-item-inner {
    margin-left: 10px;
    text-indent: -10px;
}

/* List styling (numbering) for outline pane */

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline {
  counter-reset: h1;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.pane-clickable-item {
  counter-reset: h2;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h3;
}


body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h4;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h5;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h6;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.pane-clickable-item:before {
  counter-increment: h1;
  content: counter(h1) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h2;
  content: counter(h1) "." counter(h2) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h3;
  content: counter(h1) "." counter(h2) "." counter(h3) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h4;
  content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h5;
  content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h6;
  content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". ";
}
```
