# Headers
```css
/* List styling (H1 numbering ONLY) for note content */

/* initialize css counter */
body {
    counter-reset: head-num-1;
}

/* put counter result into H1 headings */
.markdown-source-view .cm-formatting-header-1::after , h1::before {
  counter-increment: head-num-1;
  content: counter(head-num-1) ". ";
}

/* Do not render H6 header in Preview */
h6 {
  display: none;
}
```

```
/* Selection the first H1 header of the Note */
pre:nth-of-type(2).HyperMD-header.HyperMD-header-1 {
    color: red;
}
```

```css
/* Change just 1 particular header */
/* Note: gap between 1st and 2nd line must be put in ! */
<div style="color:red"></div>
```
```

```

OR put it in an html element with a class that changes the color

```css
.important {
    color: red;
}

<div class="important"></div>

/* changing the color of the header in edit mode */
.cm-header-1 {
  color:rgb(203, 77, 73);
}

/* Gradient coloured headers in Edit and Preview mode */
.cm-s-obsidian .cm-header-1,
 .markdown-preview-view h1 {
  background: linear-gradient(to right, gold, coral); /* choose any 2 colors you like */
  -webkit-background-clip: text;
  color: transparent;
  width: fit-content;
}

/* Coloured headings for editor and preview in Dracula */
.cm-header-1, .markdown-preview-view h1
{
  font-family: var(--font-family-editor);
  font-weight: 500;
  font-size: var(--font-size-h1);
  color: var(--text-title-h1);
}

.cm-header-2, .markdown-preview-view h2
{
  font-family: var(--font-family-editor);
  font-weight: 500;
  font-size: var(--font-size-h2);
  color: var(--text-title-h2);
}

.cm-header-3, .markdown-preview-view h3
{
  font-family: var(--font-family-editor);
  font-weight: 500;
  font-size: var(--font-size-h3);
  color: var(--text-title-h3);
}

.cm-header-4, .markdown-preview-view h4
{
  font-family: var(--font-family-editor);
  font-weight: 500;
  font-size: var(--font-size-h4);
  color: var(--text-title-h4);
}

.cm-header-5, .markdown-preview-view h5
{
  font-family: var(--font-family-editor);
  font-weight: 500;
  font-size: var(--font-size-h5);
  color: var(--text-title-h5);
}

.cm-header-6, .markdown-preview-view h6
{
  font-family: var(--font-family-editor);
  font-weight: 500;
  font-size: var(--font-size-h6);
  color: var(--text-title-h6);
} */

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

/* Underline H1 heading in Edit mode */
/* .cm-header-1 {
  border-bottom: 1px solid var(--text-accent);
} */

.cm-s-obsidian pre.HyperMD-header-1:after {
  content: "";
  position: absolute;
  bottom: 5px;
  left: 5px;
  width: calc(100% - 10px);
  height: 1px;
  background: var(--text-accent); /* rgb(123, 108, 214); */
}
```

