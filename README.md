# nikita.html

We will show you HTML patterns, code snippets and best practices that are worth mentioning from our point of view.

Latest Release: [![GitHub version](https://badge.fury.io/gh/nikita-kit%2Fnikita-html.png)](https://github.com/nikita-kit/nikita-html/releases)

If you want to start a new project from scratch, try [nikita.kickstarter](https://github.com/nikita-kit/nikita-kickstarter).  
If you want to write efficient and scalable (S)CSS-code for big websites, try [nikita.css](https://github.com/nikita-kit/nikita-css).


## Contents

### HTML Rules

__HTML5__ is preferred for all HTML documents, so I'm using:

__HTML5 Elements__

sectioning: `<header>, <footer>, <nav>, <aside>, <article>, <section>` …  
grouping: `<main>, <figure>, <figcaption>` …  
text-level semantic: `<mark>, <time>` …  
multimedia: `<video>, <audio>` …  

__HTML5 Forms__

types: `date, email, number, range, search, tel, url` …  
elements: `datalist, progress, output` …  
attributes: `pattern, placeholder, required` …  


### HTML Coding Style

(This list is not intended to be exhaustive.)

- __Document Type:__ Use the HTML5 doctype `<!DOCTYPE html>`.
- __Encoding:__: Use UTF-8 `<meta charset="utf-8">`
- __Validity:__ The HTML-code should be valid where possible. You can test it with the [W3C HTML validator](http://validator.w3.org/nu/).
- __Semantics:__ Use HTML according to its purpose. For example, use heading elements `h1–h6` for headings, `p` elements for paragraphs, `a` elements for anchors etc. Tables shouldn't be used for page layout. Also try to avoid DIVitis.
- __Separation of Concerns:__ Separate structure from presentation from behavior.
- __Type Attributes:__ Omit type attributes for style sheets and scripts.
- __General Formatting:__ Use a new line for every block, list, or table element and indent every such child element. I'm using tabs instead of spaces.
- __Quoting:__ When quoting attributes values, use double quotation marks `" "`.
- __Label/Input:__ Every form input should utilize a `label` with a `for`-attribute..
- __Tables:__ Make use of `<thead>, <tfoot>, <tbody>, <th>`.
- __Human readable:__ Code is written and maintained by people. Ensure your code is descriptive, well commented, and approachable by others!

### DOs and DON'Ts

Under [DOs and DON'Ts](https://github.com/nikita-kit/nikita-html/tree/master/dos-and-donts) I collect cases I came across in my daily business.

## Questions?

If you're asking yourself _»Why not …?«_ have a look at my [WHY-NOT.md](https://github.com/nikita-kit/nikita-html/blob/master/WHY-NOT.md) file. There I might answer some common questions. :)


## License

nikita.html is licensed under [CC0](http://creativecommons.org/publicdomain/zero/1.0/): Public Domain Dedication.
