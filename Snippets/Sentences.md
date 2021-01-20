# Sentences
```css
/* Reduce length of sentences in full screen */
.markdown-source-view, .markdown-preview-view {
max-width: 700px;
margin: auto;
}
```

# Combine Nested tag colors and Highlight colors
use tag to highlight the whole line
Screenshot: https://forum.obsidian.md/t/how-to-achieve-css-code-snippets/8474/76?u=klaas

/*
Combine Nested tag colors and Highlight colors,
use the same colors for both nested tag and highlight.

Author:: @steve_yang331
version:: 0.0.1
Date:: 2021-1-5 
Download::https://github.com/steveyang331/Obsidian-css/


How to use code syntax:：

    #todo ==todo== 

    #important ==important== 
    
    #complete  ==complete==
 
*/


/* ---------------- 8 colors -----------------*/

/* 8 pairs base colors 

.white   rgb(255,255,255)	
.black   rgb(0,0,0)    
  
.red     rgb(255,0,0)
.aqua    rgb(0,255,255) 

.fuchsia rgb(255,0,255)   .pink
.green   rgb(0,255,0)    

.yellow  rgb(255,255,0)   
.blue    rgb(0,0,255)    


/* WYSIWYG Editor modef for highlight colors */

```css
/* Toggle highlight,strong,italic symbols 
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-strong,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-em,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-highlight,
/* Toggle highlight colors*/
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hwhite,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hblack,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hred,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-haqua,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hfuchsia,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hpink,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hgreen,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hyellow,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hblue,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hgray,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hsilver,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hmaroon,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hteal,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hpurple,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hlime,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-holive,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hwhite,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hnavy
{
    //display: none !important;
    position: relative;
}


/* Editor mode  */
.cm-hashtag ~ span.cm-highlight {
    color: white !important; /* change this color to white or black or others for light or Dark Theme */
    border-radius: 5px;
    padding-left: 5px;
	padding-right: 5px;
	font-weight: bold;
}

/* Colorful nested Tags */

.tag {
  //background-color: var(--text-accent);
  border: none;
  font-weight: bold;
  color: white;
  font-size: 16px;
  padding-left: 8px;
  padding-right: 8px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 0px 0px;
  cursor: pointer;
  border-radius: 5px;
}

.tag:hover {
color: white;
background-color: purple ;
}

/* todo */
.tag[href^="#todo"] {
  background-color: white;
  color: black;  
}

.cm-tag-todo ~ span.cm-highlight {
	background-color: rgb(255,255,255) !important;
    color: black !important;
}

a[href^="#todo"] + mark {
	background-color: rgb(255,255,255) !important;
    color: black !important;
    border-radius: 5px;
	padding-left: 8px;
	padding-right: 8px;
	font-weight: bold;
}

/* important */
.tag[href^="#important"] {
  background-color: black;
}

.cm-tag-important ~ span.cm-highlight {
	background-color: rgb(0,0,0)  !important;
    color: black !important;
}

a[href^="#important"] + mark {
	background-color: rgb(0,0,0)  !important;
    color: white !important;
    border-radius: 5px;
	padding-left: 5px;
	padding-right: 5px;
	font-weight: bold;
}

/* complete */
.tag[href^="#complete"] {
  background-color: red;
}

.cm-tag-complete ~ span.cm-highlight {
	background-color: red !important;
    color: black !important;
}

a[href^="#complete"] + mark {
	background-color: red !important;
    color: white !important;
    border-radius: 5px;
	padding-left: 5px;
	padding-right: 5px;
	font-weight: bold;
}

/* inprogress */
.tag[href^="#inprogress"] {
  background-color: aqua;
}

.cm-tag-inprogress ~ span.cm-highlight {
	background-color: aqua !important;
    color: black !important;
}

a[href^="#inprogress"] + mark {
	background-color: aqua !important;
    color: white !important;
    border-radius: 5px;
	padding-left: 8px;
	padding-right: 8px;
	font-weight: bold;
}

/* book */
.tag[href^="#book"] {
  background-color: fuchsia ;
}

.cm-tag-book ~ span.cm-highlight {
	background-color: fuchsia  !important;
    color: white !important;
}

a[href^="#book"] + mark {
	background-color: fuchsia  !important;
    color: white !important;
    border-radius: 5px;
	padding-left: 5px;
	padding-right: 5px;
	font-weight: bold;
}
/* audio */
.tag[href^="#audio"] {
  background-color: green;
}

.cm-tag-audio ~ span.cm-highlight {
	background-color: green !important;
    color: white !important;
}

a[href^="#audio"] + mark {
	background-color: green !important;
    color: white !important;
    border-radius: 5px;
	padding-left: 8px;
	padding-right: 8px;
	font-weight: bold;
}
/* video */
.tag[href^="#video"] {
  background-color: blue;
}

.cm-tag-video ~ span.cm-highlight {
	background-color: rgb(0,0,255)   !important;
    color: black !important;
}

a[href^="#video"] + mark {
	background-color: rgb(0,0,255)  !important;
    color: white !important;
    border-radius: 5px;
	padding-left: 8px;
	padding-right: 8px;
	font-weight: bold;
}
```