```css

/* Eliminate margin (gap, space) under headings - Preview mode only */
/* H1 underlined too */
.markdown-preview-view h1 {
  padding-bottom: 5px;
  border-bottom: 1px solid var(--base2); /* PB changed from --text-accent */
  margin-bottom: -10px;
}

.markdown-preview-view h2,
.markdown-preview-view h3,
.markdown-preview-view h4,
.markdown-preview-view h5,
.markdown-preview-view h6 {
    margin-bottom: -20px;
    padding-bottom: 5px;
}

/* Changing size/color of the header hashtags # */
.cm-formatting-header {
  color: var(--text-faint);
font-size: 0.6em;
}

/* USED IN CONTEXT OF "REMOVE CLUTTER" */
/* Replace header hashes (#) by H1, H2, etc. in edit mode */ 
/* from Blue Topaz theme: DIRTY WYSIWYM HEADERS by _ph */

/* Header folder icon */
.CodeMirror-foldgutter-open, .CodeMirror-foldgutter-folded {
  padding-left: -10px;
}

.CodeMirror-sizer{
  margin-left: 35px !important;
}

/*-- reduce left padding --*/
.CodeMirror {
  height: 100%;
  direction: ltr;
  padding: 0 5px;
}

/*-- hide # markup--*/
.cm-formatting.cm-formatting-header.cm-formatting-header-1.cm-header.cm-header-1,
.cm-formatting.cm-formatting-header.cm-formatting-header-2.cm-header.cm-header-2,
.cm-formatting.cm-formatting-header.cm-formatting-header-3.cm-header.cm-header-3,
.cm-formatting.cm-formatting-header.cm-formatting-header-4.cm-header.cm-header-4,
.cm-formatting.cm-formatting-header.cm-formatting-header-5.cm-header.cm-header-5,
.cm-formatting.cm-formatting-header.cm-formatting-header-6.cm-header.cm-header-6
{font-size:0px;}

/*-- display H1-h6 in gutter--*/
.cm-formatting.cm-formatting-header.cm-formatting-header-1.cm-header.cm-header-1:before{
  content:"H1";
  font-size:14px;
  color: var(--h1ys);
  left:-36.5px;
  top:11px;
  position:absolute;
}
.cm-formatting.cm-formatting-header.cm-formatting-header-2.cm-header.cm-header-2:before{
  content:"H2";
  font-size:13px;
  color: var(--h2ys);
  left:-36.5px;
  top:9px;
  position:absolute;
}
.cm-formatting.cm-formatting-header.cm-formatting-header-3.cm-header.cm-header-3:before{
  content:"H3";
  font-size:12px;
  color: var(--h3ys);
  left:-36.7px;
  top: 7px;
  position:absolute;
}
.cm-formatting.cm-formatting-header.cm-formatting-header-4.cm-header.cm-header-4:before{
  content:"H4";
  font-size:11px;
  color: var(--h4ys);
  left:-20.5px;
  top: 7px;
  position:absolute;
}
.cm-formatting.cm-formatting-header.cm-formatting-header-5.cm-header.cm-header-5:before{
  content:"H5";
  font-size:10px;
  color: var(--h5ys);
  left:-20px;
  top: 9px;
  position:absolute;
}
.cm-formatting.cm-formatting-header.cm-formatting-header-6.cm-header.cm-header-6:before{
  content:"H6";
  font-size:9px;
  color: var(--h6ys);
  left:-19.5px;
  top: 9px;
  position:absolute;
}

/*-- is active line, hide H[1-6] in gutter --*/
.CodeMirror-activeline span.cm-formatting.cm-formatting-header.cm-formatting-header-1.cm-header.cm-header-1:before,
.CodeMirror-activeline span.cm-formatting.cm-formatting-header.cm-formatting-header-2.cm-header.cm-header-2:before,
.CodeMirror-activeline span.cm-formatting.cm-formatting-header.cm-formatting-header-3.cm-header.cm-header-3:before,
.CodeMirror-activeline span.cm-formatting.cm-formatting-header.cm-formatting-header-4.cm-header.cm-header-4:before,
.CodeMirror-activeline span.cm-formatting.cm-formatting-header.cm-formatting-header-5.cm-header.cm-header-5:before,
.CodeMirror-activeline span.cm-formatting.cm-formatting-header.cm-formatting-header-6.cm-header.cm-header-6:before
{font-size:0px;}

/*-- is active line, display # markup --*/
.CodeMirror-activeline > pre > span .cm-formatting.cm-formatting-header.cm-formatting-header-1.cm-header.cm-header-1{
  font-size:24px;
  display:inline;
}
.CodeMirror-activeline > pre > span .cm-formatting.cm-formatting-header.cm-formatting-header-2.cm-header.cm-header-2{
  font-size:22px;
  display:inline;
}
.CodeMirror-activeline > pre > span .cm-formatting.cm-formatting-header.cm-formatting-header-3.cm-header.cm-header-3{
  font-size:20px;
  display:inline;
}
.CodeMirror-activeline > pre > span .cm-formatting.cm-formatting-header.cm-formatting-header-4.cm-header.cm-header-4{
  font-size:18px;
  display:inline;
}
.CodeMirror-activeline > pre > span .cm-formatting.cm-formatting-header.cm-formatting-header-5.cm-header.cm-header-5{
  font-size:16px;
  display:inline;
}
.CodeMirror-activeline > pre > span .cm-formatting.cm-formatting-header.cm-formatting-header-6.cm-header.cm-header-6{
  font-size:16px;
  display:inline;
}

/* Change header size in Edit mode */
.cm-header-1 {
  font-size: 27px;
}
  
.cm-header-2 {
  font-size: 22px;
}
  
.cm-header-3 {
  font-size: 21px;
}
  
.cm-header-4 {
  font-size: 19px;
}
  
.cm-header-5 {
  font-size: 16px;
}
  
.cm-header-6 {
  font-size: 13px;
}

/* Change header size in Preview mode */
.markdown-preview-view h1 {
  font-size: 27px;
}
  
.markdown-preview-view h2 {
  font-size: 20px;
}
  
.markdown-preview-view h3 {
  font-size: 21px;
}
  
.markdown-preview-view h4 {
  font-size: 19px;
}
  
.markdown-preview-view h5 {
  font-size: 16px;
}
  
.markdown-preview-view h6 {
  font-size: 13px;
  font-weight: bold;
}
```

