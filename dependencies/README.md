I managed many libraries by myself instead of through npm to reduce overall file size.

**Versions**
```json
{
    "mermaid": "8.0.0",
    "plantuml": "1.2019.3",
    "wavedrom": "1.4.1",
    "reveal": "3.7.0",
    "viz": "v2.0.0",
    "MathJax": "v2.7.5",
    "jquery": "v3.2.1",
    "jquery-contextmenu": "2.6.3",
    "markdown-it": "8.4.2",
    "JavaScript-MD5": "2.7.0",
    "katex": "v0.10.2",
    "crypto-js": "3.9.1-1",
    "jquery-modal": "0.8.0",
    "vega": "5.4.0",
    "vega-lite": "3.3.0",
    "vega-embed": "4.2.0",
    "ditaa": "0.10",
    "font-awesome": "4.7",
    "flowchart": "1.11.3",
    "raphael.js": "2.2.7",
    "js-sequence-diagrams": "2.0.1",
    "webfont": "1.6.28",
    // "snap.svg": "0.5.1", // <= Doesn't work well in Preview. Use raphael.js instead
    "underscore": "1.8.3",
    "prism": "1.15.0"
}
```  

*Attention*: Need to add `window.WaveSkin = WaveSkin` at the end of **wavedrom/default.js**

*Attention*: Need to remove `font: inherit;` from `reveal.css`. Otherwise `KaTeX` and `MathJax` will have trouble rendering. Also don't forget to add the empty file `none.css`.

**cheerio 0.20.0** has bug rendering subgraph html(). `div` inside `svg` will be self-closed automatically, which is wrong. Therefore I downgrade it to 0.15.0

**cheerio 0.22.0** is buggy, restore to 0.15.0.  

*Attention*: Need to append `.mermaid ` to all selectors in `mermaid.css`, `mermaid.dark.css`, and `mermaid.forest.css`. Otherwise it will pollute `viz` graph.

*Attention*: **mpld3.v0.3.min.js** min version actually has problem, so use not minified version.  
