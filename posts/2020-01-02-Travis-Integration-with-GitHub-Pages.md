---
date: "2020-01-02"
title: Travis integration with GitHub Pages
---

To ensure that when you commit changes to your GitHub repository, your website updates we have to jump through some hoops.

- From your GitHub repo's setting's panel, enable GitHub Pages from the "gh-pages" branch and the "/" folder.
- Enable Travis integration with your GitHub repo. Edit the `.travis.yml` file paying particular attention to 
- the `pathprefix` parameter which must match the name of path your GitHub Pages site is served out on e.g. `/eleventy-minimal/` or `/blog/`.
- the `GITHUB_TOKEN` is expecting your Travis integration to be configured with a developer token to allow access to your GitHub account (as described [here](https://snook.ca/archives/servers/deploying-11ty-to-gh-pages)). 

When setup correctly, whenever you publish new Markdown to the master branch, Travis will render the site with Eleventy and write the latest site to the `gh-pages` branch of the GitHub Repo. As GitHub Pages is expecting to see your HTML in the `gh-pages` branch, it's all good.
