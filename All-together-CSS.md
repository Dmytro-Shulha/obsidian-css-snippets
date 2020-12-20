# Animations
```css
/* ===== snappier animations ==== */
.workspace-tab-header,
.workspace-tab-header-inner,
.workspace-tab-container-before,
.workspace-tab-container-after {
  transition: background-color 100ms linear;
}
```

# Block quote
```css
/* for editor */
.cm-quote {
    color: var(--text-normal) !important;
}

/* for preview */
.markdown-preview-view blockquote {
    background-color: #d3d3d3;
    border: 0px solid;
    border-color: red !important;
    border-left-width: 5px !important;
    border-radius: 0 8px 8px 0;
    font-family: ;
    color: black; 
    font-size: 15px;
    line-height: 1.5em;
    margin: 0 10px;
    padding-top: 2px;
    padding-bottom: 13px;
}

/* Vertical centering of text in blockquote */
blockquote {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

/* As per Obsidianite */
.markdown-preview-view blockquote {
  position: relative;
  padding: 1rem 2rem 1rem 3rem;
  color: white; /* #bdbdbd */
  line-height: 1.4em;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  border-top-left-radius: 3px;
  border-bottom-left-radius: 3px;
  margin-bottom: 2em;
  border-left: 4px rgba(31, 178, 129, 0.9) solid;
  border-top: transparent;
  border-bottom: transparent;
  background: linear-gradient(135deg, var(--base4), var(--base3));
  border-right: transparent;
  display: inline-block;
  margin-right: 0 !important;
}

.markdown-preview-view blockquote::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0px;
  height: 2px;
  width: 60%;
  background: linear-gradient(90deg, rgba(31, 178, 129, 0.9), var(--base3));
}

.markdown-preview-view blockquote::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0px;
  height: 2px;
  width: 25%;
  background: linear-gradient(90deg, rgba(31, 178, 129, 0.9), var(--base3));
}

.markdown-preview-view blockquote p {
  position: relative;
}

.markdown-preview-view blockquote p:first-of-type::before {
  content: '“';
  font: 14px/20px italic Times, serif;
  font-weight: 700;
  font-size: 3em;
  color: var(--base2); /* PB changed from var(--text-accent) */
  position: absolute;
  top: 0.1rem;
  left: -1.8rem;
}
```

## Quotation marks
```css
/* from https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/39 */
/* Add quotation character before quote */
blockquote:before {
  font: 14px/20px italic Times, serif;
  content: "“";
  font-size: 3em;
  line-height: 0.1em;
  vertical-align: -0.4em;
}
blockquote p { display: inline; }
```

## Signature: name of the person quoted
```css
Put this code in the CSS sheet (courtesy Gabroel)
/* signature inside the blockquote*/
.signature {
  font-family: "SignPainter"; /**Choose a cursive font */
  text-align: right;
}

Then, in the note, at the end of the blockquote put this:
`<div class="signature">- Name </div>`

if you want the font size of the signature bigger, use this instead:
`<div class="signature"> <span style="font-size:25px">- Name</span> </div>`
```

OR, without the css code and the div rule, you can simply write at the end of the blockquote:

`<cite> — Name </cite>`

which puts the name in italics, though unstylised, and thus differentiates it from the quote.

# Buttons - stylized
```css
/* Stylized buttons - from Gabroel */
button {
  border: solid 2px #fff;
  font-weight: bold;
  font-family: Product Sans;
  border-radius: 30px;
  font-size: 20px;
  color: #fff;
  box-shadow: inset 2px 2px 0 #fff, 0 8px 10px -4px rgba(0,0,0,0.4);
  cursor: pointer;
  transition: all 0.4s ease;
  margin-bottom: 5px;
  margin-top: 5px;
}
```

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

# Clutter remove
```css
/* Remove markdown clutter */
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-string.cm-url,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-link
{ display: none; }

/* except list markers */ span.cm-formatting-list,
/*code block backticks */ span.cm-formatting-code-block.cm-hmd-codeblock,
/* optionally header hashes */ span.cm-formatting-header
{ display: inline !important; }

/* and task checkboxes */
span.cm-formatting-task { display: inline !important; font-family: monospace; }

/* highlight == markdown not visible anymore if not active line */
div:not(.CodeMirror-activeline) > .CodeMirror-line .cm-formatting-highlight.cm-highlight {
  font-size: 0;
}
```

# Command palette
```css
/* Command palette: change font color of hotkeys */
.suggestion-item.is-selected .suggestion-hotkey{
  color: var(--base3)
}
```


# Country flag hashtag
```css
/* Country flag when using hashtag of ISO language code - original */
/* Source: https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/33?u=klaas */
.tag[href="#eng"]{

  color: black;
  background: #b5fbac;
  text-shadow:  20px 20px 60px #9ad592, 
             -20px -20px 60px #d0ffc6;
}

.tag[href="#eng"]:before {
  color: white;
  content: "🇺🇸";
  padding: -20pt -20pt 15pt 5pt;
  margin: 0pt;
  font-size: 15pt;
}

.tag[href="#eng"]:hover {

border-radius: 14px;
background: #b5fbac;
box-shadow:  20px 20px 60px #9ad592, 
             -20px -20px 60px #d0ffc6;
}

/* Used by PB in Solarized */
.tag[href="#nl"]{
  color: black;
  background: var(--base3);
}

.tag[href="#nl"]:before {
  color: black;
  content: "🇳🇱";
  padding: -20pt -20pt 15pt 5pt;
  margin: 0pt;
  font-size: 15pt;
}

.tag[href="#nl"]:hover {
border-radius: 14px;
background: var(--base3);
}
```

# Edge on left
```css
/* In Edit mode, reduce space between the left edge (blue line) and the line numbering, and instead of toggling to "Readable line length" use max-width - thanks to Reggie*/
/* https://discord.com/channels/686053708261228577/702656734631821413/73219976395672781 */
.cm-s-obsidian {
    max-width: 750px;
    text-align: left;
    padding-left: 0;
}

.markdown-source-view {
    padding-right: 0px;
}

.markdown-preview-view {
    max-width: 750px;
    text-align: left;
}
```

