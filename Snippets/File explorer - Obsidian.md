# File explorer - Obsidian
```css
/* condense line spacing on file explorer title list. also avoids character-level word breaks */
.nav-file-title-content,
.search-result-file-title,
.search-result-file-match {
    padding-top: 0 !important;
    padding-bottom: 0 !important;
    line-height: normal !important;
    word-break: keep-all;
}

/* file xplor : smaller & bold vault title */
.nav-folder.mod-root > .nav-folder-title {
    padding-left: 6px;
    font-size: 14px;
    font-weight: bolder;
    top:-6px;   /* higher */
    cursor: default;
    color: var(--base2);
}

/* Enhancing the view of folders in left pane */
/* by Shamama on https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/112 */

/* outliner for the outline */
.outline-heading-children{
    border-left: 1px solid rgba(118,158,165,0.2);
    border-radius:0 0px 0px 0;
    transition:all 0.5s ease-in-out;
  }
 
.outline-heading-children:hover{
    border-left-color:rgba(118,158,165,0.4);
  }

/* Connectining lines for files and folders in left pane*/
.nav-folder,.nav-file{
    margin:0 !important;
    border-left: 1px solid rgba(118,158,165,0.2);
  }

/* == File Explorer - animation for active file as per Obuntu === */
.nav-file-title,
.nav-folder-title {
  padding: 0px 14px 0px 20px;
}

.nav-folder-title {
  font-weight: bold;
}

.nav-folder.mod-root > .nav-folder-title {
  padding-left: 6px;
  font-size: 14px;
  font-weight: bolder;
  top: -6px;
  cursor: default;
}

.nav-file.is-active > .nav-file-title,
.nav-file.is-active > .nav-file-title:hover {
  background-color: var(--background-primary);
  border-radius: 6px;
  font-weight: bold;
  /* color: var(--text-accent); */
  border-left: 2px solid var(--text-accent);
  transition: all 0.5s ease;
}

.nav-file.is-active > .nav-file-title {
  padding-left: 5px;
  /* margin-left: 5px; */
}

body:not(.is-grabbing) .nav-file-title:hover,
body:not(.is-grabbing) .nav-folder-title:hover {
  background-color: var(--background-primary);
  border-radius: 2px;
  transition: all 0.2s ease;
}

.nav-file-tag {
  background-color: var(--background-secondary-alt);
  top: -1px;
}

/* Folder and file icons */
.nav-folder-children .nav-file-title-content:first-child::before { content: '🗒 '; }
.nav-folder-children .nav-folder-title-content::before { content: '📂 '; }

/* add colour to folder icons - needs 2 lines of .nav-folder-children above to work*/
.nav-folder-title-content::before {

  font-size: 17px;
  /*
   how to get CSS filter ? 
  0, open website: 
 https://www.zhangxinxu.com/sp/filter.html

  1, first: image original cloro  this is :  #000
  2, second: display color   i want : #D6FFF1
  3, CSS filter trans btn clik:  the result is :
    filter: invert(99%) sepia(90%) saturate(382%) hue-rotate(69deg) brightness(106%) contrast(102%);

  4, pause👇  : OK ✌️;
  */
  filter: invert(88%) sepia(8%) saturate(554%) hue-rotate(103deg) brightness(108%) contrast(102%);

  /*
    If you want to change the icon, you only need to modify this code.you can only change d=''
  */

  content: url("data:image/svg+xml;charset=UTF-8, <svg xmlns='http://www.w3.org/2000/svg' version='1.1' viewBox='0 0 100 100' width='17' height='17'><path  fill='currentColor' stroke='currentColor'  d='M6.1,8c-3.3,0-6,2.7-6,6v73.8c-0.1,0.5-0.1,0.9,0.1,1.4c0.6,2.7,3,4.8,5.9,4.8h78c3,0,5.4-2.2,5.9-5.1 c0-0.1,0.1-0.2,0.1-0.4c0,0,0-0.1,0-0.1l0.1-0.3c0,0,0,0,0-0.1l9.9-53.6l0.1-0.2V34c0-3.3-2.7-6-6-6v-6c0-3.3-2.7-6-6-6H36.1 c0,0,0,0-0.1,0c-0.1,0-0.2-0.2-0.6-0.6c-0.5-0.6-1.1-1.5-1.7-2.5c-0.6-1-1.3-2.1-2.1-3C30.9,9,29.7,8,28.1,8L6.1,8z M6.1,12h22 c-0.1,0,0.1,0,0.6,0.6c0.5,0.6,1.1,1.5,1.7,2.5c0.6,1,1.3,2.1,2.1,3c0.8,0.9,1.9,1.9,3.6,1.9h52c1.1,0,2,0.9,2,2v6h-74 c-3.1,0-5.7,2.5-5.9,5.6h-0.1L10.1,34l-6,32.4V14C4.1,12.9,4.9,12,6.1,12z M16.1,32h78c1.1,0,2,0.9,2,2l-9.8,53.1l-0.1,0.1 c0,0.1,0,0.2-0.1,0.2c0,0.1,0,0.2-0.1,0.2c0,0,0,0.1,0,0.1c0,0,0,0,0,0.1c0,0.1,0,0.2-0.1,0.3c0,0.1,0,0.1,0,0.2 c0,0.1,0,0.2,0,0.2c-0.3,0.8-1,1.4-1.9,1.4h-78c-1.1,0-2-0.9-2-2L14,34.4l0.1-0.2V34C14.1,32.9,14.9,32,16.1,32L16.1,32z'/></svg>");

  /* margin */
  margin-right: 5px !important;
}

/*hover color*/
.nav-folder-title:hover .nav-folder-title-content::before  {

  /* hover color   #69fafd  👆   CSS filter 👇  */
  filter: invert(87%) sepia(20%) saturate(1026%) hue-rotate(113deg) brightness(105%) contrast(103%);
}

/* change font size of file explorer */
.nav-file-title, .nav-folder-title { font-size: 14px; line-height: 15px; }

/* change font size of search results */
.search-result-file-title { font-size: xyz; }
.search-result-file-matches { font-size: xyz; }

/* Reduce space of header buttons/icons - Blue Topaz */
div.nav-header{
  padding: 0px 5px 5px 5px;
  margin-bottom: 0px;
  margin-top: 5px;
  line-height: 0px;
}
div.nav-buttons-container{
  margin: 0px 0px 0px 0px;
}
input.search-input{
  margin: 0px 10px -3px 10px;
}
.nav-action-button{
  margin: 0px 2px 0px 2px !important;
}
.workspace-leaf-content[data-type='search'] .nav-action-button, .workspace-leaf-content[data-type='backlink'] .nav-action-button{
  padding: 3px 3px 3px 3px;
}

/* Fix background of folder-collapse-indicator */
body:not(.is-grabbing) .nav-folder-title:hover .nav-folder-collapse-indicator {
  background: none;
}

/* Line up tabs with macOS traffic lights */
.hider-frameless .workspace-split.mod-left-split > .workspace-tabs {
  padding: 0;}
.workspace-tab-container-inner {
  padding-left:30px;
}
```

