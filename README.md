# New Frameworks
This repo is the documentation site for the [New Frameworks project](https://library.brown.edu/create/cds/portfolio/born-digital/). It is built in [Hugo](https://gohugo.io) and uses the [Lotus Docs](https://github.com/colinwilson/lotusdocs) theme, with some custom extensions by CDS. Both Hugo & Lotus Docs are well-documented!

# Prerequisites
Before you begin editing this site, you must:

- Install [Hugo](https://gohugo.io/installation/) (extended edition, v0.112.0 or later)
- Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

You must also be comfortable working from the command line.

# Get started
Clone [the repo from Github](https://github.com/Brown-University-Library/newframeworks). Basic commands are [documented in the Hugo docs](https://gohugo.io/getting-started/usage/). Follow those instructions to get the site running locally. Make your edits (see below). Commit those changes and push them up to Github. *Deployment instructions to come!*

# Content
The content on the homepage is managed in `data/landing.yaml`. All other pages are in Markdown files in `content/docs`. Images are put in `assets/images`. If you need other kinds of media files saved locally, please create a new folder in assets, e.g., `assets/audio`. The icons used throughout the site are Google's [Material Icons](https://fonts.google.com/icons?icon.style=Outlined&icon.set=Material+Symbols). To _create_ new content, make sure to use the `hugo new` [command to generate a Markdown file](https://gohugo.io/getting-started/quick-start/#add-content) with useful front matter.

## Markdown
You can always check the [basic syntax](https://www.markdownguide.org/basic-syntax/) guide. If you're more comfortable working with a GUI or want to preview your Markdown, there are a bunch of [tools](https://www.markdownguide.org/tools/) you can use, including [Dillinger's online editor](https://dillinger.io/), and an [add-on for Google Docs](https://workspace.google.com/marketplace/app/docs_to_markdown/700168918607).

# Media

## Images
For images in the `assets/images` folder, use the [built-in Hugo shortcode](https://gohugo.io/content-management/shortcodes/#figure).

## BDR items
In a Markdown file, use the following syntax:
```
{{<panopto UUID >}}
```
The UUID will be replaced with a long alphanumeric string that you can get from the URL of the BDR item in Panopto. (I know this is confusing, I'm working on a better way to get this information and explain the process.)

# To-do
- set up a Reclaim deployment workflow, document
- see if there's a way to embed Panopto resources with a BDR ID
- add headshots to team section/page
