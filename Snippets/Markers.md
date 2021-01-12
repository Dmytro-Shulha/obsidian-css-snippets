# Markers
```css
/* Mark a line break, trailing space, tab when in Edit mode */
.cm-trailing-space-new-line, .cm-trailing-space-a, .cm-trailing-space-b, .cm-tab{
    font-size: 0;
}
.cm-trailing-space-a::before, .cm-trailing-space-b::before, .cm-trailing-space-new-line::before, .cm-tab::before{
    content:'·';
    color:var(--text-faint);
    font-size: initial;
}
.cm-trailing-space-new-line::before {
    content:'↵';  
}
.cm-tab::before {
    content:'⟶'
}
```
