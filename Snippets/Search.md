# Search
```css
/* Global search results */
/* global search results: reduce gap between note title (bold) and hor. line above */
.search-result {
  word-break: break-word;
  margin-bottom: -4px; 
}

/* global search match highlight color */
.search-result-file-matched-text {
  background-color: lightgrey;
}

/* global search result: color of count squarelet */
.pane-list-item:hover .pane-list-item-ending-flair {
  background-color: var(--base2);
  color: white;
}

/* Local search match highlight */
/* Local (= in note) search match highlight color change in Edit mode */
.cm-s-obsidian span.obsidian-search-match-highlight {
  background-color: lightgrey; /* was fuchsia */
  color: var(--text-normal);
  }
  
/* Local (= in note) search match highlight color change in Preview mode */
.markdown-preview-view .search-highlight > div {
  background-color: darkgrey;
}

/* reduce global search result margin - Blue Topaz */
.search-result-file-match{
  padding: 0px 0px;
}

/* margin color for box for global search input */
.search-input-container input.search-input {
  border: 1px solid var(--base2);
}

.search-result-file-matched-text {
  color: var(--text-muted); 
}

.search-input {
  display: block;
  margin: 0 auto 10px auto;
  width: calc(100% - 20px);
}

.nav-action-button > svg {
  width: 17px;
  height: 17px;
}

/* align top tab header with header title - Obsdn-dark-RMX */
.workspace-leaf {
  display: flex;
  flex-direction: column;
  position: relative;
  will-change: transform;
  min-height: 20px;
}
.workspace-leaf-content[data-type='backlink'] .view-content {
  padding: 0;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  min-height: 20px;
}
.nav-header {
  padding: 8px 4px 1px 8px;
}
.nav-buttons-container {
  display: flex;
  justify-content: left;
  padding-bottom: 2px;
  border-bottom: 1px solid var(--base3);
  margin-bottom: 2px;
}

.nav-action-button > svg {
  width: 17px;
  height: 17px;
}

.nav-action-button {
  color: var(--text-muted);
  padding: 0 20px 0 10px;
  cursor: pointer;
}

.nav-files-container {
  flex-grow: 1;
  overflow-y: auto;
  padding-left: 7px;  /* reduce to 0 for more space */
  padding-bottom: 10px;
  margin-bottom: 10px;
}

/* Don't know what this does */
.cm-highlight, mark {
  background: orange;
}
```

## search results are waayyy too big
```css
/* NOTE: I picked this up from somehwere, have not used it. I use "Condense line spacing ……"

/* search results are waayyy too big */
/* These settings relate to American Typewriter font */
.search-result-file-matches {
    margin-bottom: 5px;
  }
  
.search-result-file-title {
    font-size: .83rem;
    font-weight: 600;
    line-height: 1.2rem;
    padding-left: 1.2rem !important;
    padding-right: 1.2rem !important;
}
  
.search-result-file-match {
    font-size: 12px;
}
  
.search-result-file-title,
  .search-result-file-match {
    padding: 0;
}
  
.search-result-container {
    padding: 10px 5px;
}
  
.search-result-container.mod-global-search {
    padding: 10px 15px 15px 8px;
}
  
.search-result-container.mod-global-search .search-result {
    padding-bottom: 5px;
}
  
.search-empty-state {
    font-size: 12px;
    margin: -10px 5px 15px 5px;
}
```
