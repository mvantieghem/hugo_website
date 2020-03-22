---
# Course title, summary, and position.
#linktitle: Make a website using R and Github pages
#summary: Step 1: Learn how to create a website using the Blogdown package in R studio. 
#weight: 2

# Page metadata.
title: Build website 
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
    name: 1. Build website with Blogdown and Hugo in R 
    weight: 2
---

## 1) Choose a theme for your website 
* Hugo has a wide array of website themes, which can be found [here](https://themes.gohugo.io/).
* Themes dictate both the aethetics and the format of a website.
* Choose wisely. Once you start with a certain theme, it's hard to switch themes later.

## 2) Use blogdown to generate a website template
* Once you've chosen a theme, navigate to the owner's github repository (https://github.com/user/repo). We're going to build our website using the example template for that theme.
* in R studio, install the blogdown package. \
**install.packages('blogdown')**
* Make a new R project. \
**File --> New Project**
* Generate a website from the theme template in your R Project.\
**blogdown::generate_website (theme = 'github.io/username/repository/')**.


## 3) Edit content on your website 
Every theme has a slightly different setup, but we will walk through the basic overview.  \
* **Config:** contains the backbone structure of your website. The menus.toml file can be edited based on what navigation links you would like to include on your website. In most cases, you do not need to edit the language.toml, config.toml, or params.toml files. \
* **Content:** This is where most of your editing will take place. There is a subfolder for each component of your website, and this will vary depending on your chosen theme. For example, each component (or 'widget') of the home page will be included within the 'home' folder. You can activate/inactivate or edit these .md files to your heart's content. \
* **Static:** This is the storage location for any static files that you add to your website. For example, you can add PDF files or images that are then linked to in a content page. \
* **Themes:** This stores the necessary stuff to build a website using your chosen theme. *Do not edit!* \
* **Public:** Contains the live website, built from the contents and configurations. *Do not edit!*

## 4) Preview your website 
* To preview an individual Rmd file: \
Click the **Preview** button at the top of the Rmd file in R studio
* To preview the entire wepage \
**blogdown::serve_site()** 
* The webpage will display in the viewer panel of R studio. \
* Click **open in a new window** (on the top left of the Viewer panel) to open the webpage preview in your browser.
* You only need to do this once during a single R session; the webpage preview will refresh after each time you save changes.


For additional details and trouble-shooting, see the official [Blogdown documentation](https://bookdown.org/yihui/blogdown/) for making a website using R markdown.
