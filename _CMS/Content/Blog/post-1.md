---
image: post-1-hero.jpg
description: Post 1 description to use as as excerpt.
tags:
  - tag 1
  - tag 2
---

## Heading Level 2 With Class {.style-me}

### heading level 3

paragraph {data-toggle=modal}

`inline code test`

## Syntax Highlighting Examples

A few examples of nice looking code

### JavaScript

```js
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'

Vue.use(BootstrapVue);
```

```js
var foo = function(bar) {
  return bar++
}

console.log(foo(5))
```

### Vue Template

```html
<template>
  <div>
    <h1 v-text="title" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "The Title"
    }
  }
}
</script>
```

### JSON

```json
{
  "post": true
}
```

### CSS

```css
.card {
  background: #222;
}
```


## Custom Containers like

[Markdown-It Plugin Documenation](https://github.com/markdown-it/markdown-it-container) | [VuePress's Containers Documenation](https://vuepress.vuejs.org/guide/markdown.html#custom-containers)

:::warning
Something special here! :computer: :key: :smile:
:::

:::tip
Something special here! :computer: :key: :smile:
:::

# heading 1sss

## heading 2ssss

# heading 2

- item 1
- item 2
  - item 2a
  - item 2b
- item 3

::: tip
This is a tip
:::

::: warning
This is a warninga
:::

::: danger
This is a dangerous warning
:::

::: danger STOP
Danger zone, do not proceed!
:::

[I'm an inline-style link](https://www.google.com)

- **[pica](https://nodeca.github.io/pica/demo/)** - high quality and fast image
  resize in browser.

- **[babelfish](https://github.com/nodeca/babelfish/)** - developer friendly
  i18n with plurals support and easy syntax.

- **[nuxtcms](https://github.com/davidroyer/nuxtcms/)** - the link to the the repo for this module

You will like those projects!

---

- item asssss
- item
- item 2
  - item abde
- item

## Horizontal Rules

---

## Typographic replacements

Enable typographer option to see result.

(c) (C) (r) (R) (tm) (TM) (p) (P) +-

test.. test... test..... test?..... test!....

!!!!!! ???? ,, -- ---

"Smartypants, double quotes" and 'single quotes'

## Emphasis

**This is bold text**

**This is bold text**

_This is italic text_

_This is italic text_

~~Strikethrough~~

## Blockquotes

> Blockquotes can also be nested...
>
> > ...by using additional greater-than signs right next to each other...
> >
> > > ...or with spaces between arrows.

## Lists

Unordered

- Create a list by starting a line with `+`, `-`, or `*`
- Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    - Ac tristique libero volutpat at
    - Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
- Very easy!

Ordered

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa

4) You can use sequential numbers...
5) ...or keep all the numbers as `1.`

Start numbering with offset:

57. foo
1. bar

## Code

Inline `code`

Indented code

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code



## Tables

| Option | Description                                                               |
| ------ | ------------------------------------------------------------------------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default.    |
| ext    | extension to be used for dest files.                                      |

---

Left & Right aligned columns

| Option |                                                               Description |
| :----- | ------------------------------------------------------------------------: |
| data   | path to data files to supply the data that will be passed into templates. |
| engine |    engine to be used for processing templates. Handlebars is the default. |
| ext    |                                      extension to be used for dest files. |

## Links

[link text](http://dev.nodeca.com)

[link with title](http://nodeca.github.io/pica/demo/ 'title text!')

Autoconverted link https://github.com/nodeca/pica (enable linkify to see)

## Images

![Minion](https://octodex.github.com/images/minion.png)
![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg 'The Stormtroopocat')

Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

[id]: https://octodex.github.com/images/dojocat.jpg 'The Dojocat'

## Plugins

The killer feature of `markdown-it` is very effective support of
[syntax plugins](https://www.npmjs.org/browse/keyword/markdown-it-plugin).

### [Emojies](https://github.com/markdown-it/markdown-it-emoji)

> Classic markup: :wink: :crush: :cry: :tear: :laughing: :yum:
>
> Shortcuts (emoticons): :-) :-( 8-) ;)

see [how to change output](https://github.com/markdown-it/markdown-it-emoji#change-output) with twemoji.

<!-- ### [Subscript](https://github.com/markdown-it/markdown-it-sub) / [Superscript](https://github.com/markdown-it/markdown-it-sup)

- 19^th^
- H~2~O -->

<!-- ### [\<ins>](https://github.com/markdown-it/markdown-it-ins)

++Inserted text++


### [\<mark>](https://github.com/markdown-it/markdown-it-mark)

==Marked text== -->

<!-- ### [Footnotes](https://github.com/markdown-it/markdown-it-footnote)

Footnote 1 link[^first].

Footnote 2 link[^second].

Inline footnote^[Text of inline footnote] definition.

Duplicated footnote reference[^second].

[^first]: Footnote **can have markup**

    and multiple paragraphs.

[^second]: Footnote text. -->

### [Definition lists](https://github.com/markdown-it/markdown-it-deflist)

Term 1

: Definition 1
with lazy continuation.

Term 2 with _inline markup_

: Definition 2

        { some code, part of Definition 2 }

    Third paragraph of definition 2.

_Compact style:_

Term 1
~ Definition 1

Term 2
~ Definition 2a
~ Definition 2b

### [Abbreviations](https://github.com/markdown-it/markdown-it-abbr)

This is HTML abbreviation example.

It converts "HTML", but keep intact partial entries like "xxxHTMLyyy" and so on.

\*[HTML]: Hyper Text Markup Language

### [Custom containers](https://github.com/markdown-it/markdown-it-container)

::: warning
_here be dragons_
:::
