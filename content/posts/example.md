+++ 
date = 2026-01-23T18:10:09+08:00
title = "How to build your own blog website"
description = ""
slug = ""
authors = []
tags = []
categories = ["计算机科学"]
externalLink = ""
series = []
+++

This serves as an example post on this site. 

## Setting up locally

See [here](http://www.wzhengchang.cn/posts/hugo-%E9%83%A8%E7%BD%B2%E6%95%99%E7%A8%8B/) from tag 1 to 6.

## Github actions

You should create a github repository for it if you want to use github pages for this website. Create the file `.github/workflow/build.yml` as follows:
```yml
name: Publish site (Pages artifact)

on:
  push:
    branches:
     - main

permissions:
  contents: read
  pages: write
  id-token: write
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0
          submodules: 'recursive'
      - uses: peaceiris/actions-hugo@v3
        with:
          hugo-version: 'latest'
          extended: true
      - run: hugo --minify -D
      - uses: actions/upload-pages-artifact@v4
        with:
          path: ./public
  deploy:
    needs: build
    runs-on: ubuntu-latest
    environment: 
      name: github-pages
    steps:
      - uses: actions/deploy-pages@v4
```
Remember to navigate to `Settings/Pages` tab in your github repository, enable github pages, and set Github Actions as the source.

## Configurations
You should know your configurations by reading the documentations of your theme.

## Possible bugs
- Some of the parameters in the header of your markdown files should match your taxonomies in your configuration file AND those listed in your theme. For example, if you have 
  ```toml
  [[taxonomies]]
  tag = 'ABC'
  ```
  in your `hugo.toml` or something similar, then the header will have to say `ABC = ["abc"]` to recognize `"abc"` as a hugo tag, and your theme should have an `ABC.html` in some version.
- You may want to care about the font issues of different languages, e.g. create `assets/css/custom.css` as following:
  ```css
  article, footer, p, h1, h2, h3, h4, h5, li, a {
      font-family: "Noto Sans SC";
  }
  ```
  and add the following lines into `hugo.toml`:
  ```toml
  [params]
      customCSS = ["css/custom.css"]
  ```
  As a further example, to prevent goldmark converting characters to their Chinese forms (which happens for e.g. `'` because it is escaped in html and then converted back), add these lines:
  ```toml
  [markup.goldmark.extensions]
  typographer = false
  ```
- Katex has its own bugs: a small example would be `$S_f={f^n}_1$ C $A_\bullet$`, which for god-knows-why is interpreted to have an italic `$C$` in the middle. You should add these lines to your configuration:
  ```toml
  [markup.goldmark.extensions.passthrough]
  enable = true
  delimiters = { block = [['\[', '\]'], ['$$', '$$']], inline = [['\(', '\)'], ['$', '$']]}
  ```
  But it still cannot recognize block equations that start and end with `$$`, and you should use `\\[\\]` for them. I don't know if there is a workaround.
- Remember to check which paths (relative of absolute) your configurations use; e.g. in my theme the `customCSS` parameter starts from the `assets/` folder.