# Links
## Change color
```css
/* Internal links */
/* change colour in Preview */
a.internal-link {
  color: var(--base2);
}
```
  
## Change colour in Edit
```css
.cm-s-obsidian span.cm-link,
.cm-s-obsidian span.cm-url { /* PB added */
  color: #c6ceda;
}
```

## Change colour in Edit
```css
.cm-s-obsidian span.cm-hmd-internal-link {
  color: var(--base2);
}
  
/* External links - URLs */
/* change colour in Preview */
a.external-link {
  color: var(--base3);
  font-weight: 500;
}
```


## Change color intensity of unresolved links
```css
.markdown-preview-view .internal-link.is-unresolved {
  opacity: 0.8;
}
```

## Hide little square with arrow shown next to external link in Preview
```css
.external-link {
  background-image: none;
/* This removes the space left over after the arrow is gone **/
  padding: 0;
}
```

## External link hover - view URL
```css
/* view URL in popup - courtesy of narand */
a.external-link {
  position: relative;
}

a.external-link:before {
  position: absolute;
  padding: 0px 8px 0px 8px;
  color: var(--text-normal);
  background-color: var(--background-primary-alt);
  border-radius: 3px;
  font-size: 80%;
  display: none;
  z-index: 1000;
  top: 1.8em;
  content: attr(href)
}

a.external-link:hover:before {
  display: inline; 
}

OR

/* view URL in bottom of screen - courtesy Moonbase59 */
a.external-link {
  position: relative;
}

a.external-link:before {
  position: fixed;
  left: 0;
  bottom: 0;
  padding: 0 0.5em;
  color: var(--text-normal);
  background-color: var(--background-primary-alt);
  border: 1px solid var(--background-modifier-border);
  border-radius: 0 0.4em 0 0;
  font-family: var(--default-font);
  font-size: initial;
  font-style: initial;
  font-weight: initial;
  text-decoration: initial;
  display: none;
  z-index: 1000;
  content: attr(href);
}

a.external-link:hover:before {
  display: block;
  max-width: 98%;
  overflow: hidden;
  text-overflow: ellipsis;
}
```