# Use nested tag to manage 16 highlight colors,bold,italic
/* and toggle tag , works in edit mode and preview mode. 

/*
Name:: 8 + 8 highlight colors
Author:: @steve_yang331
version:: 0.0.1
Date:: 2021-1-5
Download::
https://github.com/steveyang331/Obsidian-css/

How to use highlight code syntax:：
    #h/COLOR_name
    
    Highlighted text background , 
    Highlighted bold text ,
    Highlighted italic . 

    #h/pink ==pink== 

    #h/pink **pink**

    #h/pink _pink_
 
*/


/* ---------------- 8 + 8 colors -----------------*/

/* 8 pairs base colors 

.white   rgb(255,255,255)	
.black   rgb(0,0,0)    
  
.red     rgb(255,0,0)
.aqua    rgb(0,255,255) 

.fuchsia rgb(255,0,255) .pink
.green   rgb(0,255,0)    

.yellow  rgb(255,255,0)   
.blue    rgb(0,0,255)    

/* 8 pairs middle colors  

white/2     = .gray    rgb(128,128,128)
white*(3/4) = .silver  rgb(192,192,192)

red/2       = .maroon  rgb(128,0,0)
aqua/2      = .teal    rgb(0,128,128)

fushsia/2   = .purple  rgb(128,0,128)
green/2     = .lime    rgb(0,128,0)

yellow/2    = .olive   rgb(128,128,0)
blue/2      = .navy    rgb(0,0,128)

*/

/* WYSIWYG Editor modef for highlight colors */

