tldrcode.com
============

Don't waste time with syntax; unleash the code!

## About
After learning the concepts behind programming, learning a new language comes
down to one thing: syntax. The goal of tl;dr{code} is to be a central hub for
programming syntax, allowing developers to focus more on the code itself.

## Get Involved
We need people like you to keep this site accurate and up-to-date. If you would
like to contribute to the project by adding new languages or correcting existing
ones, please send us a pull request on github. Program long and prosper!

## Running Locally with Vagrant
If you want to run a local version of the tl;dr{code} with vagrant, install
[vagrant](https://www.vagrantup.com/). Follow these instructions - 

    vagrant up
    vagrant ssh
    cd /vagrant
    jekyll server --watch -P 8080 --force_polling

Contributions
-------------
For those looking to contribute this section is for you. Below is a list of ways
you can personally contribute to the project.

- Submit Issues to our Issue Tracker
- Correct Issues in our Issue Tracker
- Add a new Language
- Help use with some CSS (We're all pretty bad at it)
- Help document
- Send us pull requests
  - New features
  - fix our very basic features (Search)

If you can do any of the above we will be eternally grateful.

FAQ
---
Q. Why are the language files named `*.markdown` and only contain YAML?
A. They are `.markdown` files because Jekyll will not render a page from a `.yml` file. Jekyll does allow for rendering of a `.markdown` files into multiple pages. The key is that the Markdown files can contain a YAML front matter. We exploit this ability by only having a YAML front matter and nothing in markdown.
