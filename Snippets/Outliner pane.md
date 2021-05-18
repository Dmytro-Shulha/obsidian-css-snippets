# Outliner pane
```css
/* connecting lines outliner */
.outline {
  font-size: 0.8rem;
  font-weight: 200;
}

.outline .tree-item {
  line-height: 1.3;
}

.outline .tree-item-self {
  padding-top: 0.2rem;
  padding-bottom: 0.1rem;
  padding-left: 0.5rem;
  padding-right: 0.3rem;
}  

.outline .tree-item-collapse {
  left: 0.1rem;
}  

.outline .tree-item-inner{
  position:relative;
  padding-top: 0.2rem;
  /* padding-left: 1rem; */
  padding-left: 1.7em;
  text-indent: -0.8em;
  margin-left: 0.2rem;
  /* font-size: 0.9em; */
}  

.outline .tree-item-children {
  margin-left: 0.7rem;
  padding-left: 0.5rem;
  margin-top: -0.3rem;
  padding-top: 0.3rem;
  border-left: 1px solid var(--sidebar-marks, var(--background-modifier-border));
  border-radius: 4px;
  transition:all 0.5s ease-in-out;
}

.outline .tree-item-children:hover {
  border-left-color: var(--sidebar-marks-hover, var(--background-secondary));
}

.outline .collapse-icon + .tree-item-inner {
  font-weight: 400;
  padding-left: 0.2rem;
  /* margin-left: 0rem; */
  /* font-size: 1em; */
}

.outline .collapse-icon {
  margin-top: 0.2rem;
  margin-left: -0.4rem;
  margin-right: -0.4rem;
  width: 2rem;
}
```

/* indent wrapped titles outliner*/
/* included above */

```css
/* change font color outline */
div.collapsible-item-inner {
  color: var(--base3);
}
```

```css
/* Heading counter for outline pane */
.outline {
  counter-reset: rootLayout;
}
.outline .tree-item .tree-item-self .tree-item-inner::before {
  content: counters(rootLayout, ".") ". ";
  counter-increment: rootLayout;
}
.tree-item-children {
  counter-reset: internalLayout;
}
.tree-item-children .tree-item .tree-item-self .tree-item-inner::before {
  content: counters(rootLayout, ".") "." counters(internalLayout, ".") ". ";
  counter-increment: internalLayout;
}

/* nested list counting (ex: 1.1, 1.2) */
/* https://github.com/hipstersmoothie/obsidian-plugin-toc#detailed-nested-ordered-lists */
ol {
  counter-reset: item;
}

ol li {
  display: block;
}

ol li:before {
  content: counters(item, ".") ". ";
  counter-increment: item;
  padding-right: 5px;
}
```

TO AUTOMATICALLY CONVERT H1 HEADINGS TO CAPITAL LETTERS,
GO TO THE `HEADERS.md` FILE AND SCROLL DOWN FAIRLY FAR.
