# nikita.html

We will show you HTML patterns, code snippets and best practices that are worth mentioning from our point of view.

Latest Release: [![GitHub version](https://badge.fury.io/gh/nikita-kit%2Fnikita-html.png)](https://github.com/nikita-kit/nikita-html/releases)

If you want to start a new project from scratch, scaffold your stack with [generator-nikita](https://github.com/nikita-kit/generator-nikita).  
If you want to write efficient and scalable (S)CSS-code for websites, try [nikita.css](https://github.com/nikita-kit/nikita-css).


## Contents

### HTML Rules

__HTML5__ is preferred for all HTML documents, so we are using:

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
- __General Formatting:__ Use a new line for every block, list, or table element and indent every such child element. Use 4 spaces for indentation.
- __Quoting:__ When quoting attributes values, use double quotation marks `" "`.
- __Label/Input:__ Every form input should utilize a `label` with a `for`-attribute..
- __Tables:__ Make use of `<thead>, <tfoot>, <tbody>, <th>`.
- __Human readable:__ Code is written and maintained by people. Ensure your code is descriptive, well commented, and approachable by others!

### DOs and DON'Ts

Under [DOs and DON'Ts](https://github.com/nikita-kit/nikita-html/tree/master/dos-and-donts) I collect cases I came across in my daily business.

## Twig

For all our web projects we use Twig as our template engine or at least twig inspired engines like [Pebble](https://pebbletemplates.io/) for Java based projects.
See the [twig documentation](http://twig.sensiolabs.org/documentation) and the [twig intro for designers](http://twig.sensiolabs.org/doc/templates.html) if you wonder how twig is working in general.
You can add custom twig functions, filters and tags in the grunt config file at `grunt/config/twigRender.js`.
See the [grunt-twig-render documentation](https://github.com/stefanullinger/grunt-twig-render) for examples.
Also, you find a list of supported twig features in the [twig.js wiki](https://github.com/twigjs/twig.js/wiki).

### the pages-folder

Every `.twig` file will result in a `.html` file after build.

### the layouts-folder

You can decorate a page using twigs `extends` tag in a page template like this:

```
{% extends '@layouts/master.twig' %}
```


### the partials-folder

You can use a partial in a page using twigs `include`, `embed` and `use` tags:

```
{% include '@partials/gitinfos.twig' %}
```
If you want to bind data to the partial you can extend it like follows:

```
{% include '@partials/gitinfos.twig' with {
    tag: 12.3
    message: 'Hello world,
} only %}
```

Please always add the `only` keyword to the data binding to avoid accidentally binding all data from the parent scope to the partial. This saves you from unintended conflicts with you're partial data.

### the macros-folder

You can import them in a page or a partial using twigs `import` tag:

```
{% import '@macros/mymacro.twig' %}
```

### the data-folder

Include them in any template with the custom twig `data` function to set a variable with its content: 

```
{% set mydata = data('@data/data.json') %}
```

## License

nikita.html is licensed under [CC0](http://creativecommons.org/publicdomain/zero/1.0/): Public Domain Dedication.
