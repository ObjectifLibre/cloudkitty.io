---
layout: post
title: Introducing cloudkitty.io
tags: [Blog, Annoucement]
thumbnail: /assets/introducing-cloudkittyio/thumbnail.png
---



<p align="center">
    <img src="assets/introducing-cloudkittyio/cloudkitty-openstack-community.png"/>
</p>

The CloudKitty Community is proud to announce that **cloudkitty.io** is now
officially online! This website is meant to be a collaborative blog about
CloudKitty, **by and for the community**!

## What's to be found here ?

This site was built to collect user feedback and experiences around CloudKitty,
announce releases and features, make announcements...

This is the place where you should expect to find information about existing
cloudkitty deployments, how to try out new features, how to configure specific
use cases... Of course, **contributions are very welcome!**

## I'd like to post an article, how do I proceed ?

The whole website is hosted on
[GitHub](https://github.com/cloudkittyio/cloudkittyio.github.io) via GitHub
Pages. If you want to submit an article, submit a pull request, and we'll be
glad to review and merge it! 🙂

When submitting an article, the following points need to be taken into account:

- Of course, the article must be, at least partially, about CloudKitty.

- Posts are written in Markdown, see the [cheatsheet](/markdown-cheatsheet)
  for syntax.

- To be taken into account, your post must be placed in a file called
  ``yyyy-mm-dd-title.md`` inside of the ``_posts`` directory. The date is
  mandatory and must respect the specified format.

- Images are not mandatory, but they make posts look more welcoming. However,
  don't use too many, and **make sure they are free to use**.

- If there are any assets (images...) you'd like to include in your post,
  create a subdirectory in the ``assets`` directory at the root of the
  repository. The subdirectory must have the same name as the file containing
  your article, minus the date and the .md extension. For examples, the assets
  of this post can be found in ``/assets/introducing-cloudkittyio/``.

- Each article must include a header of the following form:
  {% highlight bash %}
  ---
  layout: post
  title: Your title
  tags: [A, List, Of, Tags]
  ---{% endhighlight %}

- The two most recent articles are displayed on the front page of the site. You
  can specify an optional thumbnail for your article in the header:
  ``thumbnail: /assets/myarticle/thumbnail.png``. If you don't specify a
  thumbnail, the default one (it can be found in
  ``assets/defaults/thumbnail.png``) will be used.

- If you want to know how your article looks, you can use Docker for local
  development:
  {% highlight bash %}
  # At the root of the repository
  docker build -t cloudkittyio-jekyll .

  # After running this command, point your browser to http://127.0.0.1:3000
  docker run --rm -p 3000:3000 -v "$PWD":/srv/jekyll cloudkittyio-jekyll
  {% endhighlight %}


That's all for today, we hope to see you publishing blog posts soon!