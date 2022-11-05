---
layout: post
title: How I created my personal website
description: >
  Some notes, tips and tricks on how you can create a website the way I did.

hide_description: false

noindex: true
---

<img src="../assets/img/giphy.gif" alt="giphy" style="width:200px;"/>

I primarily worked with Jekyll templates and Ruby. I forked an amazing template made by Florian, who also goes by [@qwtel](https://qwtel.com) from the GitHub repository [here](https://github.com/hydecorp/hydejack). So, I extend my special thanks to the creator of the template, Hydejack!

<!-- ![giphy.gif](../assets/img/giphy.gif) -->



At the beginning, I did seem to struggle a bit to make the template work when hosting it on GitHub pages. It felt like I followed most of the instructions but I seemed to be able to make it work locally but not after deployment. I tried out other templates which did not seem to have this problem, but decided to stick with the hydejack template due to design choice.

Most of the instructions are already provided by Florian on the main website, so I will try to pick out points and consolidate the details that are required to make a website on GitHub pages smoothly. I will try to make this small and concise with only the necessary resources. Expand the toggle for more details.

### Install Jekyll and Ruby**:**

Follow this link for [this](https://jekyllrb.com/docs/installation/) step. The steps are quite straightforward and should not be confusing.

### **Get the website working:**

- Fork the hydejack template repository from [here](https://github.com/germa89/hydejack).
    
    This is not directly from the hydejack repository but a fork of the original hydejack master branch. I was not able to make the gh-pages branch work on GitHub pages. Alternatively, feel free to fork my repository (code attached to the bottom of the document).
    
- On your _config.yaml file, make the following changes:
    
    ```yaml
    url:                   https://<username>.github.io
    baseurl:               ''
    ```
    

These are the only changes you need to get the website working! You can test it out locally using these commands on your terminal:

```bash
bundle install # done only once, if this already hasn't been done
bundle exec jekyll serve # to execute the website locally
```

To deploy it on GitHub pages:

- Commit and push the changes into your repository. It may take some time but you should be able to deploy the latest version of the website using the specified url.

### Designing your website

There’s not much I can add apart from what Florian has already documented in his website [here](https://hydejack.com/docs/config/#adding-an-author).

Although, I do think a summary of the important files and directories, where I personally made changes while making my website, would help new web-designers understand faster.

- _config.yml
    
    This is the main yaml file that you will be using to make changes to sidebar images, accent colors, add links to sidebar and landing page, pagination on the blog, change fonts along other things.
    
- _data
    - authors.yml
        
        You can provide a list of authors for your blog here, and each of their social and email IDs. Icons will be automatically allotted for each social ID, if you have the social.yml file in the same directory.
        
    - resume.yml
        
        Even though I didn’t exactly use it, I think this may be another important file for you to edit if you are purchasing the PRO version. 
        
- _layout
    
    Although, there may not be any need to edit any file in this directory, I thought it would be worthwhile for you to go through all the file here so that you can understand what kinds of pages you can create with .html files provided here. It may help if you want to create custom pages for your website. Below are some of the common ones that I used:
    
    - about.html
        
        Helps create the about page for your website. You can include contact details as well as a short description of yourself.
        
    - blog.html
        
        This was the starting navigation page from my website that appears after swiping over the landing page. But, I believe you can change the landing page.
        
    - page.html
        
        Creates a simple page, that you can use to create anything that you don’t want to put in a blog. For example, you can create a projects page and add it as a link to your sidebar menu.
        
    - post.html
        
        What you write here goes into the blog.
        
- _posts
    
    You can create separate .md files for each of your blog post here by naming them according to the date created (or the date you want it to appear as in your blog). For example, for my first blog post, I created a file named “2022_11_04-first-post.md”. This should automatically create an index.html file in _site folder, with the HTML code for your post.
    
- assets
    
    This directory helps keep all images, icons, gifs that go into your website in one place. While writing in a .md file, you can refer to an item in this directory by defining a path through assets. For example, in my code, I have a directory created for icons, another for background images, and another for project reports and so on.
    

There are definitely many other options and customization tools but these should be more than enough for a beginner to start coding up their website.

### [Code](https://github.com/Mirudhula-m/mirudhula-m.github.io)

Click on the link above to refer to the code for my website.

~~~~~~~~~~~~~~

Hope this helped!