# Embeds
## Transclusions
```css
/* Hide all H1 in transclusions .... */
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section > h1,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section > h2,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section > h3,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section > h4,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section > h5,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section > h6 {
  display:none;
}

/* .... but show H2 and on in transclusions */
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section ~ div.markdown-preview-section > h1,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section ~ div.markdown-preview-section > h2,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section ~ div.markdown-preview-section > h3,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section ~ div.markdown-preview-section > h4,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section ~ div.markdown-preview-section > h5,
div[src*="#"].internal-embed .markdown-embed-content>.markdown-preview-view>div.markdown-preview-sizer>div.markdown-preview-section ~ div.markdown-preview-section > h6 {

  display:block;
}

/* change the color of note title in the embed */
.markdown-embed-title {
	color: red; /*change color*/
	display: none; /*remove*/
  }

/*==============TRANSCLUSION TWEAKS=============*/
.markdown-embed-title {
	font-family: sans-serif;
	font-size: 10px;
	color: var(--text-accent); /*rgb(150,200,255);*/
	line-height: 10px;
	width: 100%;
	text-align: left;
	font-weight: 100;
	margin: -4px 0px;
}
.markdown-preview-view .markdown-embed {
	background-color: var(--background-primary);
	border-radius: 0px;
	border: 0;
	border-left: 1px solid #dcdcdc; /* was var(--text-selection) */
	margin: 0px -20px;
}
.markdown-embed {
	display: block;
	top: 0px;
}
.markdown-embed > .markdown-embed-content {
	display: inline;
	max-height: 100%;
	max-width: 100%;
	margin: -25px 0px -15px 0px;
	padding: 0px 0px 5px 0px;
}
.markdown-embed-content > * {
	display: block;
	max-height: 100%;
	max-width: 100%;
	margin: 10px 0px 5px 0px;
}
.markdown-embed-link {
	top: -3px;
	left: -20px;
	color: #484848; /* was var(--accent-strong) */
	cursor: pointer;
	position: absolute;
}
svg.link {
	width: 12px;
	height: 12px;
}
.file-embed-link {
	top: 10px;
	left: -10px;
	color: var(--accent-strong);
	cursor: pointer;
	position: relative;
}
.internal-embed, .internal-embed > .markdown-embed > .markdown-embed-content {
	display: block;
	max-height: 100%;
	max-width: 100%;
	left: 0px;
}
.markdown-preview-view .file-embed {
	background-color: var(--background-primary);
	border-radius: 4px;
	border: 2px solid var(--text-selection);
	padding: 5px 20px 5px 20px;
	margin: 10px 0px 10px 0px;
}
.file-embed-title {
	font-size: 12px;
	height: 40px;
	text-overflow: ellipsis;
	overflow: hidden;
	white-space: nowrap;
}

/* Eliminate scrollbars in transclusions (from death-au) */
.markdown-preview-view .markdown-embed-content,
.markdown-preview-view .markdown-embed-content>.markdown-preview-view {
  max-height: unset;
}
```

## Block references
```css
/* Indent embedded block reference */
.internal-embed[src*="#^"] .markdown-embed {
  padding-left: 30px;
}
```

https://discord.com/channels/686053708261228577/702656734631821413/773404255189073971

``.internal-embed` divs have a `src` attribute which has the link text in it (so if you're linking to a block ref in a page called note, it would be `src="note#^blockref"`.

The square bracket part is an attribute selector which checks if the src value contains (`*=`) `#^` — which is how you tell it's a block reference link.

If you wanted to target heading links, you'd have to use something like `.internal-embed[src*="#"]:not([src*="#^”])` (it contains `#` but not `#^`)

I guess for full page embeds it would be `.internal-embed:not([src*="#"]):not([src*="^”])`

if you want to target embeds of a specific page, you could do

`.internal-embed[src="The exact link I want”]`

you can use spaces. For example:

```css
.internal-embed[src="Lorum ipsum test"] {
    background-color: yellow;
}
```

To get just 1 embed coloured, in this example the "Lorum ipsum test" embed is yellow:

```css
.internal-embed:not([src*="#"]):not([src*="^"]) {
    background-color: blue;
}

.internal-embed[src="Lorum ipsum test"]:not([src*="#"]):not([src*="^"]) {
    background-color: yellow;
}
```

Reduce gap between adjacent block embeds:

```css
/* Reduce gap between adjacent block embed */
.markdown-preview-view .markdown-embed {
  margin-top: -20px;
  margin-bottom: -20px;
}
```



# Export to PDF
```css
/* Line up "native" blockquotes with transcluded ones in PDF */
@media print{.internal-embed{margin-left:-30px;}}

/* Page breaks */
@media print {
  h1 { 
    page-break-before: always;
  }
  h2, h3, h4, h5, h6 {
    page-break-after: avoid;
  }
  pre, blockquote {
    page-break-inside: avoid;
  }
}
```