## Chest-of-drawers icon in nav tab - California Coast theme by mgmeyers
```css
/* Note: css variables do not work in embedded svgs, so
I took the rgb equivalents of var(--text-accent) when active
and of var(--text-faint) for not active */

/* when the tab is NOT in focus */
.theme-light
.workspace-tab-header[aria-label="File explorer"]
  .workspace-tab-header-inner-icon:after {
  opacity: 0.5;
  content: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" viewBox="0 0 24 24" style="fill:rgb(0, 0, 0);"><path d="M21,4c0-1.103-0.897-2-2-2H5C3.897,2,3,2.897,3,4v16c0,1.103,0.897,2,2,2h14c1.103,0,2-0.897,2-2V4z M5,4h14v7H5V4z M5,20 v-7h14.001v7H5z"></path><path d="M14 7L10 7 10 6 8 6 8 9 16 9 16 6 14 6zM14 15L14 16 10 16 10 15 8 15 8 18 16 18 16 15z"></path></svg>');
}

.theme-light
.workspace-tab-header[aria-label="File explorer"]:hover
  .workspace-tab-header-inner-icon:after {
  opacity: 0.5;
  content: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" viewBox="0 0 24 24" style="fill:rgb(0, 125, 228);"><path d="M21,4c0-1.103-0.897-2-2-2H5C3.897,2,3,2.897,3,4v16c0,1.103,0.897,2,2,2h14c1.103,0,2-0.897,2-2V4z M5,4h14v7H5V4z M5,20 v-7h14.001v7H5z"></path><path d="M14 7L10 7 10 6 8 6 8 9 16 9 16 6 14 6zM14 15L14 16 10 16 10 15 8 15 8 18 16 18 16 15z"></path></svg>');
}

/* when the tab is in focus */
.theme-light
.workspace-tab-header[aria-label="File explorer"].is-active
  .workspace-tab-header-inner-icon:after {
  opacity: 0.5;
  content: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" viewBox="0 0 24 24" style="fill:rgb(0, 125, 228);"><path d="M21,4c0-1.103-0.897-2-2-2H5C3.897,2,3,2.897,3,4v16c0,1.103,0.897,2,2,2h14c1.103,0,2-0.897,2-2V4z M5,4h14v7H5V4z M5,20 v-7h14.001v7H5z"></path><path d="M14 7L10 7 10 6 8 6 8 9 16 9 16 6 14 6zM14 15L14 16 10 16 10 15 8 15 8 18 16 18 16 15z"></path></svg>');
}

/* when the tab is NOT in focus */
.theme-dark
  .workspace-tab-header[aria-label="File explorer"]
  .workspace-tab-header-inner-icon:after {
  content: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" viewBox="0 0 24 24" style="fill:rgb(122,122,122);"><path d="M21,4c0-1.103-0.897-2-2-2H5C3.897,2,3,2.897,3,4v16c0,1.103,0.897,2,2,2h14c1.103,0,2-0.897,2-2V4z M5,4h14v7H5V4z M5,20 v-7h14.001v7H5z"></path><path d="M14 7L10 7 10 6 8 6 8 9 16 9 16 6 14 6zM14 15L14 16 10 16 10 15 8 15 8 18 16 18 16 15z"></path></svg>');
}

.theme-dark
  .workspace-tab-header[aria-label="File explorer"]:hover
  .workspace-tab-header-inner-icon:after {  
  content: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" viewBox="0 0 24 24" style="fill:rgb(83, 170, 245);"><path d="M21,4c0-1.103-0.897-2-2-2H5C3.897,2,3,2.897,3,4v16c0,1.103,0.897,2,2,2h14c1.103,0,2-0.897,2-2V4z M5,4h14v7H5V4z M5,20 v-7h14.001v7H5z"></path><path d="M14 7L10 7 10 6 8 6 8 9 16 9 16 6 14 6zM14 15L14 16 10 16 10 15 8 15 8 18 16 18 16 15z"></path></svg>');
}

/* when the tab is in focus */
.theme-dark
  .workspace-tab-header[aria-label="File explorer"].is-active
  .workspace-tab-header-inner-icon:after {
  content: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" viewBox="0 0 24 24" style="fill:rgb(83, 170, 245);"><path d="M21,4c0-1.103-0.897-2-2-2H5C3.897,2,3,2.897,3,4v16c0,1.103,0.897,2,2,2h14c1.103,0,2-0.897,2-2V4z M5,4h14v7H5V4z M5,20 v-7h14.001v7H5z"></path><path d="M14 7L10 7 10 6 8 6 8 9 16 9 16 6 14 6zM14 15L14 16 10 16 10 15 8 15 8 18 16 18 16 15z"></path></svg>');
}

.workspace-tab-header[aria-label="File explorer"]
  .workspace-tab-header-inner-icon:after,
.view-header-icon:after,
.search-input-clear-button:before,
.document-search-close-button:before {
  line-height: 1;
  display: inline-block;
  width: 18px;
  height: 18px;
}

.workspace-tab-header[aria-label="File explorer"]
  .workspace-tab-header-inner-icon
  > svg {
    display: none;
}
```

