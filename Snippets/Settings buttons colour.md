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

/* dropdown box arrow color
/* NOTE: in the long line of code below, the color is designated by 23ffffff. ffffff = white.
/* You can change it to any color using a hex code */
.dropdown {
  background-image: url(data:image/svg+xml;charset=US-ASCII,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%22292.4%22%20height%3D%22292.4%22%3E%3Cpath%20fill%3D%22%23ffffff%22%20d%3D%22M287%2069.4a17.6%2017.6%200%200%200-13-5.4H18.4c-5%200-9.3%201.8-12.9%205.4A17.6%2017.6%200%200%200%200%2082.2c0%205%201.8%209.3%205.4%2012.9l128%20127.9c3.6%203.6%207.8%205.4%2012.8%205.4s9.2-1.8%2012.8-5.4L287%2095c3.5-3.5%205.4-7.8%205.4-12.8%200-5-1.9-9.2-5.5-12.8z%22%2F%3E%3C%2Fsvg%3E);
}
```
