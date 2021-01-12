# Images
```css
/* From BLUE TOPAZ */
/* Images : reduce displayed size of embedded files, zoom on hover */
.markdown-preview-view img, .markdown-preview-view video {
    width: auto;
    height: auto;
    object-fit: contain;
    max-height: 300px;
    max-width: 550px;
    outline: 0px solid var(--text-accent);
  }
.markdown-preview-view img:hover , .markdown-preview-view video:hover {
    width: 100%;
    height:100%;
    max-width: min(100%, 80vw);
    max-height: min(100%, 80vh);
    outline: none;
    cursor: zoom-in;
  }
```

OR

```css
/* Enlarge image on hover */
.markdown-preview-view img {
  display: block;
  margin-top: 20pt;
  margin-bottom: 20pt;
  margin-left: auto;
  margin-right: auto;
  width: 50%;  /* experiment with values */
  transition:transform 0.25s ease;
}

.markdown-preview-view img:hover {
    -webkit-transform:scale(1.8); /* experiment with values */
    transform:scale(2);
}
```

## Display side by side image grid
[Obsidian forum](https://forum.obsidian.md/t/display-side-by-side-image-grid-css-snippet/9359) by Kepano



## Image as background

```css
/* Add background image - from Gabroel */
/* can only add images from the web, not local */
.markdown-preview-section {
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/Satellite_view_of_Victoria_Falls.jpg/220px-Satellite_view_of_Victoria_Falls.jpg");
  background-size: cover;
  background-size: contain;
}
```
/*to use a local image, upload to the web (e.g. Imgur), then reference that */
