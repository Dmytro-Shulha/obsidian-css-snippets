/* Accent underline when fold is collapsed */
.cm-line:has(.is-collapsed) {
  text-decoration: underline;
  text-decoration-thickness: 0.2em;
  text-decoration-color: var(--text-accent);
}

/* Accent arrow when fold is collapsed */
.cm-fold-indicator .is-collapsed svg {
  stroke: var(--text-accent);
  stroke-width: 3;
}
