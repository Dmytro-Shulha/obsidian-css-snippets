# WYSIWYG
```css
/**************************************/
/* 5. WYSIWYG: imitation in Edit mode */
/**************************************/
/* Source: various people on forum, incl. Piotr and pihentagy
/**************************************/
/* Editor font: make thicker so it is like in Preview
/* Remove markdown clutter
/* Unordered lists: turn into bullets as you type, as per Typora
/* Underline H1 heading in Edit mode
/* Blockquote in edit mode with left border rendered instead of ">"
/* Tag pills in edit mode
/* Coloured headings for editor and preview, same font-weight in Edit & Preview
/* ============================================================================*/

/* For Edit mode use same font and font size as for Preview mode */

/* Editor font: make thicker so it is like in Preview */
.cm-s-obsidian .CodeMirror-line * {
    -webkit-font-smoothing: auto;
}
  
/* Remove markdown clutter */
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting,
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-string.cm-url,
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting-link,
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting-link:not(.cm-link),
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-comment,
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-hmd-barelink,
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-tag {
    display: none !important;
} 
  
/* except numbered list */
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting-list {
   display: inline !important;
}
  
/* except list markers */ span.cm-formatting-list,
/*code block backticks */ span.cm-formatting-code-block.cm-hmd-codeblock,
/* optionally header hashes */ /*span.cm-formatting-header
{ display: inline !important; }
  
/* and task checkboxes */
span.cm-formatting-task { display: inline !important; font-family: monospace; }
  
/* highlight (==) not visible anymore if not active line */
div:not(.CodeMirror-activeline) > .CodeMirror-line .cm-formatting-highlight.cm-highlight {
 font-size: 0;
}
  
/* Unordered lists: turn into bullets as you type, as per Typora */
span.cm-formatting-list-ul {
  visibility: hidden !important;
}
    
span.cm-formatting-list-ul:after {
  content: '• ';
  margin-left: -12px;
  color: var(--text-normal);
  visibility: visible !important;
}
  
/* Underline H1 heading in Edit mode */
.cm-s-obsidian pre.HyperMD-header-1:after {
  content: "";
  position: absolute;
  bottom: 5px;
  left: 5px;
  width: calc(100% - 10px);
  height: 1px;
  background: var(--text-accent); /* rgb(123, 108, 214); */
}
  
/* Blockquote: in edit mode with left border rendered instead of > */
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting.cm-formatting-quote,
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-hmd-indent-in-quote {
  display: inline !important;
  color: transparent !important;
}

div:not(.CodeMirror-activeline)>.HyperMD-quote {
   background-color:rgb(238, 234, 234);
   border-left: 3px solid var(--text-selection);
   border-color: red !important; 
   border-radius: 0 8px 8px 0;
   font-size: 17px;
   line-height: 1.5em;
   margin-left: 5px;
   padding: 12px 10px 15px 8.5px;
   display: inline-block;
}
 
/* Tag pills in edit mode */
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-hashtag-end:before {
   content: '';
}
.tag, div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-hashtag-end {
  background-color: rgba(123, 108, 214); /* wasvar(--text-accent); */
  border: none;
  color: white !important;
  font-size: 14px;
  padding: 0px 8px;
  padding-top: -2px;
  padding-bottom: 3px;
  text-align: center;
  text-decoration: none !important;
  display: inline-block;
  margin: 1px 1px;
  cursor: pointer;
  border-radius: 14px;
}

.tag:hover {
  color: white;
  background-color: var(--text-accent-hover);
}
  
/* Coloured headings for editor and preview, same font-weight in Edit & Preview */
.cm-s-obsidian .cm-header-1,
.markdown-preview-view h1 {
  font-weight: 450;
  color: rgb(123, 108, 214); /* was(115, 98, 205); */
}
  
.cm-s-obsidian .cm-header-2,
.markdown-preview-view h2 {
  font-weight: 450;
  color: rgb(123, 108, 214);
}
  
.cm-s-obsidian .cm-header-3,
.markdown-preview-view h3 {
  font-weight: 450;
  color: rgb(123, 108, 214);
}
  
.cm-s-obsidian .cm-header-4,
.markdown-preview-view h4 {
  font-weight: 450;
  color: rgb(123, 108, 214);
}
  
.cm-s-obsidian .cm-header-5,
.markdown-preview-view h5 {
  font-weight: 450;
  color: rgb(123, 108, 214);
}
  
.cm-s-obsidian .cm-header-6,
.markdown-preview-view h6 {
  font-weight: 450;
  color: rgb(123, 108, 214);
}
```

```css
/* Show line numbers only on hover */
.theme-dark
.cm-s-obsidian .CodeMirror-linenumber {
  opacity : 0;
}

.cm-s-obsidian .CodeMirror-linenumber:hover {
  opacity: 1;
}
```
