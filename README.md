This is the repository for my personal website shashankdholakia.github.io

## How to update the website:

I have modified the Astral theme from HTML5up to use jekyll. This means that I can add content to the website in the form of markdown documents without formatting, and the code in /_layouts/ will format the document into a post.

There are two locations where I can currently add/update a post.

- \_navpages
- \_portfolio

### Nav pages
_navpages contains all the markdown documents for the navigation pages, excluding the home directory (currently Work, About Me, and Contact Me). 

To add a new page that shows up in the nav bar, you will first have to go to /_layouts/default.html and change the portion under the <nav> tag to reflect the order and links for the new nav bar. A new markdown document can then be created in the \_navpages folder.
The YML header should contain three items: the title of the page (e.g About Me), the layout (should be default but doesn't matter since these posts aren't being published), and idname, which should correspond to the name of the link in the navbar. For instance: 

```
---
title: About Me
layout: default
idname: aboutme
---
```

### Portfolio posts

These posts should 