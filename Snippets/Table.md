# Table
```css
/* Expand table cells when clicked */
.markdown-preview-view table {
  position: relative;
}
 
tr {
  position: relative;
}

td:active {
  position: absolute;
  background: black;
  width: 100%;
  left: 0;
  transition: .2s;
  transform: scale(1.02);
  border-radius: 15px;
}

/* Table as per Typora Solarized theme */
table {
  padding: 0;
  word-break: initial;
}

table tr {
  border-top: 1px solid #cccccc;
  margin: 0;
  padding: 0;
}

table tr:nth-child(2n) {
  background-color: #f8f8f8;
}

table tr th {
  font-weight: bold;
  border: 1px solid #cccccc;
  text-align: left;
  margin: 0;
  padding: 6px 13px;
}

table tr td {
  border: 1px solid #cccccc;
  text-align: left;
  margin: 0;
  padding: 6px 13px;
}

table tr th:first-child,
table tr td:first-child {
  margin-top: 0;
}

table tr th:last-child,
table tr td:last-child {
  margin-bottom: 0;
}
```

```css
/* Latex table */
/* Source: DeaconLight - https://forum.obsidian.md/t/obsidian-tables-that-look-like-latex-tables-with-css/16683 */
/* ------------------------------------*/
.academia table {
	border-collapse: collapse;
	border-spacing: 0;
	width: auto;
	max-width: 100%;
	border-top: 2.27px solid black;
	border-bottom: 2.27px solid black;
	overflow-x: auto; 
	box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
}
.academia th,
.academia td {
	border: 0 none !important;
	text-align: left;
	padding: 0.5rem;
	line-height: 1.1;
}
.academia tr:hover,
.academia td:hover {
	background-color: #cccccc;
}
.academia table > tbody > tr:first-child > td,
.academia table > tbody > tr:first-child > th {
	border-top: 1.36px solid black !important;
}
.academia table > tbody > tr:last-child > td,
.academia table > tbody > tr:last-child > th {
	border-bottom: 1.36px solid black !important;
}
.academia thead th {
    background-color: white !important;
    font-weight: 700;
}
.academia tr:nth-child(even) { background-color: #dddddd ; }
```
