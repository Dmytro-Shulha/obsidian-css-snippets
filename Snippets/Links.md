# Links
## Change color
```css
/* Internal links */
/* change colour in Preview */
a.internal-link {
  color: var(--base2);
}
  
/* change colour in Edit */
.cm-s-obsidian span.cm-hmd-internal-link {
  color: var(--base2);
}
  
/* External links - URLs */
/* change colour in Preview */
a.external-link {
  color: var(--base3);
  font-weight: 500;
}

/* change colour in Edit */
.cm-s-obsidian span.cm-link,
.cm-s-obsidian span.cm-url { /* PB added */
  color: #c6ceda; /* ITS theme */
}

/* change color intensity of unresolved links */
.markdown-preview-view .internal-link.is-unresolved {
  opacity: 0.8;
}

## Hide little square with arrow shown next to external link in Preview */
.external-link {
  background-image: none;
/* This removes the space left over after the arrow is gone **/
  padding: 0;
}
```
