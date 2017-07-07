# Pop!_Docs

Minisite for Pop!_OS and related projects.

[Listing of all docs](/docs)

## Intentionally Minimalist.

This site relies on [recent updates to GitHub Pages](https://github.com/blog/2289-publishing-with-github-pages-now-as-easy-as-1-2-3)
or [the relevant Ruby Gems for local development](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#step-2-install-jekyll-using-bundler)
as well as the "v2" styling of [System76.com](https://system76.com).

## Notes

### File names

Docs are `.md` files in the `docs/` folder. Please dash-separate words in filenames `like-this.md`.

### Front Matter

Docs use [Front Matter](https://jekyllrb.com/docs/frontmatter/) to set some attributes. They'll fall back to something sane if omitted, but to prevent [duplicate titles](https://github.com/system76/pop-docs/issues/5), set the title at the top of the file:

```yaml
---
title: Foo
---
```

And then **don't** start the doc with a heading, as it will show up automatically. 
