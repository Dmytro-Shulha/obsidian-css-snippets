# Lists - (un)ordered

```css
/* Reduce indentation in bullet lists */
ol {
    padding-inline-start: 18px;
}
ul {
    padding-inline-start: 18px;
    list-style-type: disc;
}

/* Long bullet list: connect the same levels of bullets with vertical "lines" */
.cm-hmd-list-indent .cm-tab, ul ul { position: relative; }
.cm-hmd-list-indent .cm-tab::before, ul ul::before {
 content:'';
 border-left: 1px solid rgba(0, 122, 255, 0.25);
 position: absolute;
}

.cm-hmd-list-indent .cm-tab::before { left: 0; top: -5px; bottom: -4px; 
}

ul ul::before { left: -11px; top: 0; bottom: 0; /* change "left:" value for align of vert. line */
}

/* Edit mode unordered list dash rendered as dot for WYSIWYG */
/* I prefer "Turn -lists into bullets as you type as per Typora */
/* Unordered lists: turn into bullets as you type, as per Typora */
```css
span.cm-formatting-list-ul {
  visibility: hidden !important;
}
  
span.cm-formatting-list-ul:after {
  content: '• '; /* ITS theme; for Blue Topaz  */
  margin-left: -12px;
  color: var(--accent); /* ITS theme; for Blue Topaz --text-normal */
  visibility: visible !important;
}
```

## Stylized lists
```css
/*From Gabroel - Obsidian #css-themes channel*/
* {margin: 0; padding: 0; list-style: none;}
ul li:not(.task-list-item) {
  margin-left: 15px;
  position: relative;
  padding-left: 5px;
  list-style-position: inside;
  border-left: 5px solid yellow;
  box-shadow: 0 0 0 0.5px hotpink;
  border-radius: 10px;
}

ol {
  counter-reset: cupcake;
  padding-left: 5px;
}
ol li {
  counter-increment: cupcake;
  margin-left: 15px;
  position: relative;
  padding-left: 5px;
  list-style-position: inside;
  border-left: 5px solid hotpink;
  box-shadow: 0 0 0 0.5px hotpink;
  border-radius: 10px;
}

ol li:before {
  content: counters(cupcake, '.') '  ';
  /* Whatever custom styles you want here */
  color: hotpink;
  font-weight: bold;
  display: inline-block;
  white-space: pre;
}

/*Collapse indicator*/
.markdown-preview-view .collapse-indicator {
  margin-left: -46px;
  padding: 0 18px;
}

/*heading collapse indicator*/
.markdown-preview-view .heading-collapse-indicator {
  margin-left: -25px;
  padding: 0 8px;
}

div.heading-collapse-indicator.collapse-indicator.collapse-icon:hover{
  color: var(--text-accent);
}
.markdown-preview-section:not(.is-collapsed) svg.right-triangle{
  color: var(--text-accent);
}

/*outline collapse indicator*/
div.collapsible-item-collapse.collapse-icon{
  color: var(--text-accent);
}
```

## Stylized lists - auto-adjust width & auto-counter
```css
/*From Gabroel - Obsidian #css-themes channel*/
/*video demo https://discord.com/channels/686053708261228577/702656734631821413/784922140465692712 */

* {margin: 0; padding: 0; list-style: none;}

li > p:not(.task-list-item) {
  display: inline;
  margin-top: 0;
  margin-bottom: 0;
}

ul li:not(.task-list-item) {
  margin-left: 15px;
  border-left: 5px solid gray;
  box-shadow: 0 0 0 0.5px gray;
  border-radius: 10px;
  width: fit-content;
  margin-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  position: relative;
  list-style: none;
  display: list-item;
  height: fit-content;
}

ul li:not(.task-list-item)::before {
  content: '•';
  color: #8ec07c;
  display: inline-block;
  width: 1em;
  position: relative;
  margin-left: 0em;
  font-weight: bold;
  text-shadow: 0 0 0.5em #8ec07c;
}

ol {
  counter-reset: cupcake;
  padding-left: 5px;
}
ol li {
  counter-increment: cupcake;
  margin-left: 15px;
  position: relative;
  padding-left: 5px;
  list-style-position: inside;
  border-left: 5px solid gray;
  box-shadow: 0 0 0 0.5px darkgray;
  border-radius: 10px;
  width: fit-content;
  margin-bottom: 8px;
  padding-right: 5px;
}

ol li::before {
  content: counters(cupcake, '.') '. ';
  /* Whatever custom styles you want here */
  color: gray;
  font-weight: bold;
  display: inline-block;
  white-space: pre;
}


/*Collapse indicator*/
.markdown-preview-view .collapse-indicator {
  margin-left: -46px;
  padding: 0 18px;
}

/*heading collapse indicator*/
.markdown-preview-view .heading-collapse-indicator {
  margin-left: -25px;
  padding: 0 8px;
}

div.heading-collapse-indicator.collapse-indicator.collapse-icon:hover{
  color: var(--text-accent);
}
.markdown-preview-section:not(.is-collapsed) svg.right-triangle{
  color: var(--text-accent);
}
```
