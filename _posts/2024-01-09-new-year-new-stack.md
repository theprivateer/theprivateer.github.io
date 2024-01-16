---
layout: post
date: 2024-01-09
title: New Year, New Stack
---
It’s time to have another crack at maintaining this blog - which means it’s as good a time as any to give it a bit of a makeover.

I have two main criteria for choosing a blogging platform:

1. Cheap (or free) to host
2. Easy to update and maintain
3. I own my data

For the past couple of years this blog has been powered by [Jigsaw](https://jigsaw.tighten.com), a PHP static site generator, and hosted by [Netlify](https://www.netlify.com). This setup fits both of my criteria - I am able to use Netlify’s free tier to host the site, and adding a new post is as easy as adding a new Markdown file and pushing the change to Github.

However recently I’ve found things slightly more cumbersome - I’ve been having compilation issues with my SCSS files due to [Laravel Mix](https://laravel-mix.com) (a wrapper for Webpack), and Jigsaw isn’t a particularly popular or widely used application, so doesn’t have an especicially active ecosystem (although the main reason I originally chose it was because it is based on Laravel, the PHP framework I use every day).

Going all-in with Jigsaw because it is a PHP-based site generator based on Laravel was probably a little myopic. I largely disregarded other platforms because I am primarily a PHP developer - but there are so many other (better?) options out there.

So with that I have decided to give [Jekyll](https://jekyllrb.com) a go. To keep things as simple as possible, I’m moving away from Netlify and hosting the site natively on [Github Pages](https://pages.github.com) (also free). My publishing flow is still the same - adding Markdown files to my repository and pushing (or adding them directly in Github’s web UI). I’m starting off with a pared down version of Jekyll’s default Minima theme, and will start iterating on the design over the next few weeks.

_Sidenote: whilst I’m not expecting to need to do any Ruby programming - Jekyll’s vibrant ecosystem of plugins should handle anything I might need - I spent nearly a year programming exclusively in Ruby back when Rails was at version 2._
