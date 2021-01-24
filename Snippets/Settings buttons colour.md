# Settings buttons colour
```css
/* Obsidian settings, change color of: */
/* the enable/disable buttons */
.checkbox-container.is-enabled {
  background-color: var(--base2);
}

/* "Check for updates" button */
button.mod-cta {
  background-color: var(--base2);
}

button.mod-cta:hover {
  background-color: var(--base3);
}

/* "Installed" button in 3rd party plug-ins tab */
span.flair.mod-pop {
  background-color: var(--base2);
}

/* tab "3rd party plugins" font color Browse button */
.setting-item-control button {
  background-color: var(--base2) !important;
  color: var(--base3);
}

.setting-item-control button:hover {
  background-color: var(--base5) !important;
  color: var(--base3);
}

/* change color of buttons in Settings > Appearance > Themes > Browse */
.modal button:not(.mod-cta):not(.mod-warning) {
  background-color: var(--base2);
}

/* In tab "Appearance" set color of "refresh" and "Open themes folder" icons */
.setting-editor-extra-setting-button.clickable-icon {
  color: var(--base2);
}

/* link color in the settings e.g. in description of plug-in */
a {
  color: var(--base3);
}

a:hover {
  color: var(--base3);
}

/* dropdown box color, excl. arrow */
.dropdown {
  background-color: var(--text-accent);
  color: white;
  border: none;
}

.setting-item-control .dropdown:hover {
  background-color: rgb(202, 89, 86);
  color: white;
  border: none;
}
```
