# Creating the Project Webpage using GitHub Pages

This short tutorial will show you how to:

* Fork and clone the project template
* Make changes to the template
* Update your git repository with the changes
* Introduce you to Markdown

Disclaimers:

* The general steps are presented here. If you need to, follow the videos for finer details.
* This is not a full Git, Python, HTML or Markdown tutorial. View the documentation for further details.
* This tutorial is was created using a Mac. There will be minor differences in Windows, but you should be able to troubleshoot those.

## Prerequisites

Before you begin, make sure you:

* Have created a [GitHub account](https://github.com/)
* Have installed latest version of [Python](https://www.python.org/downloads/)
* Have installed latest version of [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Step 1: Fork the template
[](https://www.youtube.com/watch?v=KxRaG-HqKm4)
<a href="https://www.youtube.com/watch?v=KxRaG-HqKm4" target="_blank">Video</a>

1. Log in to your GitHub account
2. Go to https://github.com/hcitang/481-project-template, and click the "Fork" button at top right

## Step 2: Set up GitHub pages
[](https://youtu.be/7jhC4IQu1K4)
<a href="https://youtu.be/7jhC4IQu1K4" target="_blank">Video</a>

1. Rename the repo in Settings
2. In Settings, set GitHub pages source to be "master branch"
3. The link to your live site will be displayed in Settings

## Step 3: Create a local version of the site for editing
[](https://www.youtube.com/watch?v=3uguEl11r1s)
 <a href="https://www.youtube.com/watch?v=3uguEl11r1s" target="_blank">Video</a>

1. From your forked version of the repo (this is important, make sure it's your version), click the "Clone or Download" button.
2. Copy the link to your clipboard.
3. From your terminal, execute the following command in the directory you want your project to be in: 
  * `git clone *COPIEDLINK`
4. Make any changes to the local files, and push them back to the repo using the terminal. Ex:
  * `git add index.md`
  * `git commit -m "editing index.md"`
  * `git push origin master`

## Step 4: Run a python server to view changes locally
[](https://www.youtube.com/watch?v=AQYEXG2FHwA)
<a href="https://www.youtube.com/watch?v=AQYEXG2FHwA" target="_blank">Video</a>

1. With python installed, type the following command in the terminal (from your local project directory): 
  * `python -m SimpleHTTPServer 8000`
  * View <a href="http://www.linuxjournal.com/content/tech-tip-really-simple-http-server-python" target="_blank">this link</a> for a more in-depth tutorial
2. Navigate to http://127.0.0.1:8000 in your browser
  * The local site will be updated with saved changes
3. Once you're satisfied, push changes to the GitHub repo (as in Step 3)

## Resources: View Markdown documentation
[](https://www.youtube.com/watch?v=-fm0RRJfxGg)
<a href="https://www.youtube.com/watch?v=-fm0RRJfxGg" target="_blank">Video</a>

* [MDWiki](http://dynalon.github.io/mdwiki/#!index.md) - The template relies on a package that automagically renders out webpages based on markdown files (basically, text files with very simple markup).
* [Markdown Syntax (original)](https://daringfireball.net/projects/markdown/syntax) - Markdown was invented by John Gruber. This is the original syntax (note: it is not fully "standardized").
* [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) - A Markdown syntax cheatsheet.