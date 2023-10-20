# Get started
## Prerequisites
Before you begin editing this site, you must:

- Install [Hugo](https://gohugo.io/installation/) (extended edition, v0.112.0 or later)
- Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

You must also be comfortable working from the command line.

## Get the site
Clone the site from Github.

# Content
The content on the homepage is managed in `data/landing.yaml`. All other pages are in Markdown files in `content/docs`. Images are put in `assets/images`. If you need other kinds of media files saved locally, please create a new folder in assets, e.g., `assets/audio`. The icons used throughout the site are Google's [Material Icons](https://fonts.google.com/icons?icon.style=Outlined&icon.set=Material+Symbols).

## Markdown
You can always check the [basic syntax](https://www.markdownguide.org/basic-syntax/) guide. If you're more comfortable working with a GUI or want to preview your Markdown, there are a bunch of [tools](https://www.markdownguide.org/tools/) you can use, including [Dillinger's online editor](https://dillinger.io/), and an [add-on for Google Docs](https://workspace.google.com/marketplace/app/docs_to_markdown/700168918607).

# Media
## Images
## BDR items
In a Markdown file, use the following syntax:
```
{{<panopto UUID >}}
```
The UUID will be replaced with a long alphanumeric string that you can get from the URL of the BDR item in Panopto.