# File explorer - Obsidian
```css
/* condense line spacing on file explorer title list. also avoids character-level word breaks */
.nav-file-title-content,
.search-result-file-title,
.search-result-file-match {
    padding-top: 0 !important;
    padding-bottom: 0 !important;
    line-height: normal !important;
    word-break: keep-all;
}

/* file xplor : smaller & bold vault title */
.nav-folder.mod-root > .nav-folder-title {
    padding-left: 6px;
    font-size: 14px;
    font-weight: bolder;
    top:-6px;   /* higher */
    cursor: default;
    color: var(--base2);
}

/* Enhancing the view of folders in left pane */
/* by Shamama on https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/112 */

/* outliner for the outline */
.outline-heading-children{
    border-left: 1px solid rgba(118,158,165,0.2);
    border-radius:0 0px 0px 0;
    transition:all 0.5s ease-in-out;
  }
 
.outline-heading-children:hover{
    border-left-color:rgba(118,158,165,0.4);
  }

/* Connectining lines for files and folders in left pane*/
.nav-folder,.nav-file{
    margin:0 !important;
    border-left: 1px solid rgba(118,158,165,0.2);
  }

/* == File Explorer - animation for active file as per Obuntu === */
.nav-file-title,
.nav-folder-title {
  padding: 0px 14px 0px 20px;
}

.nav-folder-title {
  font-weight: bold;
}

.nav-folder.mod-root > .nav-folder-title {
  padding-left: 6px;
  font-size: 14px;
  font-weight: bolder;
  top: -6px;
  cursor: default;
}

.nav-file.is-active > .nav-file-title,
.nav-file.is-active > .nav-file-title:hover {
  background-color: var(--background-primary);
  border-radius: 6px;
  font-weight: bold;
  /* color: var(--text-accent); */
  border-left: 2px solid var(--text-accent);
  transition: all 0.5s ease;
}

.nav-file.is-active > .nav-file-title {
  padding-left: 5px;
  /* margin-left: 5px; */
}

body:not(.is-grabbing) .nav-file-title:hover,
body:not(.is-grabbing) .nav-folder-title:hover {
  background-color: var(--background-primary);
  border-radius: 2px;
  transition: all 0.2s ease;
}

.nav-file-tag {
  background-color: var(--background-secondary-alt);
  top: -1px;
}

/* Folder and file icons */
.nav-folder-children .nav-file-title-content:first-child::before { content: '🗒 '; }
.nav-folder-children .nav-folder-title-content::before { content: '📂 '; }

/* add colour to folder icons - needs 2 lines of .nav-folder-children above to work*/
.nav-folder-title-content::before {

  font-size: 17px;
  /*
   how to get CSS filter ? 
  0, open website: 
 https://www.zhangxinxu.com/sp/filter.html

  1, first: image original cloro  this is :  #000
  2, second: display color   i want : #D6FFF1
  3, CSS filter trans btn clik:  the result is :
    filter: invert(99%) sepia(90%) saturate(382%) hue-rotate(69deg) brightness(106%) contrast(102%);

  4, pause👇  : OK ✌️;
  */
  filter: invert(88%) sepia(8%) saturate(554%) hue-rotate(103deg) brightness(108%) contrast(102%);

  /*
    If you want to change the icon, you only need to modify this code.you can only change d=''
  */

  content: url("data:image/svg+xml;charset=UTF-8, <svg xmlns='http://www.w3.org/2000/svg' version='1.1' viewBox='0 0 100 100' width='17' height='17'><path  fill='currentColor' stroke='currentColor'  d='M6.1,8c-3.3,0-6,2.7-6,6v73.8c-0.1,0.5-0.1,0.9,0.1,1.4c0.6,2.7,3,4.8,5.9,4.8h78c3,0,5.4-2.2,5.9-5.1 c0-0.1,0.1-0.2,0.1-0.4c0,0,0-0.1,0-0.1l0.1-0.3c0,0,0,0,0-0.1l9.9-53.6l0.1-0.2V34c0-3.3-2.7-6-6-6v-6c0-3.3-2.7-6-6-6H36.1 c0,0,0,0-0.1,0c-0.1,0-0.2-0.2-0.6-0.6c-0.5-0.6-1.1-1.5-1.7-2.5c-0.6-1-1.3-2.1-2.1-3C30.9,9,29.7,8,28.1,8L6.1,8z M6.1,12h22 c-0.1,0,0.1,0,0.6,0.6c0.5,0.6,1.1,1.5,1.7,2.5c0.6,1,1.3,2.1,2.1,3c0.8,0.9,1.9,1.9,3.6,1.9h52c1.1,0,2,0.9,2,2v6h-74 c-3.1,0-5.7,2.5-5.9,5.6h-0.1L10.1,34l-6,32.4V14C4.1,12.9,4.9,12,6.1,12z M16.1,32h78c1.1,0,2,0.9,2,2l-9.8,53.1l-0.1,0.1 c0,0.1,0,0.2-0.1,0.2c0,0.1,0,0.2-0.1,0.2c0,0,0,0.1,0,0.1c0,0,0,0,0,0.1c0,0.1,0,0.2-0.1,0.3c0,0.1,0,0.1,0,0.2 c0,0.1,0,0.2,0,0.2c-0.3,0.8-1,1.4-1.9,1.4h-78c-1.1,0-2-0.9-2-2L14,34.4l0.1-0.2V34C14.1,32.9,14.9,32,16.1,32L16.1,32z'/></svg>");

  /* margin */
  margin-right: 5px !important;
}

/*hover color*/
.nav-folder-title:hover .nav-folder-title-content::before  {

  /* hover color   #69fafd  👆   CSS filter 👇  */
  filter: invert(87%) sepia(20%) saturate(1026%) hue-rotate(113deg) brightness(105%) contrast(103%);
}

/* change font size of file explorer */
.nav-file-title, .nav-folder-title { font-size: 14px; line-height: 15px; }

/* change font size of search results */
.search-result-file-title { font-size: xyz; }
.search-result-file-matches { font-size: xyz; }

/* Reduce space of header buttons/icons - Blue Topaz */
div.nav-header{
  padding: 0px 5px 5px 5px;
  margin-bottom: 0px;
  margin-top: 5px;
  line-height: 0px;
}
div.nav-buttons-container{
  margin: 0px 0px 0px 0px;
}
input.search-input{
  margin: 0px 10px -3px 10px;
}
.nav-action-button{
  margin: 0px 2px 0px 2px !important;
}
.workspace-leaf-content[data-type='search'] .nav-action-button, .workspace-leaf-content[data-type='backlink'] .nav-action-button{
  padding: 3px 3px 3px 3px;
}

/* Fix background of folder-collapse-indicator */
body:not(.is-grabbing) .nav-folder-title:hover .nav-folder-collapse-indicator {
  background: none;
}

/* Line up tabs with macOS traffic lights */
.hider-frameless .workspace-split.mod-left-split > .workspace-tabs {
  padding: 0;}
.workspace-tab-container-inner {
  padding-left:30px;
}
```

## Nav titles

