Based on [Dashboard++](https://github.com/TfTHacker/DashboardPlusPlus/blob/master/.obsidian/snippets/dashboard.css) by [TfT Hacker](https://github.com/TfTHacker/DashboardPlusPlus).

[link to related article on Medium](https://medium.com/obsidian-observer/dashboard-a-simple-organization-and-navigation-method-for-obsidian-vaults-2b1982d023a0)

Original css snippet have only supported lists and dataview lists.
I wanted to also have mermaid diagrams, embeds and other stuff on my diagram, so changes were made.
Done in Obsidian v1.4.3

```css
/* Updated 2023-08-20 */

.dashboard {
    padding-left: 25px !important;
    padding-right: 25px !important;
    padding-top: 20px !important;
}

.dashboard .markdown-preview-section {
    max-width: 100% !important;
}

/* Title at top of the document */
.dashboard .markdown-preview-section .title {
    top: 60px;
    position: absolute;
    font-size: 26pt !important;
    font-weight: bolder;
    letter-spacing: 8px;
}

.dashboard h1 {
    border-bottom-style: dotted !important;
    border-width: 1px !important;
    padding-bottom: 3px !important;
}

/* Get rid of the parent bullet */
.dashboard div.markdown-preview-section > div > ul > li > div.list-bullet {
    display: none !important;
}

/* Remove the indentation guide lines */
.dashboard.markdown-rendered.show-indentation-guide li > ul::before,
.dashboard.markdown-rendered.show-indentation-guide li > ol::before {
  display: none;
}

div.markdown-preview-section > div > ul.has-list-bullet > li {
    padding-left: 0px !important;
}

.dashboard div > ul, .dashboard div > p:has(span.internal-embed) {
    list-style: none;
    display: flex;
    column-gap: 50px;
    flex-flow: row wrap;
}

.dashboard div > ul > li, .dashboard div > p > span.internal-embed{
	flex: 1 1 auto;
}

/* if list have no nested lists, I want it not to be a flexbox*/
.dashboard div > ul:not(:has(li>ul)) {
	display: block;
}

/* apply flex to entire note, so all components can be part of dashboard grid */
.dashboard div.markdown-preview-section{
	display: flex;
	column-gap: 50px;
	flex-flow: row wrap;
}

/* make child elements able to take all available width */
.dashboard div.markdown-preview-section > * {
    /*min-width: 250px*/ /*or make child elements width fixed instead if needed*/
    /*width: 15%*/
	flex: 1 1 auto;
}

/*exclude elements by giving them full width*/
.dashboard div.markdown-preview-section div:has(h1,h2,h3,h4,h5,h6,hr){
	flex: 0 0 100%;
}

/*exclude note name as header on top*/
.dashboard div.markdown-preview-section > div.mod-header{
	flex: 0 0 100%;
}

/*exclude yaml frontmatter*/
.dashboard div.markdown-preview-section div:has(pre.frontmatter){
	flex: 0 0 100%;
}

/*exclude paragraphs, but not embedded notes*/
.dashboard div.markdown-preview-section div:has(p):not(:has(p>span)){
	flex: 0 0 100%;
}

/* Dataview support */
.dashboard ul.dataview {
    row-gap: 0px !important;
    list-style-type: disc !important;
}

/*I do not want yaml frontmatter to appear in view mode*/
.dashboard.markdown-preview-view .metadata-container {
  display: none !important;
}
```