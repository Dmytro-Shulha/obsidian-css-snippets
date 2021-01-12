# Links
## Change color
```css
/* internal links */
/* change colour in Preview */
a.internal-link {
  color: var(--base2);
}
  
/* change colour in Edit */
.cm-s-obsidian span.cm-hmd-internal-link {
  color: var(--base2);
}
  
/* external links - URLs */
/* change colour in Preview */
a.external-link {
  color: var(--base3);
  font-weight: 500;
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
