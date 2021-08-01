---
layout: default
title: Contributing
nav_order: 10000
---

<style>
.main-content .task-list-item {
  /* Code samples were getting messed up because of the flexbox design. Because we are using a remote theme, there is little we can do about this. */
  display:block;
}
</style>

# Contributing
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## GitHub procedure

Visit our GitHub repository [jackcrane/toa-docs](https://github.com/jackcrane/toa-docs) and poke around the files. If you find something that you want to change or add, clone and open a pull request. 

If you are thinking of doing a small change (i.e. fixing a spelling error or a syntax issue) simply open a pull request. If you are thinking of doing a large change, submit an issue or, if you have some content written, open a Draft Pull Request before you waste too much time. 

If you want to contribute but don't know where to start, check out the [issues](https://github.com/jackcrane/toa-docs/issues) or the todo list below.

Before opening/submitting a pull request, you must do each of the following:
- [ ] Check for spelling and grammatical errors
- [ ] Check for your TOA api key in code samples and replace it with `:toa-api-key`
- [ ] Check for your TOA application origin in code samples and replace it with `:toa-application-origin`
- [ ] Test all code samples to verify they are running and functional
- [ ] Test the page at a handful of screen sizes just to make sure nothing weird occurs. If it does, you can choose to fix it or open an issue and someone else will tackle it.
- [ ] Rebuild search database by running `bundle exec just-the-docs rake search:init` in the root directory.
- [ ] Add yourself to the contributors list at the bottom of this page.
- [ ] In your PR comment, write what you changed and what resources you used to write your content.

We are very open and accepting to ideas for new pages and sections. If you are not sure, open an issue and we will discuss there.

## Building from source

### Prerequisites

#### Ruby

[Visit the official installation documentation](https://www.ruby-lang.org/en/documentation/installation/)

(You will also need to install Gem if it is not already installed by Ruby.)

#### Jekyll
[Jekyll](https://jekyllrb.com/docs/) is a powerful static site generator that parses markdown into HTML that can be hosted on a static platform (like our provider, GitHub pagse).

```bash
gem install jekyll bundler
```

### Usage

1. Clone the source code from [jackcrane/toa-docs](https://github.com/jackcrane/toa-docs) using git or github desktop.
```bash
git clone https://github.com/jackcrane/toa-docs.git
```

2. Navigate to the directory
```bash
cd toa-docs
```

3. Tell Jekyll to watch for changes, and compile on save (usually compilation takes about 3 seconds)
```
bundle exec jekyll serve
```

## Using the framework

We are using [just-the-docs](https://github.com/pmarsceill/just-the-docs), a documentation theme for Jekyll. Documentation on how to use it's search, layout, design, and scripting features are on their [documentation page](https://pmarsceill.github.io/just-the-docs/)

## Contributors

[@jackcrane](https://github.com/jackcrane)