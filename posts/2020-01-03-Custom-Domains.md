---
date: "2020-01-03"
title: Custom Domains
---

It should be possible to setup a custom domain using 
[GitHub's instructions](https://docs.github.com/articles/using-a-custom-domain-with-github-pages/). 
The only thing to watch out for is that the `.travis.yml` file will have to have a value 
of `/` for `--pathprefix` because custom domain sites are served out at the root of the website, 
as opposed to default GitHub Pages sites.
 
You'll also need a CNAME file in the root of your main/master branch containing the domain name
you are using e.g.

```
mycustomdomain.com
```

Also look in the `.eleventy.js` where you'll need to uncomment the line which copies this CNAME
file to the root of the finished site.
