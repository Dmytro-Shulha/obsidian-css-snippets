# Links
```css
/* change colour of URL link in Preview */
a.external-link {
  color: red;
}

/* change colour of URL [text] part in Edit */
span.cm-link {
  color: rgb(136,136,136) !important; /* leave !important */
}

/* Change internal link colour in Preview */
a.internal-link {
  color: red;
}

/* Change internal link colour in Edit */
.cm-s-obsidian span.cm-hmd-internal-link {
  color: firebrick;
}

/* Change colour of unresolved links */
.markdown-preview-view .internal-link.is-unresolved {
  color: #00FFFF !important;
  opacity: 0.8;
}

/* Hide little square with arrow shown next to external link in Preview */
.external-link {
  /* This remove the arrow */
  background-image: none;
  /* This removes the space left over after the arrow is gone */
  padding: 0;
}
```
