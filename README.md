# New Frameworks 
This repo is the documentation site for the [New Frameworks project](https://library.brown.edu/create/cds/portfolio/born-digital/). It is built in [Hugo](https://gohugo.io) and uses the [Lotus Docs](https://github.com/colinwilson/lotusdocs) theme, with some custom extensions by CDS. Both Hugo & Lotus Docs are well-documented!

# To run a local server
If you want to run a local server and see the changes you make in-context on the site, follow these instructions. This requires a little more up-front setup.

## Prerequisites
Before you begin work, you must:

- Install [Hugo](https://gohugo.io/installation/) (extended edition, v0.112.0 or later)
- Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

You must also be comfortable working from the command line. You'll need a Github account (that's authorized to access Brown University Library repositories) and have set that account up to interact with Github. You can use a GUI such as [Github Desktop](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop) for this, but you will still have to use the command line for Hugo.

## Get started
1. Fork [the repo on Github](https://github.com/Brown-University-Library/newframeworks).
2. Download, aka clone, your fork to your local computer.
3. Start the Hugo site. Basic commands are [documented in the Hugo docs](https://gohugo.io/getting-started/usage/). Follow those instructions to get the site running locally.
4. Make your edits (see below).
5. Commit those changes and push them up to Github.
6. [Create a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork). You can request a specific person's attention by adding them as a "reviewer" to your pull request.
7. Someone else on the project team must review your work before it is merged into the main repository and deployed to the web.

## Next time
After the initial setup, you can start at step 3 above.

Periodically check for updates other people have made. To do so, the box at the top of your fork on Github may say something like "This branch is 2 commits behind Brown-University-Library:master". If your fork is _behind_, please click the "sync files" button on the right, and then the "update branch" button, _before_ you make any changes. There should now be a cheerful blue alert at the very top of the page saying "Successfully fetched and fast-forwarded from upstream Brown-University-Library:master."

# If you want to edit page content in your browser

## Set up your workspace for the *first time*

_This is very detailed, please do not freak out!_

You must have a Github account. On the New Frameworks repository page, click the "Fork" button. You now have your own copy of the site to make changes to. Click on any file, and you will see the file content.

On the upper right, there is a button with a pencil icon and a dropdown; open the dropdown and select `github.dev`.

Make your changes in the files in the `content/docs` folder (see below for details). Once you have made changes, there will be an icon on the left with a blue badge showing the number of changes you've made; when you're done, click on that icon. There will be a small textbox. Enter a _short_ description of what you've done (for example, "Added description of spaghetti pie, corrected typos") and click the "commit and push" button.

Return to _your fork_ on Github (e.g., https://github.com/elizabethyalkut/newframeworks) There will be a box saying something like "This branch is 2 commits ahead of Brown-University-Library:master". Click the "Contribute" button in that box and a popover will appear with a green "Open pull request" button, which you should click.

You can write a more detailed explanation of what you have changed, and then click the green "create a pull request" button. Your work is done! 🎉

(Someone else must review your changes before they go live, just as a double-check. You can request a specific person's attention by adding them as a "reviewer" to your pull request.)

## Returning to your workspace
Return to _your fork_ on Github (e.g., https://github.com/elizabethyalkut/newframeworks)

If someone else has been working on the site, the box at the top may say something like "This branch is 2 commits behind Brown-University-Library:master". If your fork is _behind_, please click the "sync files" button on the right, and then the "update branch" button, _before_ you make any changes. There should now be a cheerful blue alert at the very top of the page saying "Successfully fetched and fast-forwarded from upstream Brown-University-Library:master."

You may now repeat the editing process as before, beginning with the pencil-icon dropdown and clicking on "github.dev".

# Content
The content on the homepage is managed in `data/landing.yaml`.

All other pages are in Markdown files in `content/docs`. At the top of every Markdown file, there is "front matter" -- information so that Hugo can build the site correctly. You can update the _values_ here (change the title! add a useful description! make the draft status true or false!).

Images used in content are saved alongside their content. See the `content/docs/team` folder for an example: the text is in the `index.md` file, and the several .jpgs in the folder are referenced in the file.

If you're using the local server process, at top, to _create_ new content, make sure to use the `hugo new` [command to generate a Markdown file](https://gohugo.io/getting-started/quick-start/#add-content) with useful front matter.

(If you're using the browser editor, I'm still writing that documentation.)

## Markdown
You can always check the [basic syntax](https://www.markdownguide.org/basic-syntax/) guide. If you're more comfortable working with a GUI or want to preview your Markdown, there are a bunch of [tools](https://www.markdownguide.org/tools/) you can use, including [Dillinger's online editor](https://dillinger.io/), and an [add-on for Google Docs](https://workspace.google.com/marketplace/app/docs_to_markdown/700168918607). (Obviously, you'll have to move anything you edit using those tools into the codebase so other people can access it.)

# Media

## Images
Use the [built-in Hugo shortcode](https://gohugo.io/content-management/shortcodes/#figure).

## BDR items
In a Markdown file, use the following syntax:
```
{{<panopto UUID >}}
```
The UUID should be the long alphanumeric string at the end of the URL of the BDR item in Panopto. For example: if you wanted to embed the BDR item at `https://brown.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=67c067ff-14d9-48d7-9687-af9e00f0e273`, the UUID would be `67c067ff-14d9-48d7-9687-af9e00f0e273` and the shortcode would be `{{<panopto 67c067ff-14d9-48d7-9687-af9e00f0e273 >}}`.

# To-do
- set up a Reclaim deployment workflow, document
- get the various CSS additions to compile & attach properly
- spec the link to sketch in artist page; is the Hugo [Related Content](https://gohugo.io/content-management/related/) thing overkill?
- Document creating new content using github.de
