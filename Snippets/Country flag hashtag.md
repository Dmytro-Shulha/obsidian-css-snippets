# Country flag hashtag
```css
/* Country flag when using hashtag of ISO language code - original */
/* Source: https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/33?u=klaas */
.tag[href="#eng"]{

  color: black;
  background: #b5fbac;
  text-shadow:  20px 20px 60px #9ad592, 
             -20px -20px 60px #d0ffc6;
}

.tag[href="#eng"]:before {
  color: white;
  content: "🇺🇸";
  padding: -20pt -20pt 15pt 5pt;
  margin: 0pt;
  font-size: 15pt;
}

.tag[href="#eng"]:hover {

border-radius: 14px;
background: #b5fbac;
box-shadow:  20px 20px 60px #9ad592, 
             -20px -20px 60px #d0ffc6;
}

/* Used by PB in Solarized */
.tag[href="#nl"]{
  color: black;
  background: var(--base3);
}

.tag[href="#nl"]:before {
  color: black;
  content: "🇳🇱";
  padding: -20pt -20pt 15pt 5pt;
  margin: 0pt;
  font-size: 15pt;
}

.tag[href="#nl"]:hover {
border-radius: 14px;
background: var(--base3);
}
```
