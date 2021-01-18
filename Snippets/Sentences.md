# Sentences
```css
/* Reduce length of sentences in full screen */
.markdown-source-view, .markdown-preview-view {
max-width: 700px;
margin: auto;
}
```

# Combine Nested tag colors and Highlight colors
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
