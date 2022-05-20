# eleventy-minimal

A very minimal Eleventy blog template. So minimal that it's hardly even there.

- blog posts are added to the `posts` directory and appear in a list on the home page.
- compatible with GitHub Pages.
- includes template `.travis.yml` so that Travis can be used to deploy the blog to GitHub Pages (some additional config required).

See what it looks like and read more [https://glynnbird.github.io/eleventy-minimal/](https://glynnbird.github.io/eleventy-minimal/).

## Technologies used:

- [11ty](https://www.11ty.dev/) - simple static site generator.
- [nunjucks](https://mozilla.github.io/nunjucks/) - a rich an powerful templating language.
- [lit CSS](https://github.com/ajusa/lit) - a tiny responsive CSS framework.
- [GitHub Pages](https://pages.github.com/) - free website hosting for your projects.
- GitHub Actions to run 11ty and deploy the output to GitHub Pages

All of this is a fork of the excellent [Eleventy Minimal Blog](https://github.com/arpitbatra123/eleventy-blog-mnml) which I forked and substantially changed to make even more minimal. 

## What do all the files mean?

### `_includes`

The `_includes` directoy contains snippets of code that can either be

- incorporated into pages or other includes with `{% include "header.njk" %}`
- used as a `layout` in the _front matter_ of pages e.g https://raw.githubusercontent.com/glynnbird/eleventy-minimal/master/index.md

You can think of `_includes` as a combination of Jekyll's `_includes` & `_layouts` directory.

I've used Nunjucks files (with the `.njk` extension) - other templating languages are supported.

### `assets`

This directoy contains static assets which are moved to the destination site unchanged. This behaviour is not the default: it's set up in `.elevnty.js` [here](https://github.com/glynnbird/eleventy-minimal/blob/master/.eleventy.js#L3). This folder should be used to store static assets: JavaScript, CSS, images etc.

### `posts`

The `posts` directory contains one file per blog post, in Markdown. The directory also contains a `posts.json` which contains data which is combined with the front matter of every blog post. See [here](https://github.com/glynnbird/eleventy-minimal/blob/master/posts/posts.json).

### `.eleventy.js`

The `.eleventy.js` file contains Eleventy congifuration. It sets up the copy of `assets` to the finished site. It can also be used to add other Eleventy plugins such as syntax highlighting.


