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
```

```css
/* change the color of note title in the embed */
.markdown-embed-title {
	color: red; /*change color*/
	display: none; /*remove*/
 }
 ``` 

## TRANSCLUSION TWEAKS
```css
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
```

## Transclusions/clean-embeds
### Clean embeds on a per note basis
```css
    Removes title, link, padding, margins from embeds,
    so they really look like the same note.

   PLEASE NOTE: To be used with `cssclass: clean-embeds` in YAML frontmatter.

    2021-05-25 Matthias C. Hormann (Moonbase59)
    TODO: Find out how to correct PDF export. L/R margins & vspace too large on embeds.
*/

/* remove title and link */
.markdown-preview-view.clean-embeds .markdown-embed-title,
.markdown-preview-view.clean-embeds .markdown-embed-link {
  display: none;
}

/* remove border and scroll */
.markdown-preview-view.clean-embeds .markdown-embed,
.markdown-preview-view.clean-embeds .file-embed {
  border: none;
  padding: 0;
  margin: 0;
}

.markdown-preview-view.clean-embeds .markdown-embed-content,
.markdown-preview-view.clean-embeds .markdown-embed-content > .markdown-preview-view { 
  max-height: unset;
  padding: 0;
  margin: 0;
}

/* remove <br> between internal embeds */
.clean-embeds .markdown-preview-section div > p br,
.clean-embeds .markdown-preview-section div > br {
  display: none;
}

/* remove vertical space added by markdown-preview-sizer */
.clean-embeds div.markdown-preview-sizer.markdown-preview-section {
  min-height: unset !important;
  padding-bottom: 0 !important;
}

/* special considerations for printing (PDF export) */
@media print {

  /* remove frontmatter if "Show frontmatter" was enabled */
  .markdown-preview-view .frontmatter {
    display: none;
  }
}
```

### Clean embeds on a vault-wide basis, alternative for Naked embeds below

/* NOTE: THIS VERSION OF CLEAN EMBEDS DOES **NOT** REQUIRE
A `CSSCLASS` TO BE SET, THIS VERSION IS VAULT-WIDE, LIKE
DEATH_AU'S NAKED EMBED CODE */

/*
    clean-embeds-all.css snippet

    Removes title, link, padding, margins from embeds,
    so they really look like the same note.

    This will not require a `cssclass` to be set but work for _all_ notes.
    Derived from the `clean-embeds.css` snippet.

    2021-05-27 Matthias C. Hormann (Moonbase59)

    TODO: Find out how to correct PDF export. L/R margins & vspace too large on embeds.
*/

```css
/* remove title and link */
.markdown-preview-view .markdown-embed-title,
.markdown-preview-view .markdown-embed-link { /* comment out this line if Option 1A & 1B are used */
    display: none;
}
    
/* remove border and scroll */
.markdown-preview-view .markdown-embed,
.markdown-preview-view .file-embed {
    border: none;
    padding: 0;
    margin: 0;
}
    
.markdown-preview-view .markdown-embed-content,
.markdown-preview-view .markdown-embed-content > .markdown-preview-view { 
    max-height: unset;
    padding: 0;
    margin: 0;
}
    
/* remove <br> between internal embeds */
.markdown-preview-section div > p br,
.markdown-preview-section div > br {
    display: none;
}
    
    
/* remove vertical space added by markdown-preview-sizer */
div.markdown-preview-sizer.markdown-preview-section {
    min-height: unset !important;
    padding-bottom: 0 !important;
}
    
/* special considerations for printing (PDF export) */
@media print {
    
/* remove frontmatter box if "Show frontmatter" was enabled */
    pre.frontmatter {
    display: none;
    }
}

Optional
/* LINK ICON */
.markdown-embed-link,
.file-embed-link {
  top:0px;
  right:0;
  text-align:right;
}

/* hide */
.file-embed-link svg,
.markdown-embed-link svg {
  width:16px;
  opacity:0;
}

/* show on hover */
.markdown-embed:hover .file-embed-link svg,
.markdown-embed:hover .markdown-embed-link svg {
  opacity:1;
}
```

## Naked embeds
courtesy death_au
```css
.markdown-embed-title { display:none; }
.markdown-preview-view .markdown-embed { border:none; padding:0; margin: 0; }
.markdown-preview-view .markdown-embed-content { max-height: unset;}
.markdown-preview-view .markdown-embed-content>:first-child { margin-top: 0; }
.markdown-preview-view .markdown-embed-content>:last-child { margin-bottom: 0; }

/* remove vertical space added by markdown-preview-sizer */
div.markdown-preview-sizer.markdown-preview-section {
  min-height: unset !important;
  padding-bottom: 0 !important;
}

Optional
/* LINK ICON */
.markdown-embed-link,
.file-embed-link {
  top:0px;
  right:0;
  text-align:right;
}

/* hide */
.file-embed-link svg,
.markdown-embed-link svg {
  width:16px;
  opacity:0;
}

/* show on hover */
.markdown-embed:hover .file-embed-link svg,
.markdown-embed:hover .markdown-embed-link svg {
  opacity:1;
}
```

## Eliminate scrollbars in transclusions (from death-au)
```css
.markdown-preview-view .markdown-embed-content,
.markdown-preview-view .markdown-embed-content>.markdown-preview-view {
  max-height: unset;
}
```

## Tranclusion pointing to header but leave out header, only show text below
```css
.internal-embed .markdown-embed h1,
.internal-embed .markdown-embed h2,
.internal-embed .markdown-embed h3,
.internal-embed .markdown-embed h4,
.internal-embed .markdown-embed h5,
.internal-embed .markdown-embed h6 {
    display: none;
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

## To get just 1 embed coloured, in this example the "Lorum ipsum test" embed is yellow:
```css
.internal-embed:not([src*="#"]):not([src*="^"]) {
    background-color: blue;
}

.internal-embed[src="Lorum ipsum test"]:not([src*="#"]):not([src*="^"]) {
    background-color: yellow;
}
```

## Reduce gap between adjacent block embeds:
```css
/* Reduce gap between adjacent block embed */
.markdown-preview-view .markdown-embed {
  margin-top: -20px;
  margin-bottom: -20px;
}
```

## Videos
```css
/* Embedded video */
/* NOTE: ADD THE CODE BELOW TO YOUR NOTE OR A TEMPLATE
/* REPLACE THE SECTION "https://......PASTE_ID" WITH THE VIDEO ID OF THE TO-BE-EMBEDDED VIDEO
<div class\="videoWrapper"\>
<iframe width\="560" height\="315" src\="https://www.youtube.com/embed/PASTE_ID"

.videoWrapper {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 */
  height: 0;
  margin-bottom: 3%;
}
.videoWrapper iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```
