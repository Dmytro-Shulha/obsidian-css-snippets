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
/* NOTE: syntax to be used to have a sticky rendered
/* <p class="stickies">Some text</p> */


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
```

/* Another sticky possibility from j314 - https://discord.com/channels/686053708261228577/702656734631821413/801873554785566760
/* NOTE: syntax to be used to have a sticky rendered
/* <p class="sticky">Some text</p> */

```css
.sticky {
  background-color:var(--yellow);
  padding:10px;
  width:300px;
  height:200px;
  color:black;
  margin-left:150px;
  font-family: chalkboard;
  box-shadow: 10px 10px 7px rgb(0,0,0,0.5);
  transform:rotate(3deg);
  transition: transform .15s linear;
}
.sticky:hover {
  transform:scale(1.1);
}
```

## Images with a piece of scotch tape effect - thanks to Lithou*/
/* placement of images */
/* After putting the code below, you can get the tape effect doing ![[imagename.png#tape]] */
/* refer to Lithou's sandbox https://github.com/lithou/sandbox */

```css
div{
    --coremarg: 1%; 
    --extramarg: 1%; /* This margin is used for any added margin between items */
    --defaultwidth: 60%; /*This is the default width for core flags such as the "side" and "tape" */
}

/* Core Flags */
/* side */

```css
        div[alt*="+side"]{
            position: relative;
            width: var(--defaultwidth);
            float: right;
            margin: 0px;
            margin-left: var(--coremarg);
        }
```

/* tape */

```css
div[alt*="+tape"] {
            position: relative;
            float: right;
            width: var(--defaultwidth);
            margin-left: var(--coremarg);
            -webkit-transform: rotate(0deg);
            -moz-transform: rotate(0deg);
            -o-transform: rotate(0deg);
            -ms-transform: rotate(0deg);
            transform: rotate(2deg);
        }
```

```css
div[alt*="+tape"]::before {
            content: "";
            display: block;
            position: relative;
            margin: auto;
            width: 100px;
            height: 30px;
            top: 12px;
            background: rgba(255, 234, 118, 0.377); /*here you can chosse the scotch tape background*/
            -webkit-box-shadow: 0px 1px 3px rgba(0,0,0,0.4);
            -moz-box-shadow: 0px 1px 3px rgba(0,0,0,0.4);
            box-shadow: 0px 1px 3px rgba(0,0,0,0.4);
            z-index: 10;
            clip-path: polygon(50% 0%, 100% 0%, 
            98% 10%, 100% 20%, 98% 30%, 100% 40%, 98% 50%, 100% 60%, 98% 70%, 100% 80%, 98% 90%,100% 100%,
            0% 100%, 2% 90%, 0% 80%, 2% 70%, 0% 60%, 2% 50%, 0% 40%, 2% 30%, 0% 20%, 2% 10%, 0% 0%);  
        }
        div[alt*="-lg"]::before{
            width: 100px;
            height: 30px;
        }

        div[alt*="-med"]::before{
            width: 70px;
            height: 25px;
        }

        div[alt*="-sm"]::before{
            width: 45px;
            height: 15px;
            top: 8px;
        }
        div[alt*="-thumb"]::before{
            width: 25px;
            height: 5px;
            top: 2px;
        }
```

/* Push Pin */

```css
div[alt*="+pin"] {
            position: relative;
            float: right;
            width: var(--defaultwidth);
            margin: auto;
            margin-left: var(--coremarg);
            -webkit-transform: rotate(0deg);
            -moz-transform: rotate(0deg);
            -o-transform: rotate(0deg);
            -ms-transform: rotate(0deg);
            transform: rotate(2deg);}
        div[alt*="+pin"]::before {
            content: "";
            position: absolute;
            width: 5px;
            height: 5px;
            background-color: #4588cc;
            top: -3%;
            left: 50%;
            border: solid #336699 8px;
            border-radius: 50%;
            box-shadow: #274d74 -5px 3px 1px;}
    /* Portrait and Landscape */
        div[alt*="+portrait"]{
            position: relative;
            width: calc(var(--defaultwidth)/2);
            float: right;
            /* background-color:blue; This setting will create a border effect of set color */
            clip-path: ellipse(36% 46% at 50% 50%);}
        div[alt*="+portrait"]>img{
            vertical-align: middle;
            clip-path: ellipse(35% 45% at 50% 50%);}
        div[alt*="+landscape"]{
            position: relative;
            width: var(--defaultwidth);
            float: right;
            /* background-color:blue; This setting will create a border effect of set color */
            clip-path: ellipse(46% 36% at 50% 50%);}
        div[alt*="+landscape"]>img{
            vertical-align: middle;
            clip-path: ellipse(45% 35% at 50% 50%);}
```

/* Banner and HR */

```css
        div[alt*="+banner"]{
            height: 100px;
            overflow: hidden;

        }

        div[alt*="+banner"]>img{
            margin-top: -130px;
            }

        div[alt*="+hr"]{
            height: 10px;
            overflow: hidden;
            border-radius: 20px;

        }

        div[alt*="+hr"]>img{
            margin-top: -200px;
            }
```        

/* Custom Core Flags */

```css
div[alt*="+custom1"]{
        position: relative;
        width: var(--defaultwidth);
        float: right;
        margin-top: 0px;
        margin-bottom: 0px;
    }
    div[alt*="+custom2"]{
        position: relative;
        width: var(--defaultwidth);
        float: right;
        margin-top: 0px;
        margin-bottom: 0px;
    }
```

/* Modifier Flags */
    /* Orientation and position */

```css
div[alt*="-left"]{
            float: left;
            margin: 0px;
            margin-right: var(--extramarg);}
        div[alt*="-right"]{
            float: right;
            margin: 0px;
            margin-left: var(--extramarg);}
        div[alt*="-fix"]{position: fixed;}
        div[alt*="-abs"]{position: absolute;}
```

/* Size */

```css
div[alt*="-thumb"]{width: 11.50%;}
        div[alt*="-sm"]{width: 24%;}
        div[alt*="-med"]{width: 32.3333%;}
        div[alt*="-lg"]{width: 49%;}
        div[alt*="-huge"]{width: 67%;}
        div[alt*="-cwidth"]{float: none;margin-left: -10%;width: 120%;}
```

/* Borders */

```css
div[alt*="-border1"]>img{border: solid black 3px;}
div[alt*="-border2"]>img{border: solid white 3px;}
div[alt*="-bradius1"]>img{border-radius: 5px;}
div[alt*="-bradius2"]>img{border-radius: 20px;}
div[alt*="-bradiustl"]>img{border-top-left-radius: 20px;}
div[alt*="-bradiusbr"]>img{border-bottom-right-radius: 20px;}
div[alt*="-bradiustr"]>img{border-top-right-radius: 20px;}
div[alt*="-bradiusbl"]>img{border-bottom-left-radius: 20px;}
div[alt*="-bthick"]>img{border-width: 5px;}
div[alt*="-bthin"]>img{border-width: 1px;}
```

/* Div Borders */

```css
div[alt*="-divborder1"]{border: solid #336699 2px;}
div[alt*="-divborder2"]{border: solid black 2px;}
div[alt*="-divbradius1"]{border-radius: 5px;}
div[alt*="-divbradius2"]{border-radius: 20px;}
div[alt*="-cdivbradius1"]{border-radius: 50px;}
```

```css
div[alt*="-shadow1"]>img{
    box-shadow: darkgrey -2px 2px 2px;

}


div[alt*="-glow"]>img{
    box-shadow: darkgrey 0px 0px 20px;
}

div[alt*="-nofloat"]{
    float:none
}
```
