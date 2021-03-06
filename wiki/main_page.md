---
title: "Welcome!"
layout: 'git-wiki-bs-united' 
redirect_from: "/"
---

## PolitWiki? Polyblog?

Welcome to you, the cruiser of the endless abyss of Internet! If perchance you stumbled upon this little inchoate site, consider yourself ... Who cares? Seriously, though, this site was born as a result of my several months-long journey of finding a perfect set up (for me) to have notes in the Wiki format AND still have an access to them online. I will be working on moving my Wiki notes here. 

## What is Politwiki/Polyblog?

This site, as I envision it at the moment, will be an amalgamation of several things:

1. A Wiki, with the collaboration option conditioned upon [Github](https://github.io) registration (to add files and use Prose.io). In the foreseeable future, though, it will be just the remote clone of my personal Wiki notes (synced with `Git`).

2. A blog where I will try to document the Wiki management or post about a variety of topics I am personally interested in: 
  `Unix/Linux`, `Academia`, `Languages`, `Scripting for social-scientists (non IT specialists)`. 

I also have a [repository](https://github.com/gizehgrun/TIL) on Github with my TIL snippets - short notes on technical topics in **"Today I learned"** style (post on TIL and scripts I use upcoming). 

## Credits

This wiki was made possible with [Github Pages](https://pages.github.com/) and their wonderful static site assistant - [Jekyll](https://jekyllrb.com/). Thanks to the [Git](https://git-scm.com/) version-control system, I can control the website from the comfort of my `Linux` OS. Additionally, the guys from [git-wiki-theme](http://drassil.github.io/git-wiki/) saved me, probably, a year of learning about Jekyll and provided this template. 

## To-dos

- [ ] Learn tagging with Liquid
- [ ] Justifying text (tinker with templates?)
- [ ] Git pulling/pushing automatize (scripts?)
- [ ] Change the repository name shown at top to something else

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
