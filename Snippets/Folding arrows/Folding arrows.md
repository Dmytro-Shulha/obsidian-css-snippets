# Folding arrows

![demo](demo.png)

```css
/* Bigger folding arrows in edit mode, clearer affordance on hover */
:root {
  --foldgutter-width: 1.8rem;
}

.CodeMirror-foldgutter {
  width: var(--foldgutter-width);
}

.CodeMirror-guttermarker-subtle {
  font-size: 0.8em;
  text-align: center;
  opacity: 0.5;
  line-height: var(--foldgutter-width);
  height: var(--foldgutter-width);
  border-radius: 3px;
}

.CodeMirror-guttermarker-subtle:hover {
  opacity: 1;
  background-color: var(--background-secondary-alt); 
}

.CodeMirror-foldgutter-open::after {
  content: "\25BC";
}

.CodeMirror-foldgutter-folded::after {
  content: "\25BA";
}
```