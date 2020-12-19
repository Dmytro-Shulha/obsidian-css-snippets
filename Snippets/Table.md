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
