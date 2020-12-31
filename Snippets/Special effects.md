# Special effects
## Images - oval, banner, call-out
/* From Lithou - some 250 lines of code, which I have not added here.
/* I recommend visiting Lithou's Github page (http://github.com/lithou/sandbox), read his spiel, then download pub-Image_Flags.css */

## Side notes
/* use this syntax: <aside>some text</aside>
aside {
  float: right;
  border: 1px solid lightgrey;
  padding: 8px;
  position: relative;
  left: 10px;
  top: 20px;
  width: 155px;
  box-shadow: 0 10px 10px 2px rgba(0, 0, 0, 0.3);
  color: var(--text-accent);
}

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