```css
/* Toggle highlight,strong,italic symbols 
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-strong,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-em,
*/
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-highlight,
/* Toggle highlight colors*/
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hwhite,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hblack,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hred,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-haqua,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hfuchsia,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hpink,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hgreen,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hyellow,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hblue,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hgray,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hsilver,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hmaroon,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hteal,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hpurple,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hlime,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-holive,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hwhite,
div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-tag-hnavy
{
    display: none !important;
    position: relative;
}


/* Editor mode  */
.cm-hashtag ~ span.cm-highlight {
    color: white !important; /* change this color to white or black or others for light or Dark Theme */
    border-radius: 5px;
    padding-left: 5px;
	padding-right: 5px;
	font-weight: bold;
}


/* -- white --  */
.cm-tag-hwhite ~ span.cm-highlight {
	background-color: rgb(255,255,255) !important;
    color: black !important;
}

.cm-tag-hwhite ~ span.cm-strong {
	color: rgb(255,255,255);
}

.cm-tag-hwhite ~ span.cm-em {
	color: rgb(255,255,255);
}

/* -- black --  */
.cm-tag-hblack ~ span.cm-highlight{
	background-color: rgb(0,0,0)!important;
    color: white !important;
}

.cm-tag-hblack ~ span.cm-strong {
	color: rgb(0,0,0);
}

.cm-tag-hblack ~ span.cm-em {
	color: rgb(0,0,0);
}

/* -- red --  */
.cm-tag-hred ~ span.cm-highlight{
	background-color: rgb(255,0,0) !important;
}

.cm-tag-hred ~ span.cm-strong {
	color: rgb(255,0,0);
}

.cm-tag-hred ~ span.cm-em {
	color: rgb(255,0,0);
}

/* -- aqua --  */
.cm-tag-haqua ~ span.cm-highlight{
	background-color: rgb(0,255,255)!important;
}

.cm-tag-haqua ~ span.cm-strong {
	color: rgb(0,255,255);
}

.cm-tag-haqua ~ span.cm-em {
	color: rgb(0,255,255);
}

/* -- fuchsia --  */
.cm-tag-hfuchsia ~ span.cm-highlight{
	background-color: rgb(255,0,255)!important;
}

.cm-tag-hfuchsia ~ span.cm-strong {
	color: rgb(255,0,255);
}

.cm-tag-hfuchsia ~ span.cm-em {
	color: rgb(255,0,255);
}


/* -- pink --  */
.cm-tag-hpink ~ span.cm-highlight{
	background-color: rgb(255,0,255)!important;
}

.cm-tag-hpink ~ span.cm-strong {
	color: rgb(255,0,255);
}

.cm-tag-hpink ~ span.cm-em {
	color: rgb(255,0,255);
}

/* -- green --  */
.cm-tag-hgreen ~ span.cm-highlight{
	background-color: rgb(0,255,0)!important;
}

.cm-tag-hgreen ~ span.cm-strong {
	color: rgb(0,255,0);
}

.cm-tag-hgreen ~ span.cm-em {
	color: rgb(0,255,0);
}

/* -- yellow --  */
.cm-tag-hyellow ~ span.cm-highlight{
	background-color: rgb(255,255,0) !important;
    color: black !important;
}

.cm-tag-hyellow ~ span.cm-strong {
	color: rgb(255,255,0) ;
}

.cm-tag-hyellow ~ span.cm-em {
	color: rgb(255,255,0) ;
}


/* -- blue --  */
.cm-tag-hblue ~ span.cm-highlight{
	background-color: rgb(0,0,255) !important;
}

.cm-tag-hblue ~ span.cm-strong {
	color: rgb(0,0,255);
}

.cm-tag-hblue ~ span.cm-em {
	color: rgb(0,0,255);
}


/* -- gray --  */
.cm-tag-hgray ~ span.cm-highlight{
	background-color: rgb(128,128,128) !important;
}

.cm-tag-hgray ~ span.cm-strong {
	color: rgb(128,128,128);
}

.cm-tag-hgray ~ span.cm-em {
	color: rgb(128,128,128);
}

/* -- silver --  */
.cm-tag-hsilver ~ span.cm-highlight{
	background-color: rgb(192,192,192) !important;
}

.cm-tag-hsilver ~ span.cm-strong {
	color: rgb(192,192,192);
}

.cm-tag-hsilver ~ span.cm-em {
	color: rgb(192,192,192);
}

/* -- maroon --  */
.cm-tag-hmaroon ~ span.cm-highlight{
	background-color: rgb(128,0,0) !important;
}

.cm-tag-hmaroon ~ span.cm-strong {
	color: rgb(128,0,0);
}

.cm-tag-hmaroon ~ span.cm-em {
	color: rgb(128,0,0);
}

/* -- teal --  */
.cm-tag-hteal ~ span.cm-highlight{
	background-color: rgb(0,128,128)!important;
}

.cm-tag-hteal ~ span.cm-strong {
	color: rgb(0,128,128);
}

.cm-tag-hteal ~ span.cm-em {
	color: rgb(0,128,128);
}

/* -- teal --  */
.cm-tag-hpurple ~ span.cm-highlight{
	background-color: rgb(128,0,128)!important;
}

.cm-tag-hpurple ~ span.cm-strong {
	color: rgb(128,0,128);
}

.cm-tag-hpurple ~ span.cm-em {
	color: rgb(128,0,128);
}

/* -- lime --  */
.cm-tag-hlime ~ span.cm-highlight{
	background-color: rgb(0,128,0)!important;
}

.cm-tag-hlime ~ span.cm-strong {
	color: rgb(0,128,0);
}

.cm-tag-hlime ~ span.cm-em {
	color: rgb(0,128,0);
}

/* -- olive --  */
.cm-tag-holive ~ span.cm-highlight{
	background-color: rgb(128,128,0)!important;
}

.cm-tag-holive ~ span.cm-strong {
	color: rgb(128,128,0);
}

.cm-tag-holive ~ span.cm-em {
	color: rgb(128,128,0);
}

/* -- navy --  */
.cm-tag-hnavy ~ span.cm-highlight{
	background-color: rgb(0,0,128)!important;
}

.cm-tag-hnavy ~ span.cm-strong {
	color: rgb(0,0,128);
}

.cm-tag-hnavy ~ span.cm-em {
	color: rgb(0,0,128);
}


/*----------------------- Preview mode ------------------------ */

a[href^="#h/"]{
    display:none !important;  
}


a[href^="#h/"] + mark {
    color: white !important; /* change this color to white or black or others for light or Dark Theme */
	border-radius: 5px;
	padding-left: 5px;
	padding-right: 5px;
	font-weight: bold;
}

/* -- white --  */
a[href^="#h/white"] + mark {
	background-color: rgb(255,255,255) !important;
    color: black !important;
}

a[href^="#h/white"] + strong {
	color: rgb(255,255,255);
}

a[href^="#h/white"] + em {
	color: rgb(255,255,255);
}

/* -- black --  */
a[href^="#h/black"] + mark {
	background-color: rgb(0,0,0)!important;
}

a[href^="#h/black"] + strong {
	color: rgb(0,0,0);
}

a[href^="#h/black"] + em {
	color: rgb(0,0,0);
}

/* -- red --  */
a[href^="#h/red"] + mark {
	background-color: rgb(255,0,0) !important;
}

a[href^="#h/red"] + strong {
	color: rgb(255,0,0);
}

a[href^="#h/red"] + em {
	color: rgb(255,0,0);
}

/* -- aqua --  */
a[href^="#h/aqua"] + mark {
	background-color: rgb(0,255,255)!important;
}

a[href^="#h/aqua"] + strong {
	color: rgb(0,255,255);
}

a[href^="#h/aqua"] + em {
	color: rgb(0,255,255);
}

/* -- fuchsia --  */
a[href^="#h/fuchsia"] + mark {
	background-color: rgb(255,0,255)!important;
}

a[href^="#h/fuchsia"] + strong {
	color: rgb(255,0,255);
}

a[href^="#h/fuchsia"] + em {
	color: rgb(255,0,255);
}


/* -- pink --  */
a[href^="#h/pink"] + mark {
	background-color: rgb(255,0,255)!important;
}

a[href^="#h/pink"] + strong {
	color: rgb(255,0,255);
}

a[href^="#h/pink"] + em {
	color: rgb(255,0,255);
}

/* -- green --  */
a[href^="#h/green"] + mark {
	background-color: rgb(0,255,0)!important;
}

a[href^="#h/green"] + strong {
	color: rgb(0,255,0);
}

a[href^="#h/green"] + em {
	color: rgb(0,255,0);
}

/* -- yellow --  */
a[href^="#h/yellow"] + mark {
	background-color: rgb(255,255,0) !important;
    color: black !important;
}

a[href^="#h/yellow"] + strong {
	color: rgb(255,255,0) ;
}

a[href^="#h/yellow"] + em {
	color: rgb(255,255,0) ;
}


/* -- blue --  */
a[href^="#h/blue"] + mark {
	background-color: rgb(0,0,255) !important;
}

a[href^="#h/blue"] + strong {
	color: rgb(0,0,255);
}

a[href^="#h/blue"] + em {
	color: rgb(0,0,255);
}


/* -- gray --  */
a[href^="#h/gray"] + mark {
	background-color: rgb(128,128,128) !important;
}

a[href^="#h/gray"] + strong {
	color: rgb(128,128,128);
}

a[href^="#h/gray"] + em {
	color: rgb(128,128,128);
}

/* -- silver --  */
a[href^="#h/silver"] + mark {
	background-color: rgb(192,192,192) !important;
}

a[href^="#h/silver"] + strong {
	color: rgb(192,192,192);
}

a[href^="#h/silver"] + em {
	color: rgb(192,192,192);
}

/* -- maroon --  */
a[href^="#h/maroon"] + mark {
	background-color: rgb(128,0,0) !important;
}

a[href^="#h/maroon"] + strong {
	color: rgb(128,0,0);
}

a[href^="#h/maroon"] + em {
	color: rgb(128,0,0);
}

/* -- teal --  */
a[href^="#h/teal"] + mark {
	background-color: rgb(0,128,128)!important;
}

a[href^="#h/teal"] + strong {
	color: rgb(0,128,128);
}

a[href^="#h/teal"] + em {
	color: rgb(0,128,128);
}

/* -- teal --  */
a[href^="#h/purple"] + mark {
	background-color: rgb(128,0,128)!important;
}

a[href^="#h/purple"] + strong {
	color: rgb(128,0,128);
}

a[href^="#h/purple"] + em {
	color: rgb(128,0,128);
}

/* -- lime --  */
a[href^="#h/lime"] + mark {
	background-color: rgb(0,128,0)!important;
}

a[href^="#h/lime"] + strong {
	color: rgb(0,128,0);
}

a[href^="#h/lime"] + em {
	color: rgb(0,128,0);
}

/* -- olive --  */
a[href^="#h/olive"] + mark {
	background-color: rgb(128,128,0)!important;
}

a[href^="#h/olive"] + strong {
	color: rgb(128,128,0);
}

a[href^="#h/olive"] + em {
	color: rgb(128,128,0);
}

/* -- navy --  */
a[href^="#h/navy"] + mark {
	background-color: rgb(0,0,128)!important;
}

a[href^="#h/navy"] + strong {
	color: rgb(0,0,128);
}

a[href^="#h/navy"] + em {
	color: rgb(0,0,128);

```
