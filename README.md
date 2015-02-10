# labnotebook

The official weblog for EyeCue Lab

# Colophon

The EyeCue Lab Notebook runs on [Jekyll](http://jekyllrb.com/). It is bootstrapped from the [Lanyon](http://github.com/poole/lanyon) template made by [@mdo](http://twitter.com/mdo).

=======
# How To

## Make a new post

Make a new text file whose file name matches the following format:

`/_posts/YYYY-MM-DD-hello-world.md`

- replace `YYYY-MM-DD` with the post date
- replace `hello-world` with the URL slug you want for your post (*example: http://blog.eyecuelab.com/2015/02/09/**hello-world**.html*)

Copy the template below into your new file. 

```
---
layout: post
title: Hello world!
author: rick
author2: nicci
author3: paul
---

Hello! This is a sample post for the EyeCue Lab Notebook. 

```

Replace the `title:` and `author:` attributes in the top section with the post title and author names. Posts can have up to three authors. If you have fewer authors, you can remove the `author2` and `author3` lines.

Type the content of your post below the title/author section. Use [Markdown syntax](https://help.github.com/articles/markdown-basics/) to format your post.

Save your file into the `_posts/` directory. Add and commit your changes to the git repository, then push to `eyecuelab/labnotebook`.

## Add a new user to the system

- Upload the user's avatar image to `/public/images/team`. Make the image 170x170 px and grayscale
- Add the user's information to the `_data/authors.yml` file

# Development Log

## To Do

- **GitHub Pages Configuration**
  - need an `eyecuelab/eyecuelab.github.io` repo with CNAME `eyecuelab.com` 
  - need an `eyecuelab/labnotes` repo with CNAME `blog.eyecuelab.com`
  - need to set up a CNAME record for `blog.eyecuelab.com` that points to `eyecuelab.github.io.`
- **Comment System**
  - set up eyecuelab Disqus account
  - integrate: [link](https://help.disqus.com/customer/portal/articles/472138-jekyll-installation-instructions)
- **EyeCue Lab Logos/Staff Images**
  - get EyeCue Lab logos(+inverted) for sidebar toggle button
- **Assets**
  - implement an asset pipeline for fonts and static content