## Nav titles
```css
/* Wrap long nav text */
.nav-file-title, .nav-folder-title {
    white-space: normal;
    width: auto;
}

/* Indent wrapped nav text */
.nav-file-title-content {
    margin-left: 10px;
    text-indent: -10px;
}

/* Set background color when hovering over a title */
.nav-file-title-content:hover {
  background-color: var(--base4);
}
```

## Top tab container background color
```css
.theme-dark {
  --background1: rgb(51, 51, 51);
}

.theme-light {
  --background1: #f2f8fd;
}

.workspace-tab-header-container {
  background-color: var(--background1);
}

.workspace-tab-container-before.is-before-active .workspace-tab-header-inner,
.workspace-tab-container-after.is-after-active .workspace-tab-header-inner,
.workspace-tab-header.is-before-active .workspace-tab-header-inner,
.workspace-tab-header.is-after-active .workspace-tab-header-inner {
  background-color: var(--background1);
}

.workspace-tab-header,
.workspace-tab-header-inner,
.workspace-tab-container-before,
.workspace-tab-container-after {
  transition: none;
}

.workspace-tabs {
  background-color: var(--background1);
}
```

## Emojis in folder name
/* 2 examples */
```css
.nav-folder-title[data-path="+inbox"] .nav-folder-title-content::before {
  content: "📥 ";
  font-size:1.3em;
}

.nav-folder-title[data-path="+Obsidian"] .nav-folder-title-content::before {
  content: "⚙️ ";
  font-size:1.3em;
}
```

## Hide a folder
Note: If you don’t know the data-path to put in the code below, you can open the developer with 
CTRL/CMD+SHIFT+I and check the path. Beware, the data path only updates after a restart for newly file/folder.
```css
div[data-path='folder'], 
div[data-path='folder'] + div.nav-folder-children 
{
    display: none;
}
```

# Hide a file
```css
.nav-file-title[data-path="file_path.md"] {
	display: none;
}
```
