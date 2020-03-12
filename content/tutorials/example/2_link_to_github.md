---
# Course title, summary, and position.
#linktitle: stuff Make a website using R and Github pages
#summary: Step 2: Learn how to link your website to github & github pages 
#weight: 3

# Page metadata.
title: Link your website to github
date: "2018-09-09T00:00:00Z"
lastmod: "2018-09-09T00:00:00Z"
draft: false  # Is this a draft? true/false
toc: true  # Show table of contents? true/false
type: docs  # Do not modify.

# Add menu entry to sidebar.

# - name: Declare this menu item as a parent with ID `name`.
# - weight: Position of link in menu.
menu:
  example:
    name: 2. Link your website to github
    weight: 3
---

Before we start, it's important to explain that there will be 2 separate github repositories for this website. This is because hugo (and many website platforms) separate editable content from your live website content ('public' folder). \
**1. webpage:** This repository will contain the editable contents of your website, which you already generated in step 1. \
**2. username.github.io:** This repository will be a submodule of the 'webpage' repository. It contains the 'public' folder of your website, and is used to generate your live website on github pages.  


## 1) Make a 'webpage' repository
* make a new repository on github, and call it 'webpage' or whatever you'd like to call your main website repo. Don't add anything to the repository yet! 
* Copy the 'clone' link for your new repository. 
* Open R studio and click File --> New Project. 
* Choose 'from version control' and 'Github' in the project options.
* Create your R project using the copied repository link. 
* Then copy the entire contents of your Hugo website into the new R project directory & close your R project. 

## 2) Make the 'username.github.io' repository and add it as a submodule. 
* Make a new repository on github called **username.github.io**. Github pages will automatically generate a webpage from any repository with this specific name, so unfortunately you cannot be creative here! 
* Open terminal and navigate to your webpage directory on your local machine. **cd webpage/**
* Delete your public repository. **rm -rf public**
* Now we are going to add our 'username.github.io' repository as a submodule of the 'webpage' repository. **submodule add -b master https://github.com/username/username.github.io.git public** 
Next time we serve the site, the 'username.github.io.git' repository will contain the contents of the 'public' directory. 

## 3) Set your website html address
* Open the **config.toml** file in the home directory of your webpage_hugo R project.
* Replace the baseURL https://example.com with your github page domain: **https://username.github.io**
* Save the changes to the config.toml file.


For additional information and trouble-shooting, see the related [Hugo documentation](https://gohugo.io/hosting-and-deployment/hosting-on-github/) for hosting websites on github pages.