```css
/* Automatically convert H1 headings to capitals in the Outline pane */
.outline .tree-item-inner {
    text-transform: uppercase;
}

.outline .tree-item-children .tree-item-inner {
    text-transform: none;
}
```

If you need to have H1 headings capitalized in the note text, use:
```css
/* Automatically convert H1 headings to capitals in text */
.cm-header-1, .markdown-preview-view h1 {
    text-transform: uppercase;
}
```

In Live Preview, header hashes are hidden if the line is not active.
Some people prefer to keep them visible to know what level header they are dealing with.
The code below is courtesy of @NothingIsLost on the Discord forum.
```css
.cm-line > span.cm-header-1:not(.cm-formatting):before { content: "# "; }
.cm-line.cm-active > span.cm-header-1 > span:not(.cm-selection):before { content: "# "; }
.cm-line > span.cm-header-1 ~ span.cm-header-1:not(.cm-formatting):before { content: ""; }

.cm-line > span.cm-header-2:not(.cm-formatting):before { content: "## "; }
.cm-line.cm-active > span.cm-header-2 > span:not(.cm-selection):before { content: "## "; }
.cm-line > span.cm-header-2 ~ span.cm-header-2:not(.cm-formatting):before { content: ""; }

.cm-line > span.cm-header-3:not(.cm-formatting):before { content: "### "; }
.cm-line.cm-active > span.cm-header-3 > span:not(.cm-selection):before { content: "### "; }
.cm-line > span.cm-header-3 ~ span.cm-header-3:not(.cm-formatting):before { content: ""; }

.cm-line > span.cm-header-4:not(.cm-formatting):before { content: "#### "; }
.cm-line.cm-active > span.cm-header-4 > span:not(.cm-selection):before { content: "#### "; }
.cm-line > span.cm-header-4 ~ span.cm-header-4:not(.cm-formatting):before { content: ""; }

.cm-line > span.cm-header-5:not(.cm-formatting):before { content: "##### "; }
.cm-line.cm-active > span.cm-header-5 > span:not(.cm-selection):before { content: "##### "; }
.cm-line > span.cm-header-5 ~ span.cm-header-5:not(.cm-formatting):before { content: ""; }

.cm-line > span.cm-header-6:not(.cm-formatting):before { content: "###### "; }
.cm-line.cm-active > span.cm-header-6 > span:not(.cm-selection):before { content: "###### "; }
.cm-line > span.cm-header-6 ~ span.cm-header-6:not(.cm-formatting):before { content: ""; }
```
