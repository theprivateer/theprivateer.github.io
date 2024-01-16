---
layout: post
date: 2024-01-10
title: Installing Jekyll on macOS Sonoma
render_with_liquid: false
---
I use a Mac, and whilst macOS ships with a copy of Ruby I immediately ran into issues trying to install Jekyll (mostly around Ruby being out of date). Typically I would just reach for [Homebrew](https://brew.sh) and install the latest version of Ruby with something like `brew install ruby` but in this instance that doesn’t work as well as you might think.

Instead you need to use a Ruby-specific version manager to install a newer version. In this instance we’ll use [`chruby`](https://github.com/postmodern/chruby), but others are available.

## Install a newer version of Ruby

Install `chruby` and `ruby-install` with Homebrew (if you don’t have Homebrew installed yet, follow the instructions [here](https://brew.sh/#install)):

```bash
brew install chruby ruby-install xz
```

Now you can install the latest stable version of Ruby supported by Jekyll (3.1.3 at time of writing):

```bash
ruby-install ruby 3.1.3
```

Finally, configure your shell to automatically use `chruby`:

```bash
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc
```

I use Zsh for my shell - if you use a different shell you will need to adjust these last few commands. For example if you’re using Bash, replace `.zshrc` with `.bash_profile`.

Either relaunch your terminal session or type `source ~/.zshrc` to reload the configuration.

You can confirm you are now using the version of Ruby installed above by typing the following:

```bash
ruby -v
```

## Install Jekyll

Now that you’re on the latest (supported) version of Ruby you can go ahead and install the latest Jekyll gem:

```bash
gem install jekyll
```

From here you can spin up a new site with `jekyll new my-awesome-site`.
