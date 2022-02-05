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
```

## Blockquote as per Obsidianite
/* in Edit mode */
```css
.cm-quote {
    color: var(--text-normal) !important;
  }
  
div:not(.CodeMirror-activeline)>.CodeMirror-line span.cm-formatting-quote {
  color: transparent !important;
  display: inline !important;
}  
  
div:not(.CodeMirror-activeline)>.HyperMD-quote {
  border-left: 4px solid var(--text-selection);
  border-color: var(--text-accent);
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  border-top-left-radius: 3px;
  border-bottom-left-radius: 3px;
  line-height: 1.3em;
  padding: 12px 0px 15px 8.5px; /* or 12px 15px 15px 8.5px ? */
  margin-right: 15px !important;
  margin-left: 15px !important; /* or 5px ? */
  border-top: transparent;
  border-bottom: transparent;
  background: linear-gradient(120deg, var(--background-secondary), var(--text-faint));
  display: inline-block;
}
  
div:not(.CodeMirror-activeline)>.HyperMD-quote::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0px;
  height: 2px;
  width: 60%;
  background: linear-gradient(90deg, var(--text-accent), var(--text-faint));
}
  
div:not(.CodeMirror-activeline)>.HyperMD-quote::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0px;
  height: 2px;
  width: 25%;
  background: linear-gradient(90deg, var(--text-accent), var(--text-faint));
}
```

/* in Preview mode */
```css
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

/* as per Obsidianite */
/* in Edit mode */
```css
div:not(.CodeMirror-activeline)>.HyperMD-quote>span:first-of-type::before {
  content: '“' !important;
  font: 14px/20px italic Times, serif;
  font-weight: 700;
  font-size: 3em;
  color: var(--text-accent);
  left: 3px;
  top: 15px;
  position: relative;
}
```

/* in Preview mode */
```css
.markdown-preview-view blockquote p:first-of-type::before {
  content: '“';
  font: 14px/20px italic Times, serif;
  font-weight: 700;
  font-size: 3em;
  color: var(--text-accent);
  position: absolute;
  top: 0.1rem;
  left: -1.8rem;
}
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
