---
# Course title, summary, and position.
#linktitle: Make a website using R and Github pages
#summary: Step 1: Learn how to create a website using the Blogdown package in R studio. 
#weight: 2

# Page metadata.
title: Serve website on github pages 
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
    name: 3. Serve site to github pages 
    weight: 4
---

## 1) Edit content on your webpage 
* Open your 'webpage' R project to continue editing content on your website.
* Re-generate the public folder with updated content: **blogdown::serve_site()**

## 2) Deploy your changes to the live website 
* Here, we are going to push the changes to the 'public' directory to our 'username.github.io' repository. This step has to be done in terminal, not R studio.
* In terminal, navigate to the public folder of the 'webpage' directory. \
**cd webpage/public**
* Add, commit and push your changes with the following lines of code: \
**git add . ** \
**git commit -m "my message here"** \
**git push origin master** \
* Check your live website updates at **username.github.io**

## 3) Track your content changes to the website repository 
* Here, we are  going to push the changes of the 'webpage' directory to the 'webpage' repository. I prefer to do this using R studio. 
* Exclude the 'public' folder from being tracked by adding this line to your .gitignore file: **public/**. 
*Make sure you commit & push the updated .gitignore file too.



