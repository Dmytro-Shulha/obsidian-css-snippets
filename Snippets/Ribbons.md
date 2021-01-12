# Ribbons
```css
/* Ribbons */ 
/* collapse buttons: change color */
.workspace-ribbon-collapse-btn {
  color: var(--base2);
}

/* on left change background color */
.workspace-ribbon.mod-left {
  border-color: transparent;
  width: 35px;
  background: var(--base3);
}

/* on left icons: change color */
.side-dock-ribbon-tab, .side-dock-ribbon-action {
  color: var(--base2);
  text-align: center;
  font-size: 18px;
  opacity: 0.9;
}

.side-dock-ribbon-tab, .side-dock-ribbon-action:hover {
  color: var(--base5);
  text-align: center;
}

/* on right change background color */
.workspace-ribbon.mod-right {
  border-color: transparent;
  width: 30px;
  background: var(--base3);
}

/* hide Preview/Edit icon, only show on hover */
.view-action[aria-label*="Preview"], .view-action[aria-label*="Edit"] {
  opacity: 0;
}

.view-action:hover {
  opacity: 1;
}
```
