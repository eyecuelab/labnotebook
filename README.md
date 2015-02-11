# labnotebook

The official weblog for EyeCue Lab

## Colophon

The EyeCue Lab Notebook runs on [Jekyll](http://jekyllrb.com/). 

The template is bootstrapped from the [Lanyon](http://github.com/poole/lanyon) theme made for [Poole](http://github.com/poole/poole) by [@mdo](http://twitter.com/mdo).

It is hosted with [GitHub Pages](https://pages.github.com/).


## How To

### Make a new post

First, clone the `eyecuelab/labnotebook` repository and switch to the `gh-pages` branch:

```
cd ~/Code
git clone https://github.com/eyecuelab/labnotebook.git
cd labnotebook
git branch gh-pages
```

Next, make a new text file whose file name matches the following format:

`/_posts/YYYY-MM-DD-hello-world.md`

- replace `YYYY-MM-DD` with the post date
- replace `hello-world` with the URL slug you want for your post (*example: ht<span>tp:</span>//blog.eyecuelab.com/2015/02/09/**hello-world**.html*)

Copy the template below into your new file. 

```
---
layout: post
title: Hello world!
author: rick
author2: nicci
author3: paul
p-category: Product & Design
---

Hello! This is a sample post for the EyeCue Lab Notebook. 

```

Replace the `title:` and `author:` attributes in the top section with the post title and author name. Posts can have up to three authors. If you have fewer authors, you can remove the `author2` and `author3` lines.

Replace the `p-category:` attribute with the post category. This text is displayed above each post.

Type the content of your post below the title/author section. Use [Markdown syntax](https://help.github.com/articles/markdown-basics/) to format your post.

Save your file into the `_posts/` directory. 

Add and commit your changes to the git repository, then push to the `gh-pages` branch of `eyecuelab/labnotebook`:

```
git add _posts/2015-02-09-hello-world.md
git commit -m "add a new post"
git pull --rebase origin gh-pages
git push origin gh-pages
```

### Include images in your Post

Here's an example: your image's file name is `kitten.jpg`.

First, copy `kitten.jpg` into the `/public/images/posts/` directory.

Next, copy this syntax into the post where you want to include the image:

```
![An Adorable Kitten]({{ site.baseurl }}public/images/posts/kitten.jpg)
```

Don't forget to add and commit the image to the repository before you push to the `gh-pages` branch:

```
git add public/images/posts/kitten.jpg
git add _posts/2015-02-09-your-post-here.md
git commit -m "add a new post"
git pull --rebase origin gh-pages
git push origin gh-pages
```

### Add a new user to the system

- Upload the user's avatar image to `/public/images/team`. Make the image 170x170 px and grayscale
- Add the user's information to the `_data/authors.yml` file

## Development Log

### To Do

- **Comment System**
  - set up eyecuelab Disqus account
  - integrate: [link](https://help.disqus.com/customer/portal/articles/472138-jekyll-installation-instructions)

