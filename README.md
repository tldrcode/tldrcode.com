tldrcode.com
============
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/tldrcode/tldrcode.com?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Don't waste time with syntax; unleash the code!

[tldrcode.com](http://tldrcode.com)

## About
After learning the concepts behind programming, learning a new language comes
down to one thing: syntax. The goal of tl;dr{code} is to be a central hub for
programming syntax, allowing developers to focus more on the code itself.

Contributions
-------------
For those looking to contribute this section is for you. We need people like you to keep this site accurate and up-to-date. Below is a list of ways you can personally contribute to the project.

- Submit Issues to our Issue Tracker
- Correct Issues in our Issue Tracker
- Add a new Language
- Help us with some CSS (We're all pretty bad at it)
- Help document
- Send us pull requests
  - New features
  - Fix our very basic features (Search)

If you can do any of the above we will be eternally grateful.

## Running Locally with Vagrant
If you want to run a local version of the tl;dr{code} with vagrant, install
[vagrant](https://www.vagrantup.com/). Follow these instructions - 

    vagrant up
    vagrant ssh
    cd /vagrant
    jekyll server --watch -P 8080 --force_polling

FAQ
---
Q. Why are the language files named `*.markdown` and only contain YAML?

A. They are `.markdown` files because Jekyll will not render a page from a `.yml` file. Jekyll does allow for rendering of a `.markdown` files into multiple pages. The key is that the Markdown files can contain a YAML front matter. We exploit this ability by only having a YAML front matter and nothing in markdown.

## Site Colors
- Dark Gray: #2a2a2a
- Pink: #de577b
- Mint: #3fa38d
- Off White: #edeff0
