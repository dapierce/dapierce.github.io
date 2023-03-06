---
title: A new website, made in the web
description: How I built my new website
date: 2023-03-01
tags:
  - web development
---

The modern web has mostly become 3-5 websites the past couple decades. They are powerful websites that most who use the internet frequent, and arguably the easiest way for someone to make a name for themselves.

But there will always be a place for your own unique presence that cannot be controlled by someone else. A place that you can really make your own. And in 2023, there are enough free tools online that you can entirely build yourself a new website, host it and maintain it completely through a web browser.

My website is largely built and maintained *within* the browser, and although I keep a copy of the repository on my own hard drive, ultimately most of my time spent on it has been remotely. I'm going to walk through how I do it.

## 11ty to GitHub

I started with a static site generator, **[11ty](https://www.11ty.dev/)**, and used their [starter blog](https://github.com/11ty/eleventy-base-blog), which allows you to get up and running with a simple blog website.

I made my own repository on **GitHub** using the starter as a template, and from there I began tinkering with the code and layouts using GitHub's Codespaces. Basically, it opens VS Code on your browser and you can just start working on the site right there. The terminal is fully functional, and so you can just run

```bash
npx @11ty/eleventy --serve
```

and GitHub will serve up a live updated version of your site, and give you a link to view it as you work. Move that tab over to its own window on the other side of your desktop and you can work and watch the site change.

*Note that you only get 60 hours of Codespaces time on the free plan*, so if you're done designing your site and don't need a live preview anymore, you can use [https://github.dev/](https://github.dev/) to make changes to your codebase and make new posts.

## GitHub to Netlify

Once I had a decent looking site made on Codespaces, I commited my work to my personal repository, and then went to **[Netlify](https://www.netlify.com/)** for free web hosting. I don't get a ton of traffic, so the free plan works great for my blog. On your Netlify account, you can log in with GitHub and just directly deploy your website's repository. Since I have a domain name, I set that up on the **Domain Management** settings in Netlify, and within a day I had my new website on my address.

## GitHub Pages

While Netlify does a great job of just building and deploying a site with no fuss, maybe you don't want another site to log into. Instead, you can host your website using GitHub for free by naming your website repository **\<username\>.github.io** and tinker with [**GitHub Actions**](https://docs.github.com/en/actions). After some effort setting up your workflow, your website will become public at **http://\<username\>.github.io** and that can be your new, free home on the internet.

This is the config I used to build my 11ty site using **11ty-dockerless-build**, and then deploy on GitHub Pages using **actions-gh-pages**. The `github_token` part at the end can be a bit tricky and will require some setup in your Github account and repository settings. [You can get more info about the deploy step here](https://github.com/peaceiris/actions-gh-pages).

```yml
name: Eleventy Build
on: [push]

jobs:
  build_deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@master
      - name: Build
        uses: extrawitz/11ty-dockerless-build@v1
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          publish_dir: _site
          publish_branch: gh-pages
          github_token: (your auth goes here)
```

## Alternatives

**[GitLab](https://gitlab.com/)** will work similarly to GitHub, as it can also run VS Code in browser, and they also have a similar coding environment, GitPod that allows live updating just like Codespaces. Additionally, GitLab Pages can deploy and host your site with an arguably easier setup than GitHub.

I've also seen **[Glitch](https://glitch.com/)** used not only to code and build things with a more accessible interface, but also to deploy and host websites. It looks very easy to set up and use, as it has everything built-in.

## Final thoughts

Social media as a whole isn't going anywhere. But individual sites gain and lose prominence, and they are constantly changing their Terms of Service and rules. It's important to have your own place on the internet with the words, images, videos and other things that you care about, that a massive compnay cannot dictate or remove on the whim of its shareholders.

While we are using services to set this website up that are controlled by companies, ultimately what we're making is a git repository that you can maintain copies of on your own hard drive and in multiple clouds.

This is your site, your data, and if you need to take it somewhere else because Netlify or GitHub go away, it'll be pretty easy to do so.
