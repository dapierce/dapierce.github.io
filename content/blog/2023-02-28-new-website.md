---
title: A new website, made in the web
description: How I built my new website
date: 2023-02-28
tags:
  - web development
draft: true
---

The modern web has mostly become 3-5 websites the past couple decades. They are powerful websites that most who use the internet frequent, and arguably the easiest way for someone to make a name for themselves.

But there will always be a place for your own unique presence that cannot be controlled by someone else. A place that you can really make your own. And in 2023, there are enough free tools online that you can entirely build yourself a new website, host it and maintain it completely through a web browser.

My website is largely built and maintained *within* the browser, and although I keep a copy of the repository on my own hard drive, ultimately most of my time spent on it has been remotely. I'm going to walk through how I do it.

## 11ty to GitHub

I started with a static site generator, [11ty](https://www.11ty.dev/), and used their [starter blog](https://github.com/11ty/eleventy-base-blog), which allows you to get up and running with a simple blog website.

I made my own repository using the starter as a template, and from there I began tinkering with the code and layouts using GitHub's Codespaces. Basically, it opens VS Code on your browser and you can just start working on the site right there. The terminal is fully functional, and so you can just run

```bash
npx @11ty/eleventy --serve
```

and GitHub will serve up a live updated version of your site, and give you a link to view it as you work. Move that tab over to its own window on the other side of your desktop and you can work and watch the site change.

## GitHub to Netlify

Once I had a decent looking site made on Codespaces, I commited my work to my personal repository, and then went to [Netlify](https://www.netlify.com/) for free web hosting. I don't get a ton of traffic, so the free plan works great for my blog. On your Netlify account, you can log in with GitHub and just directly deploy your website's repository. Since I have a domain name, I set that up on the **Domain Management** settings in Netlify, and within a day I had my new website on my address.

If you don't need a fancy domain name, then you can simply host your website using GitHub for free by naming your website repository **\<username\>.github.io**. The website will then become public at **http://\<username\>.github.io** and that can be your new, free home on the internet.