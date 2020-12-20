# Check box
```css
/* checkbox alignment */
.markdown-preview-view .task-list-item-checkbox {	
	width: 15px;
	height: 15px;
	top: 0px	
}

/* Apple style checkbox */
input[type=checkbox] {
    vertical-align: middle;
    -webkit-appearance: none;
    appearance: none;
    border-radius: 50%;
    border: 1px solid var(--text-faint);
    padding: 0;
}

input[type=checkbox]:focus{
  outline:0;
}

input[type=checkbox]:checked {
    background-color: var(--text-accent-hover);
    border: 1px solid var(--text-accent-hover);
    background-position: center;
    background-size: 70%;
    background-repeat: no-repeat;
    background-image: url('data:image/svg+xml; utf8, <svg width="12px" height="10px" viewBox="0 0 12 8" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(-4.000000, -6.000000)" fill="%23ffffff"><path d="M8.1043257,14.0367999 L4.52468714,10.5420499 C4.32525014,10.3497722 4.32525014,10.0368095 4.52468714,9.8424863 L5.24777413,9.1439454 C5.44721114,8.95166768 5.77142411,8.95166768 5.97086112,9.1439454 L8.46638057,11.5903727 L14.0291389,6.1442083 C14.2285759,5.95193057 14.5527889,5.95193057 14.7522259,6.1442083 L15.4753129,6.84377194 C15.6747499,7.03604967 15.6747499,7.35003511 15.4753129,7.54129009 L8.82741268,14.0367999 C8.62797568,14.2290777 8.3037627,14.2290777 8.1043257,14.0367999"></path></g></g></svg>');
.markdown-preview-view .task-list-item-checkbox { margin-left:-25px; }
.markdown-preview-view .task-list-item { padding-inline-start:25px; }

/* Checkbox as per Molecule theme */
.markdown-preview-view .task-list-item-checkbox {
  -webkit-appearance: none;
  box-sizing: border-box;
  border: 1px solid var(--text-muted);
  border-radius: 2px;
  position: relative;
  width: 1.3em;
  height: 1.3em;
  margin: 12px;
  filter: none;
  outline: none;
  margin-right: 4px;
  margin-bottom: 1px;
  cursor: pointer;
  vertical-align: center;
}

.markdown-preview-view .task-list-item-checkbox:checked {
  border: none;
  background-color: var(--base2);
}

.markdown-preview-view .task-list-item-checkbox:checked::before {
  content: ' ';
  position: absolute;
  background-color: white;
  left: 2px;
  top: 2px;
  right: 2px;
  bottom: 2px;
  -webkit-mask-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' viewBox=\'0 0 14 14\'%3E%3Cpolygon points=\'5.5 11.9993304 14 3.49933039 12.5 2 5.5 8.99933039 1.5 4.9968652 0 6.49933039\'%3E%3C/polygon%3E%3C/svg%3E');
}
  
/* Remove strikethrough from completed to-do lists/checkbox */  
.markdown-preview-view ul > li.task-list-item.is-checked {
    text-decoration: none;
    color: inherit;
}
```

```css
/* CHECKBOX: Green / Red color */

.markdown-preview-view .task-list-item-checkbox{
    -webkit-appearance: none;
  box-sizing: border-box;
  border: 1px solid var(--text-muted);
  border-radius: 2px;
  position: relative;
  width: 1.3em;
  height: 1.3em;
  margin: 0;
  outline: none;
  margin-right: 4px;
  margin-bottom: 2px;
  cursor: pointer;
  vertical-align: baseline;

  background-color: #d068688f;
}

.markdown-preview-view .task-list-item-checkbox:checked {
  background-color: #68d0688f;
}
```