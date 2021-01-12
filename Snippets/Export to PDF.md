# Export to PDF
```css
/* Line up "native" blockquotes with transcluded ones in PDF */
@media print{.internal-embed{margin-left:-30px;}}

/* Page breaks */
@media print {
  h1 { 
    page-break-before: always;
  }
  h2, h3, h4, h5, h6 {
    page-break-after: avoid;
  }
  pre, blockquote {
    page-break-inside: avoid;
  }
}
```
