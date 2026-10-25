## Run the page locally using Jekyll

To run locally, follow instruction [here](https://jekyllrb.com/) to install Jekyll then run `jekyll serve` to see in `localhost:4000`. Here is a brief install guidelines.

```bash
sudo gem install jekyll
sudo gem install rouge
jekyll serve
```

## Editing the lab website

Below, we explain how to edit the lab webpage

### Add posts

It's very easy to add post. All the posts are located in `_posts` folder. It arrangement is based on
date. Each post can be written in markdown format. You just have to state headers before writing: `title`, `description` and `categories`. `description` will be shown when you share on social media like Facebook or twitter. See the following headers:

``` markdown
---
title: Summer School in Computational Sensory-Motor Neuroscience (CoSMo)
description: all links to CoSMo summer school in computational neuroscience materials
categories: scientists
---
```

We have 4 categories: `scientists`, `students`, `discussion`, `blog` you can choose and this will be rendered to different location.

### How to add posts

- **Directly edit on Github**, you can simply go to `_posts` and click `New file` then put some markdown file e.g. `2016-02-03-post-name.md` and start writing blog post. Github also allows you to preview it so it's nice for people who don't want to clone the repo. 

- **Clone the repository**, kind of the same as directly add post on Github. You just have to clone the repository. Then add new post file, commit and push to the repo.

The changes will take approximately half a minute to render. You can see the new posts or changes on [kordinglab.com](http://kordinglab.github.io/)!

### Add yourself

You can add yourself to the page in `_people` folder just create file name `<firstname>_<lastname>.md` in the folder. We require few line of header before you start writing your own page. See the following for the header

``` markdown
---
name: Eva Dyer
position: postdoc
avatar: eva.jpg
twitter:
joined: 2014
---
```

If you don't have information, just leave it blank. The avatar will bring photo from `images/people` folder and display it on people page. 
For lab position, you can choose position from 4 classes including `postdoc`, `gradstudent`, `visiting`, `others` (so called Honorary members). Position will put you into section that you choose.

### Add new publications

The publications page is generated from `documents/references.bib` by `js/publications.js`.
Add your BibTeX entry to that file and it will appear at `/publication`. The page itself
lives in `pages/publications.md`.

### Add news

News on the front page is the list inside `index.html`. Add a line at the top of that list.

### Where things live

| What | Where |
| :--- | :--- |
| Site pages (publications, people, research, ...) | `pages/` |
| Blog posts | `_posts/` |
| Person profiles | `_people/` |
| Course pages | `_teaching/` |
| Layouts and the navbar | `_layouts/`, `_includes/` |
| Stylesheet | `css/style.scss` |
| Bibliography, CVs, PDFs | `documents/` |
| Helper scripts | `scripts/` |

Pages in `pages/` each declare their own `permalink`, so the folder never appears in a URL.
