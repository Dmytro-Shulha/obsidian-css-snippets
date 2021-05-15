```css
/* Sidenote in line with the main text */
aside {
  float: right;
  border: 1px solid lightgrey;
  padding: 8px;
  padding-top: 0px;
  position: relative;
  left: 10px;
  top: 5px;
  width: 300px; /*PB changed from 155px */
  box-shadow: 5px 10px 10px 2px rgba(119, 119, 119, 0.3);
  color: var(--text-accent);
  font-size: 14px;
  border-radius: 4px;
}
```

```css
/* to put the sidenote in the right gutter, add this rule to the code above */
margin-right: -20em;
```

```css
/*-Comments/Asides- source: ITS theme
Syntax to be used in the note: <s class="aside-…">text</s>
and replace … with show or hide or in */

/*Show Aside*/
.aside-show {
    text-decoration: unset;
    text-align: justify;
    font-weight: unset;
    float: right;
    position: relative;
    margin-right: -23em;
    margin-bottom: .2em;
    clear: right;
    width: 300px; /* PB changed from 400 */
    background-color: var(--background-primary-alt);
    padding: 0.2em 1em 1em 1em; /* PB changed from padding: 1em >> the 4 values */ 
    box-shadow: .3em .3em var(--interactive-accent);
    font-size: 14.5px; /* PB added this */
    border-radius: 4px; /* PB added this */
}

/*Hide Aside and hover to reveal it*/
.aside-hide {
    text-decoration: unset;
    text-align: justify;
    color: transparent;
    font-weight: unset;
    float: right;
    position: relative;
    margin: .5em;
    margin-right: -1.8em;
    width: 1.5em;
    height: 1.5em;
    clear: right;
    overflow: hidden;
    background-color: var(--background-primary-alt);
    color: transparent;
}
.aside-hide:before {
    display: block;
    border-bottom: 2px solid var(--background-modifier-border);
    content: "🗨 ";
    color: none;
    text-shadow: 0 0 0 var(--interactive-accent);
    font-size: 12px;
    padding-top: .1em;
    padding-left: .3em;
}
.aside-hide:hover {
    white-space: normal;
    text-overflow: unset;
    color: unset;
    width: 300px; /* PB changed from 400 */
    height: unset;
    background-color: var(--background-primary-alt);
    padding: 1em;
    padding-top: .5em;
    z-index: 3;
    /*box-shadow: .5em .5em var(--outer-bar);*/
    border-right: 2px solid var(--interactive-accent);
    font-size: 14.5px; /* PB added this */
    border-radius: 4px; /* PB added this */
}

/*Aside Inside the Note*/
.aside-in {
    text-decoration: none !important;
    text-align: justify;
    font-weight: unset;
    float: right;
    position: relative;
    margin-bottom: .2em;
    clear: right;
    width: 18em;
    background-color: var(--background-primary-alt);
    padding: 1em;
    box-shadow: .3em .3em var(--interactive-accent);
    z-index: 3;
    font-size: 14.5px; /* PB added this */
    border-radius: 4px; /* PB added this */
}

.aside-in .internal-embed.is-loaded:not(.image-embed),
.aside-in .markdown-embed {
    width:100%;
}
/*Shrink Scrollbar*/
.aside > ::-webkit-scrollbar {
    width: 5px;
}
```
