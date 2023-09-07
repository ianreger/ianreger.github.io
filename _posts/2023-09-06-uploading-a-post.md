---
layout: post
title: "Creating a post"
date: 2023-09-06 22:30:00 -0500
categories: [jekyll,github,markdown]
tags: [jekyll,github,git,markdown,ci,cd,actions,blog,documentation] #all tags MUST be lowercase
---

# Creating a new post

### Get the latest repository

Whether you are pulling or cloning the repo, make sure you have the newest version. 

ex: git clone https://github.com/ianreger/ianreger.github.io

### Create a post file

Create a .md file in the `/_post` folder using the same conventions shown on previous posts. The post must have the file name of `YYYY-MM-DD-title.md`.

### Add then push the files to GitHub

Once the files are saved and ready to upload to your site, in your terminal run the following commands:

```
git add .
git commit -m "feat(post): Title"
git push
```

Your files should now show up on your repository, and the GitHub Actions will automatically build and upload the new pages.  