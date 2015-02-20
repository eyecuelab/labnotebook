# labnotebook

**labnotebook** is the repository for EyeCue Lab's blog.

You can view it on the web at [blog.eyecuelab.com](http://blog.eyecuelab.com).

## Colophon

The EyeCue Lab Notebook runs on [Jekyll](http://jekyllrb.com/). 

The template is bootstrapped from the [Lanyon](http://github.com/poole/lanyon) theme made for [Poole](http://github.com/poole/poole) by [@mdo](http://twitter.com/mdo).

The site is hosted with [GitHub Pages](https://pages.github.com/).

Comments are powered by [Disqus](https://disqus.com).

## How To

Below are instructions for our staff to perform common tasks.

### Write a new post

Open your favorite plaintext editor and just start writing.

Copy this block to the top of the post:


```
---
layout: post
title: Hello world!
comments: true
author: rick
author2: nicci
author3: paul
p-category: Product & Design
---

(your post content goes here)

```

This block is called the [Front Matter](http://jekyllrb.com/docs/frontmatter/).

Replace the `title` and `author` attributes with the post title and author name. Posts can have up to three authors. If you have fewer authors, you can remove the `author2` and `author3` lines.

Replace the `p-category` attribute with the post category. This text is displayed above each post.

Type your post below the Front Matter block. Follow the Markdown [syntax guide](https://help.github.com/articles/markdown-basics/).

Save the post with this naming convention:

`YYYY-MM-DD-hello-world.md`

- Replace `YYYY-MM-DD` with the post date.
- Replace `hello-world` with a web-friendly title for your post. This will become part of the web address once your post is published.

## Publish a post to the web

Use Git to clone the `eyecuelab/labnotebook` repository and switch to the `gh-pages` branch:


```
cd ~/Code
git clone https://github.com/eyecuelab/labnotebook.git
cd labnotebook
git branch gh-pages
```

Copy your post into the `_posts/` directory.

Add and commit your new post to the Git repository.

```
git add _posts/2015-02-09-hello-world.md
git commit -m "add a new post"
```

Use Git to push your changes to the `gh-pages` branch of `eyecuelab/labnotebook`:


```
git pull --rebase origin gh-pages
git push origin gh-pages
```

### Include images in your Post

You have an image called `eyecue-logo.png`.

First, copy `eyecue-logo.png` into the `/public/images/posts/` directory.

Next, use [Markdown's image syntax](http://daringfireball.net/projects/markdown/syntax#img) to include the image in your post:

```
![EyeCue Logo]({{ site.postimage }}eyecue-logo.png)
```

Don't forget to add and commit the image to the repository before you push to the `gh-pages` branch:

```
git add public/images/posts/eyecue-logo.png
git add _posts/2015-02-09-your-post-here.md
git commit -m "add a new post"
git pull --rebase origin gh-pages
git push origin gh-pages
```

### Add a new author to the system

Add the author's avatar image to `/public/images/team`.

Add the user's information to the `_data/authors.yml` file in this format:

```
andrew:
    name: Andrew Westling
    email: hello@eyecuelab.com
    twitter: eyecuelab
    avatar: andrew.gif
```

Use Git to commit, rebase, and push your changes to the `gh-pages` branch.

## Meta

EyeCue Lab  
[eyecuelab.com](http://eyecuelab.com)  
[@eyecuelab](http://twitter.com/eyecuelab)
