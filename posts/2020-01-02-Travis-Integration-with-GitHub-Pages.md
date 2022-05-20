---
date: "2022-05-20"
title: GitHub Actions with GitHub Pages
---

To ensure that when you commit changes to your GitHub repository, your website updates we have to jump through some hoops.

An GitHub action is configured (see `./github/workflows/eleventy_build.yml`) to deploy the site to the `gh-pages`. This uses this pre-built action: https://github.com/marketplace/actions/eleventy-action.

When setup correctly, whenever you publish new Markdown to the master branch, Travis will render the site with Eleventy and write the latest site to the `gh-pages` branch of the GitHub Repo. As GitHub Pages is expecting to see your HTML in the `gh-pages` branch, it's all good.