```css
/* Wrap long nav text */
.nav-file-title, .nav-folder-title {
    white-space: normal;
    width: auto;
}

/* Indent wrapped nav text */
.nav-file-title-content {
    margin-left: 10px;
    text-indent: -10px;
}

/* Set background color when hovering over a title */
.nav-file-title-content:hover {
  background-color: var(--base4);
}
```

# Font
```css
/* Font for the markdown source panel */
div.markdown-source-view {
    font-family: var(--font-family-editor);
    font-size: 0.9em;
}

/* Font for the markdown preview panel */
div.markdown-preview-view {
    font-family: var(--font-family-preview);
    font-size: 0.9em;
}

/* Editor font: make thicker */
.cm-s-obsidian .CodeMirror-line * {
    -webkit-font-smoothing: auto;
}

.cm-s-obsidian .cm-header {
    -webkit-font-smoothing: antialiased;
}

/* Coloring fonts - from Lithou on forum */
/* of italics in Edit mode all notes in a vault */
.cm-em {
    color: red;
}

/* of italics in Preview  all notes in a vault */
em {
    color: red;
}

/* Note 1: the color can be different in Edit and Preview
/* Note 2: for bold use `cm-strong` and `strong` respectively

/* Color of italics in 1 note only */
div.test em {
    color: red;
}

/* And in the note itself add to the top:
`---`
cssclass: test
`---`
```

# Footnotes
```css
/* Footnote styling - works for me w/ inline footnotes */
.footnotes-list {font-size:12px;}
.markdown-preview-section .footnotes {font-size: 80%;}
.footnotes p {margin-top: 0px;margin-bottom:5px;}

.is-flashing {
  transition: background-color 1s ease;
  background-color: orange;
}

a.footnote-link {
  color: var(--base2);
}

/* Setting the gap above and below a hor. footnote line
/* if this code block is deleted from your CSS file, the space above and below the footnote line jumps up, but changing the px values has no effect
/* footnote lines gaps can also be set with a general hr rule - see section Lines */
.markdown-preview-view
.footnotes hr {
  margin-top: 5px;
  margin-bottom: 5px;
}
```

Other possibilities:

```css
.markdown-preview-view .mod-highlighted {
  color: black;
  background-color: fuchsia;
}

.footnotes {
text-align: justify;
hyphens: auto;
font-size: 15px;
}

sup {
vertical-align: top;
font-size: 11px;
display: inline-block;
position: relative;
margin: -4px 0 0 3px;
}
sub {
vertical-align: bottom;
font-size: 11px;
display: inline-block;
position: relative;
margin: 0px 0 -4px 3px;
}
```

OR

```css
/* FROM _ph @ https://forum.obsidian.md/t/theme-obsdn-dark-rmx-now-with-light-dark-updated-2020-08-07/2225/46 */
/* also sets the colour of superscript number that lights up when return arrow is clicked */

.markdown-preview-view .mod-highlighted {
    color: #0cf32b;  /* <---- pick your color */
}

.footnotes-list {
    font-size: 13px; /* I like smaller footnotes */
}

/* set space above and below hor. line/rule */
.markdown-preview-view
.footnotes hr {
  margin-top: 3px;
  margin-bottom: 3px;
}
```

OR

```css
/* FROM DANIEL FLAUM via email */

/* Footnote styling - smaller font */
.footnote-link.mod-highlighted {
   background-color: var(--orange);
   color: var(--base3);
}

section.footnotes li {
font-size: small;
}

section.footnotes p {
font-size: small;
}
```

# Graph nodes
```css
/* to style the new nodes in the 0.9.1+ */
.theme-light .graph-view.color-arrow {
color: #5cc863;
}

.theme-light .graph-view.color-fill-tag {
  color: #440154;
}

.theme-light .graph-view.color-fill-attachment {
  color: #277f8e;
}

.theme-light .graph-view.color-fill-unresolved {
  color: #fde725; 
}
```

# Gutter line numbers
```css
/* Make subtler folding gutter arrows */
.CodeMirror-foldgutter-folded:after, .CodeMirror-foldgutter-open:after {
  opacity: 0.2;
  font-size: 70%;
}

  /*=== From Obsdn-Dark-Rmx: line nos. smaller and less bright ===*/
/*== Section name in O-D-R: codemirror line numbers gutter edit mode ====*/
.cm-s-obsidian .CodeMirror-linenumber {
    color: var(--text-accent);
    opacity : 0.8;
    font-size: 14px;
    font-family: Consolas,monospace;
}
.CodeMirror-gutter-elt {
    position: absolute;
    cursor: default;
    z-index: 4;
}
.CodeMirror-linenumber {
    padding: 0 3px 0 0px;
    min-width: 20px;
    text-align: right;
    white-space: nowrap;
}
```

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

# HTML
```css
/* HTML in editor */
/* html tags in editor */
.cm-s-obsidian span.cm-tag {
  color: var(--base4);
}

/* html comments in editor */
.cm-s-obsidian span.cm-comment {
  color: var(--base4);
}
```

# Hyphenation-Justification
```css
/* _hyphenation and justification      */
/*-------------------------------------*/
.cm-s-obsidian, .markdown-preview-view {
  text-align: justify;
  hyphens: auto;
}
```

# Images
```css
/* From BLUE TOPAZ */
/* Images : reduce displayed size of embedded files, zoom on hover */
.markdown-preview-view img, .markdown-preview-view video {
    width: auto;
    height: auto;
    object-fit: contain;
    max-height: 300px;
    max-width: 550px;
    outline: 0px solid var(--text-accent);
  }
.markdown-preview-view img:hover , .markdown-preview-view video:hover {
    width: 100%;
    height:100%;
    max-width: min(100%, 80vw);
    max-height: min(100%, 80vh);
    outline: none;
    cursor: zoom-in;
  }
```

OR

```css
/* Enlarge image on hover */
.markdown-preview-view img {
  display: block;
  margin-top: 20pt;
  margin-bottom: 20pt;
  margin-left: auto;
  margin-right: auto;
  width: 50%;  /* experiment with values */
  transition:transform 0.25s ease;
}

.markdown-preview-view img:hover {
    -webkit-transform:scale(1.8); /* experiment with values */
    transform:scale(2);
}
```

