---
layout: post
title:  "Making GitHub Pages blog"
date:   2023-01-28 21:26:58 +0100
categories: blog
excerpt: This is the first article in this blog, so I would like to share some information about the process of setting up GitHub Pages with Jekyll.
---

Hello there.

This is the first article in this blog, so I would like to share
some information about the process
of setting up GitHub Pages with Jekyll.

I won't describe the whole process. The documentation does it well.
Still, there are some things that are not covered in the documentation
but you may face them. Actually, if you never worked with Jekyll or
GitHub Pages before, you will face them for sure.

The list of links you will need to set up the GitHub Pages with Jekyll:

- [Installing Ruby][installing-ruby]
- [Jekyll Quickstart Guide][jekyll-docs]
- [Setting up a GitHub Pages site with Jekyll][jekyll-ghp-setup-doc]
- [Configuring publishing source for GitHub Pages site][ghp-publishing-source]
- [Jekyll & GitHub Pages Troubleshooting][ghp-troubleshooting]

All these resources contain all the information you need to set up GitHub Pages blog with Jekyll.
Still, there are some aspects not covered by these documents.

### Issue #1 - Add webrick gem to the project

If you have Ruby v.3.0.0 or newer, then you need to run this command to be able
running your site locally with Jekyll.

```shell
bundle add webrick
```

### Issue #2 - Blank page with the remote theme

This one is very annoying. You can assign a theme for your Jekyll sites.
Actually, GitHub has great support for some of them. But neither GitHub's nor Jekyll's
documentation doesn't tell much about the proper steps to use different themes.

That may happen because of several reasons:
1. Theme is not compatible with your Jekyll version, the solution: pick another theme
2. Some themes require additional configuration in `_config.yml`, usually it is described in the readme in the theme's repository on GitHub
3. Theme's layouts are different from the ones from the default theme,
   to fix that you need to explore the theme's source code and check `_layouts` folder,
   check that your markdown pages use those layouts and not the other ones.

### Issue #3 - Jekyll does not support Windows officially

Meaning that Windows users must suffer. Again.

Of course, there is a way to make things work. Still, there is no guarantee it will.
But you can try [this documentation][jekyll-win], maybe it will help. Or maybe not :D

Despite the good initial documentation those tools still have some problems, like any Open Source product.
Maybe you will face them, maybe not. But knowing this will help you set up GitHub Pages in
a few minutes.


[installing-ruby]: https://www.ruby-lang.org/en/documentation/installation/
[jekyll-ghp-setup-doc]:   https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll
[ghp-publishing-source]: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
[ghp-troubleshooting]: https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/troubleshooting-jekyll-build-errors-for-github-pages-sites
[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-win]: https://jekyllrb.com/docs/installation/windows/
