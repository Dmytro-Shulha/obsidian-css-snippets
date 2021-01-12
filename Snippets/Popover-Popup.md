# Popover-Popup
```css
/*============bigger link popup preview  ================*/
.popover.hover-popover {
    position: absolute;
    z-index: var(--layer-popover);
    transform: scale(0.9); /* makes the content smaller */
    max-height: 800px;    /* was 300 */
    min-height: 100px;
    width: 500px; /* was 400 */
    overflow: hidden;      
    padding: 0;
    border-bottom: none;
  }
/* I'm not sure what this does, got popove code from Obsdn-Dark-Rmx */
/*
  .popover {
    background-color: var(--background-primary);
    border: 1px solid var(--background-primary-alt);
    box-shadow: 3px 3px 7px var(--background-modifier-box-shadow);
    border-radius: 6px;
    padding: 15px 20px 10px 20px;
    position: relative;
}

/* remove-tweak the bottom gradient on the popup: remove the gradient or set height to 0 */
    .popover.hover-popover:after {
      height: 0px;    
      background: linear-gradient(to bottom, transparent, var(--background-primary) 80%, var(--background-primary));
  }

/* Colour for pop-up text in ⌘+O */
.suggestion-item.is-selected {
  background-color: blue; /* PB changed from var(--text-accent) */
  color: whitesmoke;
}
```
