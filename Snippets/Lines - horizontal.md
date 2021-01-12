# Lines - horizontal
```css
/* Horizontal gradient line in Preview as per Obsidianite theme */
.markdown-preview-view hr {
  margin-block-start: 4em;
  margin-block-end: 4em;
}

.markdown-preview-view hr,
div:not(.CodeMirror-activeline)>.HyperMD-hr-bg {
  border: none;
  height: 0;
  border-bottom: 1px solid;
  border-image-slice: 1;
  border-width: 1px;
  border-image-source: linear-gradient(to right,
          transparent,
          var(--base3), /* PB changed from var(--text-accent) */
          transparent);
}

div:not(.CodeMirror-activeline)>.HyperMD-hr-bg {
  top: 50%;
}

.markdown-preview-view hr::after,
div:not(.CodeMirror-activeline)>.HyperMD-hr-bg::after {
  content: '§';
  display: inline-block;
  position: absolute;
  left: 50%;
  transform: translate(-50%, -50%) rotate(60deg);
  transform-origin: 50% 50%;
  padding: 0.5rem;
  color: var(--base3); /* PB changed from var(--text-sub-accent) */
  background-color: var(--base1);
}

/* Setting the gap above and below a hor. line, incl. footnotes ……
/* …… but footnotes can be set separately - see section Footnotes */
div.markdown-preview-section hr {
  margin-block-start: 30px;
  margin-block-end: 40px;
}
```
