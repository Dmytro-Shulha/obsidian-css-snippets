# Graph nodes
```css
/* to style the new nodes in the 0.9.1+ */
.theme-light .graph-view.color-arrow {
color: #5cc863;
}

.theme-light .graph-view.color-fill-tag {
  color: #440154;
}

.theme-light .graph-view.color-fill-attachment {
  color: #277f8e;
}

.theme-light .graph-view.color-fill-unresolved {
  color: #fde725; 
}
```

Might work as well:
```css
.graph-view.color-fill {
  color: var(--background-secondary);
}
.graph-view.color-circle {
  color: var(--text-normal);
}
.graph-view.color-line {
  color: var(--background-modifier-border);
}
.graph-view.color-text {
  color: var(--text-normal);
}
.graph-view.color-fill-highlight {
  color: var(--interactive-accent);
}
.graph-view.color-line-highlight {
  color: rgb(var(--interactive-accent-rgb));
}
```