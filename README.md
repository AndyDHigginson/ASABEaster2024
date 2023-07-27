# MacaqueNet Website

Source code for [https://macaquenet.github.io/](https://macaquenet.github.io/)

# Acknowledgements

MacaqueNet would like to thank Julia Watzek, the builder of the ManyPrimates website who's base code we utilised for this website (details provided below). Julia provided her invaluable knowledge and guidance in the creation of the MacaqueNet website. 

## Structure 

The website structure detailed below is based on the open code from the ManyPrimates GitHub repository. Some of the code files detemrining the underlying website structure and layout are unchanged. All .md project files and images have been replaced with MacaqueNet's content, and fonts, colour schemes and page layouts have been altered accordingly. 

(not all folders shown)

```
.
├── _config.yml         <-- some general settings/info
├── _includes           <-- building blocks for each page
├── _layouts            <-- collection of different page layouts
├── assets
│   ├── conferences     <-- put PDFs for slides/posters here
│   ├── images          <-- put images here
│   └── pdfs            <-- put PDFs for published papers here
├── index.md            <-- edit these .md files to edit content
├── database.md
├── diversity.md
├── drivers.md
└── [...].md
```

## Prerequisites

You need some basic familiarity with these tools to make edits to the website. The good news is that 2-3 commands will cover 90% of use cases, so don't get overwhelmed. There's no need to learn everything.

- Git & GitHub: 
    - to sync this online folder/'repo' with one on your computer and keep track of who made what changes and when
    - check out, e.g., [this guide](https://guides.github.com/introduction/git-handbook/) to get started
- Markdown: 
    - to format text on a website with really simple syntax in plain-text files (e.g. `**I want to make a bold statement.**` turns into **I want to make a bold statement.**)
    - check out, e.g., [this guide](https://guides.github.com/features/mastering-markdown/) to get started

Knowledge of HTML is very optional. If you already know some, you can mix and match Markdown and HTML bits when editing the `.md` files. Sometimes that's useful because there's no equivalent in Markdown for what you want to do.

## Making changes to the content

- Fetch any upstream changes to your local repo (i.e., make sure you have the latest version)
    - You can ignore almost all of the folders/files. It's set up so that you simply edit the content and it'll do the rest automatically
- Edit the text in the Markdown `.md` files
- Put images, PDFs, etc. that you reference in the `assets` subfolders
- Use relative urls whenever possible, e.g. `pilot.html` instead of `https://macaquenet.github.io/pilot.html`
- **Do not touch the files in the folders that start with an `_`underscore unless you're sure you know what you're doing!**

## Setting up a local site to preview changes

- Have a clone of the github repo on your local machine

- We recommend creating a local clone using RStudio (read here to find out how --> https://resources.github.com/github-and-rstudio/ )
    - You can make changes to your github files within RStudio and then you need to commit the changes, then push the changes. You have to click push for your changes to transfer to your online repository.
- Julia recommends:
    - Install Jekyll: `gem install bundler jekyll`
    - If that gives you any errors, google them... or check [here](https://jekyllrb.com/docs/installation/)
    - Install jekyll-seo-tag: `gem install bundler jekyll-seo-tag`
    - `cd` into the git repo for the website
    - Build local Jekyll site: `bundle exec jekyll serve`
    - Open browser and go to: `http://localhost:4000`
    - You should see any changes you save on your local `.md` files (refresh)
    - Push your changes when you're happy with the preview! GitHub will then (re)build the site (typically within a few minutes)

