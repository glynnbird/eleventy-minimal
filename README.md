# eleventy-minimal

A very minimal Eleventy template based on [this](https://github.com/arpitbatra123/eleventy-blog-mnml), but even more minimal.

- blog posts are added to the `posts` directory and appear in a list on the home page.
- compatible with GitHub Pages.
- includes template `.travis.yml` so that Travis can be used to deploy the blog to GitHub Pages (some additional config required).

This is what the rendered output looks like: https://glynnbird.github.io/eleventy-minimal/.

## How to use

Clone this repo and rename the repo to something useful (e.g. `blog`): remember with GitHub Pages that the repo name may form part of of your url e.g. https://glynnbird.github.io/eleventy-minimal/.

Add posts be creating Markdown files in the `posts` folder. Use the existing posts as guides.

Alter `index.md` to alter the content of the home page.

To see your site run `npm run serve` and visit http://localhost:8080/. Notice that if you alter and save markdown, CSS or JavaScript files, the rendered web page updates automatically. 

To just build the static files that represent your site run `npm run build`

## Travis integration with GitHub Pages

From your GitHub repo's setting's panel, enable GitHub Pages from the "gh-pages" branch and the "/" folder.

Enable Travis integration with your GitHub repo. Edit the `.travis.yml` file paying particular attention to 

- the `pathprefix` parameter which must match the name of path your GitHub Pages site is served out on e.g. `/eleventy-minimal/` or `/blog/`.
- the `GITHUB_TOKEN` is expecting your Travis integration to be configured with a developer token to allow access to your GitHub account (as described [here](https://snook.ca/archives/servers/deploying-11ty-to-gh-pages)). 

When setup correctly, whenever you publish new Markdown to the master branch, Travis will render the site with Eleventy and write the latest site to the `gh-pages` branch of the GitHub Repo. As GitHub Pages is expecting to see your HTML in the `gh-pages` branch, it's all good.

