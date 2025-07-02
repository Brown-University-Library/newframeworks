# New Frameworks 
This repo is the documentation site for the [New Frameworks project](https://library.brown.edu/create/cds/portfolio/born-digital/). It is built in [Hugo](https://gohugo.io) and uses the [Lotus Docs](https://github.com/colinwilson/lotusdocs) theme, with some custom extensions by CDS. Both Hugo & Lotus Docs are well-documented!

## Content
The content on the homepage is managed in `data/landing.yaml`.

All other pages are in Markdown files in `content/docs`.

Images used in content are saved alongside their content. See the `content/docs/team` folder for an example: the text is in the `index.md` file, and the several .jpgs in the folder are referenced in the file. See below for the shortcode to add an image to your content.

## Media

### Images
Use the [built-in Hugo shortcode](https://gohugo.io/content-management/shortcodes/#figure).

An example for an artist headshot that displays 200px wide (the original image is larger) and has text wrapped around it:
```
{{< figure src="morrissey.jpg" alt="Judd, unsmiling" caption="photo courtesy Judd Morrissey" width="200" class="me-3 figure float-start">}}
```

### BDR items
In a Markdown file, use the following syntax:
```
{{<panopto UUID >}}
```
The UUID should be the long alphanumeric string at the end of the URL of the BDR item in Panopto. For example: if you wanted to embed the BDR item at `https://brown.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=67c067ff-14d9-48d7-9687-af9e00f0e273`, the UUID would be `67c067ff-14d9-48d7-9687-af9e00f0e273` and the shortcode would be `{{<panopto 67c067ff-14d9-48d7-9687-af9e00f0e273 >}}`.

## Deploying
There is a Workflow in `.github/workflows/hugo.yml` which auto-deploys updates to the `master` branch to Reclaim.