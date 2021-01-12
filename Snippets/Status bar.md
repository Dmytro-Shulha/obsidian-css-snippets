# Status bar
```css
/* Remove status bar */
.status-bar {display: none;}

/* Fading Status Bar and Note Controls (from MAGMA theme) */
.status-bar:hover .status-bar-item {
    opacity: 1;
    transition: opacity .1s ease-in-out;
}
.status-bar:not(:hover) .status-bar-item {
    opacity: 0.25;
    transition: opacity .25s ease-in-out;
}
.view-header:hover .view-actions {
    opacity: 1;
    transition: opacity .1s ease-in-out;
}
.view-header:not(:hover) .view-actions {
    opacity: 0.25;
    transition: opacity .25s ease-in-out;
}

/*  Flat status bar  */
.status-bar {
    background-color: var(--background-secondary-alt);
    border-top: 0px solid var(--background-modifier-border);
    color: var(--text-accent);
    font-family: "Roboto";
}
```
