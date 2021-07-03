# Block quote inline

May be very useful to create block references to a certain paragraphs and formulas.

```css
/* Source by Murf: https://gist.github.com/GitMurf/bb68e9f48556b80d9a694eb0fd1742fe */
/* INLINE BLOCK REFS v1.0 */
:root {
    --block-ref-color: yellow;
    --block-ref-link-color: transparent;
}
.markdown-preview-view span[src*="^"].internal-embed:not(.image-embed) > div.markdown-embed {
    border-top: none;
    border-bottom-color: var(--block-ref-color);
    border-bottom-style: dashed;
    padding: 0px;
    margin: 0px;
}

.markdown-preview-view span[src*="^"].internal-embed:not(.image-embed),
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer > div,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer > div > p,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer > div > div {
    display: inline;
    padding: 0px !important;
    margin: 0px !important;
}

/* Convert bullet list block refs inline (remove the bullet) */
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer ul,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer li,
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer li > div {
    display: inline;
}
.markdown-preview-view span[src*="^"].internal-embed:not(.image-embed) > div.markdown-embed > div.markdown-embed-content > div.markdown-preview-view > div.markdown-preview-section ul {
    padding: 0px !important;
    margin: 0px !important;
}

/* Hide the block ref link unless hovered */
.markdown-preview-view span[src*="^"].internal-embed:not(.image-embed) > div.markdown-embed > div.markdown-embed-link {
    display: none;
    color: var(--block-ref-link-color);
    top: 0px;
    left: 20px;
}
/* Show the block ref link on hover */
.markdown-preview-view span[src*="^"].internal-embed:not(.image-embed) > div.markdown-embed:hover > div.markdown-embed-link {
    display: block;
}
.markdown-preview-view span[src*="^"].internal-embed:not(.image-embed) > div.markdown-embed:hover {
    border-bottom-style: solid;
}

.markdown-preview-view span[src*="^"].internal-embed:not(.image-embed) > div.markdown-embed > div.markdown-embed-content > div.markdown-preview-view > div.markdown-preview-section {
    min-height: 0px !important;
}
/* Remove line breaks on multi-line block refs */
.markdown-preview-view span[src*="^"].internal-embed > .markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer br {
    /*display: none;*/
}
```
