---
layout: post
title:  "Jekyll Blog"
date:   2021-05-18 08:00:00 +0100
categories: dev
tags: [jekyll, github, blogging]
---
{% comment %}
=======================
The purpose of this snippet is to list all the tags you have in your site.
=======================
{% endcomment %}
{% for tag in page.tags %}
	<a href="#{{ tag | slugify }}"> {{ tag }} </a>
{% endfor %}

For while now I played with the idea of publishing a personnal blog to help me keep track of the many things I experiment with. It comes with the added benefit of providing some information on different subjects that might be of help to someone, someday.

There are many different blogging tools available for pretty much every programming language that I know of. My first choice was to go with a full-fledged MVC framework like Laravel for PHP or Django for Python. As I’m pretty lazy and know myself well enough, I didn’t want to spend another year goofing around with the tool before starting to write things down. The next best solution was to create a quick’n dirty bare-bone blogging tool with Express or something similar. That’s when I stumbled upon Jekyll which offered an interesting concept : a serverless blogging tool which renders static content.

Unlike dynamic content blog solutions, Jekyll requires the author to create and build entries locally before publishing them. This means there is no admin dashboard accessible through the web to edit or create new posts. But because posts consist of simple markdown files, a basic text editor is all that is needed to create them. As for building & publishing, GitHub pages integrates Jekyll natively and will rebuild & publish the entire site on each commmit from the blog repository. And since GitHub now allows editing repository files directly from the browser, we don’t need a local setup anymore after the initial repository creation.

If the need for previewing the posts comes up, a simple solution is to use GitPod which lets users open a virtual VS Code based workspace in the browser. There we can start a live server and watch files to preview live changes. GitPod currently offers a free plan with 50 hours of worksapce use per month for public repositories.