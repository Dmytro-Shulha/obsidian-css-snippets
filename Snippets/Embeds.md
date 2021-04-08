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

```css
/* Tranclusion pointing to header but leave out header, only show text below */
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
