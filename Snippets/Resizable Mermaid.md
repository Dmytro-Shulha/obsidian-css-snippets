# Resizable Mermaid Diagrams

```css
svg[id^="m"][width][height][viewBox] {
    max-width: 95%;
    max-height: 95%;
}

div.mermaid {
    margin-left: 0 !important;
    text-align: center;
    resize:both;
    overflow:auto;
    margin-bottom: 2px;
    position:relative;
    max-height: 600px;
    max-width: 100%;
}

div.mermaid::after {
    content:'';
    display:block;
    width:10px;
    height:10px;
    background-color:yellowgreen;
    position:absolute;
    right:0;
    bottom:0;
}
```

![](https://raw.githubusercontent.com/tctco/ImgHosting/master/mermaidResize.gif)
