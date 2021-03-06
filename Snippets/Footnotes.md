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

```css
/* Stop footnotes affecting line height */
sup { 
    vertical-align: top; 
    position: relative; 
    top: -0.3em; 
    font-size: 0.75em; 
}
```