## Display side by side image grid
[Obsidian forum](https://forum.obsidian.md/t/display-side-by-side-image-grid-css-snippet/9359) by Kepano



## Image as background

```css
/* Add background image - from Gabroel */
/* can only add images from the web, not local */
.markdown-preview-section {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/Satellite_view_of_Victoria_Falls.jpg/220px-Satellite_view_of_Victoria_Falls.jpg");
  background-size: cover;
  background-size: contain;
}

/*to use a local image, upload to the web (e.g. Imgur), then reference that */
​```
```



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
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting-list-ul {
    color: transparent;
    max-width: 10px;
}
  
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting-list-ul:after {
    content: "•";
    position: absolute;
    top: 6px;
    left: 4px;
    color: var(--text-normal);
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

# Mermaid
```
​```mermaid
graph TD;

%% Class Definitions
%% =================

classDef FixFont font-size:11.5px;

%% Nodes
%% =====

A[CREATIVITY]:::FixFont --> B[Combinatorial]:::FixFont;
A[CREATIVITY]:::FixFont --> C[Exploratory]:::FixFont;
A[CREATIVITY]:::FixFont --> D[Transformational]:::FixFont;
B[Combinatorial] --> E[Problem-driven]:::FixFont;
B[Combinatorial] --> F[Similarity-driven]:::FixFont;
B[Combinatorial] --> G[Inspiration-driven]:::FixFont;

%% Node styles
%% ===========

style A fill:gold;  
style B fill:cyan;
style C fill:cyan;
style D fill:cyan;
style E fill:mediumvioletred;
style F fill:mediumvioletred;
style G fill:mediumvioletred;

​```
```

# Note title in pane
```css
/* Change the colour or the font-weight of the note title in a pane */
.view-header-title {
    /*color: red; */
    font-weight: 300; /** this range from 1 - 1000 **/
}

/* Change color of note title active pane - Obsidianite */
.workspace-leaf.mod-active .view-header-title {
  color: var(--base2);
}

/* Change icon above  vert. note title on title spine - from Obsidianite */
.view-header-icon {
    color: rgb(31, 178, 129); /* PB changed from var(--text-accent) */
}

/* Change color of line next to note title in Andy Mode - Obsidianite */
.workspace-leaf.mod-active .view-header {
  border-right: 2px solid var(--base2) !important; /* change to border-bottom in non-AM */
}
```

# Outliner pane
```css
/* connecting lines outliner */
.outline .collapsible-item-children {
    margin-left: 20px;
    border-left: 1px solid var(--text-muted);
    border-radius: 4px;
    transition:all 0.5s ease-in-out;
}

.outline .collapsible-item-children:hover {
    border-left-color: var(--text-normal);
}

/* change font color outline */
div.collapsible-item-inner {
  color: var(--base3);
}

/* indent wrapped titles outliner*/
  .outline .collapsible-item-inner {
    margin-left: 10px;
    text-indent: -10px;
}

/* List styling (numbering) for outline pane */

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline {
  counter-reset: h1;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.pane-clickable-item {
  counter-reset: h2;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h3;
}


body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h4;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h5;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item {
  counter-reset: h6;
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.pane-clickable-item:before {
  counter-increment: h1;
  content: counter(h1) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h2;
  content: counter(h1) "." counter(h2) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h3;
  content: counter(h1) "." counter(h2) "." counter(h3) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h4;
  content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h5;
  content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". ";
}

body > div > div.horizontal-main-container > div > div.workspace-split.mod-horizontal.mod-right-split > div.workspace-tabs > div.workspace-leaf > div > div.view-content > div.outline > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.outline-heading-children > div > div.pane-clickable-item:before {
  counter-increment: h6;
  content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". ";
}
```

# Popover-Popup
```css
/*============bigger link popup preview  ================*/
.popover.hover-popover {
    position: absolute;
    z-index: var(--layer-popover);
    transform: scale(0.9); /* makes the content smaller */
    max-height: 800px;    /* was 300 */
    min-height: 100px;
    width: 500px; /* was 400 */
    overflow: hidden;      
    padding: 0;
    border-bottom: none;
  }
/* I'm not sure what this does, got popove code from Obsdn-Dark-Rmx */
/*
  .popover {
    background-color: var(--background-primary);
    border: 1px solid var(--background-primary-alt);
    box-shadow: 3px 3px 7px var(--background-modifier-box-shadow);
    border-radius: 6px;
    padding: 15px 20px 10px 20px;
    position: relative;
}

/* remove-tweak the bottom gradient on the popup: remove the gradient or set height to 0 */
    .popover.hover-popover:after {
      height: 0px;    
      background: linear-gradient(to bottom, transparent, var(--background-primary) 80%, var(--background-primary));
  }

/* Colour for pop-up text in ⌘+O */
.suggestion-item.is-selected {
  background-color: blue; /* PB changed from var(--text-accent) */
  color: whitesmoke;
}
```

# Progress bar vault launch
```css
/* Vault launch progress bar change color */
.progress-bar-subline {
  position: absolute;
  background-color: var(--base2);
  height: 8px;
}

.progress-bar-line {
  position: absolute;
  opacity: 0.4;
  background-color: var(--base2);
  width: 150%;
  height: 8px;
}
```

Alternatively use this [Obsidian forum](https://forum.obsidian.md/t/progress-bar/9092/3)
```css
/* in `.theme` put: */
--interactive-accent: var(--base2)
```

Comment by “Cannibalox” (Obsidian forum) on progress bar:

> to inspect elements like this (elements that appear on specific events like hover, timer, etc) : use the PAUSE function of the devtools (f_ or CTRL ) : . open obsdian's devtools with CTRL SHIFT I or F12 . go to the `sources` tab, there is a play/pause icon in the sub-header menu . on obsidian, trigger your event (ie: hover over a link to see the popup or in your previous case, refresh Obsi with `CTRL R` to see the loading bar)
>
> while the event is active, hit F8 or CTRL / to pause obsidian (it will 'freeze' obsi until you hit F8 again)
>
> now, in devtools, switch to the `elements` tab and inspect the event as you normally would . tweak and copy your modified parameters . once you're done inspecting the css, hit F8 or CTRL \ to un-pause
>
> you can google `devtools + pause` for more infos on the process. it's easier to do than to describe really

Comment by PB:

> Klaas:
>
> The problem is the next step after finding the element that needs to be addressed is knowing the syntax that achieves what you're after.

Answer from Cannibalox:

> the devtools should provide suggestions, when you inspect to find the css corresponding to the elements, in the `styles` tab you can tweak values in real time. if you delete a value, it should provide suggestions / autocompletion. Then you copy the rule to your obsidian css. you can use https://www.w3schools.com/css to find relevant infos when you need something specific like taxonomy / syntax / commands

# Ribbons
```css
/* Ribbons */ 
/* collapse buttons: change color */
.workspace-ribbon-collapse-btn {
  color: var(--base2);
}

/* on left change background color */
.workspace-ribbon.mod-left {
  border-color: transparent;
  width: 35px;
  background: var(--base3);
}

/* on left icons: change color */
.side-dock-ribbon-tab, .side-dock-ribbon-action {
  color: var(--base2);
  text-align: center;
  font-size: 18px;
  opacity: 0.9;
}

.side-dock-ribbon-tab, .side-dock-ribbon-action:hover {
  color: var(--base5);
  text-align: center;
}

/* on right change background color */
.workspace-ribbon.mod-right {
  border-color: transparent;
  width: 30px;
  background: var(--base3);
}

/* hide Preview/Edit icon, only show on hover */
.view-action[aria-label*="Preview"], .view-action[aria-label*="Edit"] {
  opacity: 0;
}

.view-action:hover {
  opacity: 1;
}
```

# Scroll bar
```css
/* Scrollbar */
/* change width */
::-webkit-scrollbar {
  width:15px;
}

/* no rounded corners - Obsdn-dark-RMX */
::-webkit-scrollbar-thumb {
  -webkit-border-radius: 0px;
}

::-webkit-scrollbar-thumb:active {
  -webkit-border-radius: 0px;
}
```

# Search
```css
/* Global search results */
/* global search results: reduce gap between note title (bold) and hor. line above */
.search-result {
  word-break: break-word;
  margin-bottom: -4px; 
}

/* global search match highlight color */
.search-result-file-matched-text {
  background-color: lightgrey;
}

/* global search result: color of count squarelet */
.pane-list-item:hover .pane-list-item-ending-flair {
  background-color: var(--base2);
  color: white;
}

/* Local search match highlight */
/* Local (= in note) search match highlight color change in Edit mode */
.cm-s-obsidian span.obsidian-search-match-highlight {
  background-color: lightgrey; /* was fuchsia */
  color: var(--text-normal);
  }
  
/* Local (= in note) search match highlight color change in Preview mode */
.markdown-preview-view .search-highlight > div {
  background-color: darkgrey;
}

/* reduce global search result margin - Blue Topaz */
.search-result-file-match{
  padding: 0px 0px;
}

/* margin color for box for global search input */
.search-input-container input.search-input {
  border: 1px solid var(--base2);
}

.search-result-file-matched-text {
  color: var(--text-muted); 
}

.search-input {
  display: block;
  margin: 0 auto 10px auto;
  width: calc(100% - 20px);
}

.nav-action-button > svg {
  width: 17px;
  height: 17px;
}

/* align top tab header with header title - Obsdn-dark-RMX */
.workspace-leaf {
  display: flex;
  flex-direction: column;
  position: relative;
  will-change: transform;
  min-height: 20px;
}
.workspace-leaf-content[data-type='backlink'] .view-content {
  padding: 0;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  min-height: 20px;
}
.nav-header {
  padding: 8px 4px 1px 8px;
}
.nav-buttons-container {
  display: flex;
  justify-content: left;
  padding-bottom: 2px;
  border-bottom: 1px solid var(--base3);
  margin-bottom: 2px;
}

.nav-action-button > svg {
  width: 17px;
  height: 17px;
}

.nav-action-button {
  color: var(--text-muted);
  padding: 0 20px 0 10px;
  cursor: pointer;
}

.nav-files-container {
  flex-grow: 1;
  overflow-y: auto;
  padding-left: 7px;  /* reduce to 0 for more space */
  padding-bottom: 10px;
  margin-bottom: 10px;
}

/* Don't know what this does */
.cm-highlight, mark {
  background: orange;
}
```

## search results are waayyy too big
```css
/* NOTE: I picked this up from somehwere, have not used it. I use "Condense line spacing ……"

/* search results are waayyy too big */
/* These settings relate to American Typewriter font */
.search-result-file-matches {
    margin-bottom: 5px;
  }
  
.search-result-file-title {
    font-size: .83rem;
    font-weight: 600;
    line-height: 1.2rem;
    padding-left: 1.2rem !important;
    padding-right: 1.2rem !important;
}
  
.search-result-file-match {
    font-size: 12px;
}
  
.search-result-file-title,
  .search-result-file-match {
    padding: 0;
}
  
.search-result-container {
    padding: 10px 5px;
}
  
.search-result-container.mod-global-search {
    padding: 10px 15px 15px 8px;
}
  
.search-result-container.mod-global-search .search-result {
    padding-bottom: 5px;
}
  
.search-empty-state {
    font-size: 12px;
    margin: -10px 5px 15px 5px;
}
```

# Sentences
```css
/* Reduce length of sentences in full screen */
.markdown-source-view, .markdown-preview-view {
max-width: 700px;
margin: auto;
}
```

# Settings buttons colour
```css
/* Obsidian settings, change color of: */
/* the enable/disable buttons */
.checkbox-container.is-enabled {
  background-color: var(--base2);
}

/* "Check for updates" button */
button.mod-cta {
  background-color: var(--base2);
}

button.mod-cta:hover {
  background-color: var(--base3);
}

/* "Installed" button in 3rd party plug-ins tab */
span.flair.mod-pop {
  background-color: var(--base2);
}

/* tab "3rd party plugins" font color Browse button */
.setting-item-control button {
  background-color: var(--base2) !important;
  color: var(--base3);
}

.setting-item-control button:hover {
  background-color: var(--base5) !important;
  color: var(--base3);
}

/* change color of buttons in Settings > Appearance > Themes > Browse */
.modal button:not(.mod-cta):not(.mod-warning) {
  background-color: var(--base2);
}

/* "Installed plug-ins" refresh button */
.setting-editor-extra-setting-button.clickable-icon {
  color: var(--base2);
}

/* link color in the settings e.g. in description of plug-in */
a {
  color: var(--base3);
}

a:hover {
  color: var(--base3);
}
```

# Sidebar
```css
/* BOTH SIDEBARS */
/* Collapsible sidebars */
.workspace-ribbon.is-collapsed:not(:hover) .workspace-ribbon-collapse-btn, 
.workspace-ribbon.is-collapsed:not(:hover) .side-dock-actions, 
.workspace-ribbon.is-collapsed:not(:hover) .side-dock-settings {display:none;}
.workspace-ribbon.is-collapsed:not(:hover) {width: 0;}
.workspace-split.mod-left-split[style="width: 0px;"] {margin-left: 0;}
.workspace-split.mod-right-split[style="width: 0px;"] {margin-right: 0;}
.workspace-ribbon {transition: none}
```

OR

```css
.side-dock-ribbon.is-collapsed:not(:hover){ width: 0px !important; opacity: 0 }
.side-dock-ribbon.mod-right.is-collapsed:not(:hover) ~ .workspace-split.mod-right-split { margin-right: 0 }
.side-dock-ribbon.mod-left.is-collapsed:not(:hover) ~ .workspace-split.mod-left-split { margin-left: 0 }
```

```css
/* Vert. resize handle to change pane width: change color */
.workspace-leaf-resize-handle:hover {
  background-color: var(--base2);
}
```

```css
/* LEFT SIDEBAR */
/* clean up side bar empty state (e.g. unlinked mentions) */
.search-empty-state {
    width: auto;
    padding-left: 15px;
    padding-right: 15px;
    line-height: normal;
}

/* Connectining lines for files and folders in File Explorer*/
.nav-folder-children .nav-folder-children {
  margin-left: 20px;
  padding-left: 0;
  border-left: 1px solid rgba(118,158,165,0.7);
  border-radius: 4px;
  transition:all 0.5s ease-in-out;
}
.nav-folder-children .nav-folder-children:hover {
  border-left-color: rgba(118,158,165,0.7);
}

/* RIGHT SIDEBAR */
/* outliner for the outline */
.outline .collapsible-item-children {
    margin-left: 20px;
    border-left: 1px solid var(--text-muted);
    border-radius: 4px;
    transition:all 0.5s ease-in-out;
  }
.outline .collapsible-item-children:hover {
    border-left-color: var(--text-normal);
}
```

# Special effects
## Translucent modals and popovers
```css
/* Translucent modals - from: Nosedive-Obsidian */
/* Modify modal, omnibar, open looks */
input.prompt-input, input.prompt-input:active, input.prompt-input:focus {
  border-radius: 3px;
  border: 2px solid rgba(38, 38, 59, 0.5); /* in the original code this is var(--text-muted) */
  background-color: transparent;
  box-sizing: border-box;
  border-collapse: collapse;
}

.modal-bg {
  background-color: #FFFFFF01;
  backdrop-filter: blur(20px);
}

/* Make legible background for menus since we overrode the background */
div.popover.hover-popover, .menu, .suggestion-container {
  background-color: #FFFFFF01;
  backdrop-filter: blur(30px);
  border: none;
}
```
## Oval, call-out, in sidebar
/* There is an amazing piece of CSS code by [Lithou](https://forum.obsidian.md/t/how-to-achieve-css-code-snippets/8474/35?u=klaas) on the forum. I have not copied the code here because it is important to 1<sup>st</sup> see what it does. Also, check out his video that he links to.

## Sticky notes
/* From Gabroel - https://discord.com/channels/686053708261228577/702656734631821413/789334135788273724 and scroll down that page. Code was not quite correct, so here is the right code. */
```css
.stickies {
  text-align: center;
  transition: width 2s;
  padding: 5px;
  margin: 10px;
  position: relative;
  float: right;
  right: -30px;
  box-shadow: 0 10px 10px 2px rgba(0, 0, 0, 0.3);
  width: 40%;
  background: hotpink;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  -ms-transform: rotate(0deg);
  transform: rotate(2deg);
  transition: all 2s ease;
  z-index: 1;
  padding-top: 10px;
  padding-bottom: 10px;
  border-radius: 0px;
  color: black;
}

.stickies::after {
  content: "";
  left: -1%;
  top: -10px;
  background: ffff00;
  height: 40px;
  width: 15px;
  border-radius: 10px;
  border: 3px solid black;
  display: inline-block;
  position: absolute;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  -ms-transform: rotate(0deg);
  transform: rotate(-11deg);
  z-index: 11;
}

.stickies::before {
  width: 11px;
  height: 20px;
  content: "";
  background: ffff00;
  display: inline-block;
  position: absolute;
  left: -1.3%;
  top: -2px;
  border-radius: 10px;
  border: 3px solid black;
  border-bottom: 0;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
  z-index: 10;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  -ms-transform: rotate(0deg);
  transform: rotate(-11deg);
}

.stickies2 {
  position: relative;
  float: left;
  box-shadow: 0 10px 10px 2px rgba(0, 0, 0, 0.3);
  width: 30%;
  background: #edec92;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  -ms-transform: rotate(0deg);
  transform: rotate(-2deg);
  transition: all 2s ease;
  z-index: 1;
  padding: 20px;
  margin: 10px;
  color: black;
}

.stickies2::after {
  content: "";
  display: block;
  height: 32px;
  width: 2px;
  position: absolute;
  left: 50%;
  top: -10px;
  z-index: 1;
  border-radius: 50%;
  display: inline-block;
  height: 15px;
  width: 15px;
  border: 1px;
  box-shadow: inset -10px -10px 10px #f0b7a4, inset 3px 3px 5px;
}

/* Images with a piece of scotch tape effect */
/* After putting the code below, you can get the tape effect doing ![[imagename.png#tape]] */
div[src$="#tape"]::before {
  content: "";
  display: block;
  width: 100px;
  height: 30px;
  position: relative;
  top: 10px;
  margin: auto;
  background: rgba(255,255,200,0.6);
  -webkit-box-shadow: 0px 1px 3px rgba(0,0,0,0.4);
  -moz-box-shadow: 0px 1px 3px rgba(0,0,0,0.4);
  box-shadow: 0px 1px 3px rgba(0,0,0,0.4);
  z-index: 10;
  clip-path: polygon(50% 0%, 100% 0%, 
    98% 10%, 100% 20%, 98% 30%, 100% 40%, 98% 50%, 100% 60%, 98% 70%, 100% 80%, 98% 90%,100% 100%,
    0% 100%, 2% 90%, 0% 80%, 2% 70%, 0% 60%, 2% 50%, 0% 40%, 2% 30%, 0% 20%, 2% 10%, 0% 0%);
}

div[src$="#tape"] {
  float: right;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  -ms-transform: rotate(0deg);
  transform: rotate(2deg);
}
```

# Status bar
```css
/* Remove status bar */
.status-bar {display: none;}

/* Fading Status Bar and Note Controls (from MAGMA theme) */
.status-bar:hover .status-bar-item {
    opacity: 1;
    transition: opacity .1s ease-in-out;
}
.status-bar:not(:hover) .status-bar-item {
    opacity: 0.25;
    transition: opacity .25s ease-in-out;
}
.view-header:hover .view-actions {
    opacity: 1;
    transition: opacity .1s ease-in-out;
}
.view-header:not(:hover) .view-actions {
    opacity: 0.25;
    transition: opacity .25s ease-in-out;
}

/*  Flat status bar  */
.status-bar {
    background-color: var(--background-secondary-alt);
    border-top: 0px solid var(--background-modifier-border);
    color: var(--text-accent);
    font-family: "Roboto";
}
```

# Table
```css
/* Expand table cells when clicked */
.markdown-preview-view table {
  position: relative;
}
 
tr {
  position: relative;
}

td:active {
  position: absolute;
  background: black;
  width: 100%;
  left: 0;
  transition: .2s;
  transform: scale(1.02);
  border-radius: 15px;
}

/* Table as per Typora Solarized theme */
table {
  padding: 0;
  word-break: initial;
}

table tr {
  border-top: 1px solid #cccccc;
  margin: 0;
  padding: 0;
}

table tr:nth-child(2n) {
  background-color: #f8f8f8;
}

table tr th {
  font-weight: bold;
  border: 1px solid #cccccc;
  text-align: left;
  margin: 0;
  padding: 6px 13px;
}

table tr td {
  border: 1px solid #cccccc;
  text-align: left;
  margin: 0;
  padding: 6px 13px;
}

table tr th:first-child,
table tr td:first-child {
  margin-top: 0;
}

table tr th:last-child,
table tr td:last-child {
  margin-bottom: 0;
}
```

# Tag pills
```css
/* Tag pills in edit mode */
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-hashtag-end:before {
    content: '#';
}
.tag, div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-hashtag-end {
  background-color: var(--text-accent);
  border: none;
  color: white !important;
  font-size: 13px;
  padding: 1px 8px;
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
.tag[href^="#obsidian"] {
  background-color: #4d3ca6;
}

/* Tag pills in tag pane */
.tag-pane-tag-count {
  background-color: var(--text-accent);
  border: none;
  color: white;
  font-size: 11px;
  padding: 1px 8px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 0px 0px;
  cursor: pointer;
  border-radius: 14px;
}

.tag-pane-tag-text {
  background-color: var(--text-accent);
  border: none;
  color: white;
  font-size: 11px;
  padding: 1px 8px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 0px 0px;
  cursor: pointer;
  border-radius: 14px;
}

/* Change color of tag count pill when hovering */
.tag-pane-tag:hover .tag-pane-tag-count {
  color: white;
  background-color: var(--base2);
}
```

# Title bar
```css
/* Title Bar without text, custom colour */
.titlebar {
  background-color: black; (match to your theme);
  border-bottom:1px solid darkslategrey;
}

.titlebar-text,
.titlebar-button {
  display: none;
}

/* Frameless = no titlebar */
.is-frameless {
  padding-top:0px !important;
}

/* hide title bar text */
.titlebar-text {
  color: transparent;
}
```

# Tooltip
```css
/* Tooltips - from Obuntu theme */
.tooltip {
  background-color: var(--base2); /* PB changed from var(--text-accent) to (123, 108, 214) to blue */ 
  color: whitesmoke; /* was 46, 41, 56 */
  font-weight: normal;
  font-size: 12px;
}
.tooltip .tooltip-arrow {
  border-bottom: 5px solid var(--tooltip-bg);
}
```

# URLs
```css
/* Hide URLs in Edit mode - source death_au @ https://forum.obsidian.md/t/hide-or-truncate-urls-in-editor-using-css/359/2*/
div:not(.CodeMirror-activeline) > .CodeMirror-line .cm-string.cm-url:not(.cm-formatting) {
    font-size: 0;
}
div:not(.CodeMirror-activeline) > .CodeMirror-line .cm-string.cm-url:not(.cm-formatting)::after {
    content: '🔗';
    font-size: 1rem;
}
```

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

# Yaml
```css
/* remove the yaml metadata from embed */

/* Remove embed yaml first separator */
.markdown-embed-content > hr:first-child {
  display: none;
}

/* Remove embed yaml content */
.markdown-embed-content > hr:first-child + p {
  display: none;
}

/* Remove embed yaml second separator (if empty) */
.markdown-embed-content > hr:first-child + hr {
  display: none;
}

/* Remove embed yaml second separator */
.markdown-embed-content > hr:first-child + p + hr {
  display: none;
}
```


