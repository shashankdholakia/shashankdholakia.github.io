This is the repository for my personal website [shashankdholakia.github.io](https://shashankdholakia.github.io/)

## How to update the website:


This documentation is mostly so I can remember how to update my own website after some time.

I have modified the Astral theme from HTML5up to use jekyll. This means that I can add content to the website in the form of markdown documents without formatting, and the code in /_layouts/ will format the document into a post in html.

### When making and posting any changes to the website:

Jekyll has a way to locally "compile" changes to view how the site looks before updating the website itself. To view the site locally, cd to the directory of the repo and type in a terminal:

```
bundle exec jekyll serve --watch
```

Then, go to http://localhost:4000/ in any browser. When ready to update the website, push the changes to github. 

There are two locations where I can currently add/update a post.

- \\_navpages
- \\_portfolio

### Nav pages
_navpages contains all the markdown documents for the navigation pages, excluding the home directory (currently Work, About Me, and Contact Me). 

To add a new page that shows up in the nav bar, you will first have to go to \layouts\default.html and change the portion under the <nav> tag to reflect the order and links for the new nav bar. A new markdown document can then be created in the \\_navpages folder.
The YML header should contain three items: the title of the page (e.g About Me), the layout (should be default but doesn't matter since these posts aren't being published), and idname, which should correspond to the name of the link in the navbar. For instance: 

```
---
title: About Me
layout: default
idname: aboutme
---
```

### Portfolio posts

These posts show up on the front page of the website, so they should look nice! There are a few steps needed to make a portfolio post:

- putting an image in the images folder for the thumbnail
- creating a markdown document in \\_portfolio to create a post and text on the thumbnail

The image should be 4:3 aspect ratio and should not be over 1000 pixels so it can load faster. Gifs may work although I haven't yet tried.

The front matter in the markdown document sets the thumbnail on the page of the website. For instance: 

```
title: "Gravity Darkening"
weight: 3
subtitle: "Fast transit models for <br> rapidly rotating stars"
image: "images/gdark.png"
layout: page
```

The quotes around the title and subtitle are important to ensure that you can use html formatting, like the line break <br>. The weight tag sets how far up the thumbnail appears on the website--a higher number means the thumbnail will be more recent (so the oldest post should be set to 1). The image tag should be the path to the thumbnail image, which ought to be in the images folder.

### Blog:

As of Dec 2021, I have updated the website to include a blog. The blog is quite rudimentary so far and might change. These are the steps to creating a new blog post:

1. Create a file called YEAR-MONTH-DAY-title.markdown in the _posts directory. The yml front matter (top lines in the doc) should read:
  ```
  ---
layout: post
title:  ENTER TITLE HERE
date:   YEAR-MONTH-DAY HH:MM:SS -0800
categories: <any category tags>
---
  ```
2. Write the post in the same way as a portfolio page. The post will show up under the 'blog' tab of the website. By default, the excerpt will be the first paragraph of the post. To customize this, add this to the front matter of the markdown file for the post:

```
  excerpt_separator: <!--more-->
```
then, use <!--more--> within the post to deliniate where the excerpt should end.


### Adding images to posts and pages:
The standard way of adding an image is to write in the markdown file:
```
  <p align="center"><img src="{{ site.baseurl }}path/to/image.jpg" width="70%"/></p>
```
The alignment and width can change. In general, images should be within the images folder in the root directory, and for posts with multiple images a subfolder containing all images for that post is recommended. In addition, images should be resized down to a few megapixels in Photoshop or similar to speed the website loading.

### Credit:

Based on the stellar theme:

 https://github.com/hubertchoo/stellar-jekyll-theme

which is originally built on **Astral by HTML5 UP**

