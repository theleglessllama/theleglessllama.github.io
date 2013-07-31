---
layout: post
title: "Creating a New Post"
date: 2013-07-29 11:37
comments: true
categories: [Tech Support]
---

We're running [Octopress](http://octopress.org/) on [Github Pages](http://pages.github.com/). If the previous sentence, or the links referred to in that sentence looked like Greek to you and you really only want to make one post, we highly recommend you approach someone from AAD, or Linan, or Kenneth, to help you publish your post. This method's been scientifically proven to cause less hair loss.

Really want to learn Greek? Let's get started then. This is a "Dummy's Guide", by the way. If you have a degree/major/minor in Computer Science, or are going to get one, it may be easier for you to follow the documentation provided by Octopress themselves in the link above.

## Introduction to Octopress
Octopress is a blogging engine for hackers. It doesn't have a GUI like [Tumblr](http://tumblr.com/) or [Blogspot](http://blogspot.com/) with buttons for you to click and a nice space for you to upload photos and type your post. Everything's done from the command line, and posts are written a text file. Let's break that down bit by bit. 

Octopress is built off a page management system called Jekyll. The reason why we don't set up Jekyll directly, is because Jekyll is one sonovabitch to get working, so we use Octopress. 

Octopress runs off Git and [Github](http://github.com/). Git is version control software. It looks at all your files, compares it to the "stock" version on a server and shows you the difference between the two, asking what changes you'd like to keep and what you'd like to throw away. Github is a website that stores all the Git data and makes life easier for people who find using Git from a command line too daunting.

## Step 1: Get Permission
You'll need to be added as a collaborator in the repository in order to post. Create a Github account if you don't already have one, and drop a note to Kenneth to add you in.

## Step 2: Cloning Octopress
We'll start by making a copy of Octopress. If you're a command-line addict, run:
```bash
git clone git://github.com/theleglessllama.github.io.git OEKR
cd OEKR
```
in a directory of your choice. If you're not, visit our [Github Repository](http://github.com/theleglessllama.github.io) and click "Clone to Desktop". A dialog box will pop up asking you where you'd like to save the files. Both methods are identical.

## Step 3: Creating a New Post
Hereforth you may shy away from the command line no longer. Open Terminal or [iTerm](http://www.iterm2.com/) (we don't really care about Windows, but if it pleases you, open that bloatware called MS-DOS Prompt) and type:
```bash
rake new_post
```
This will return a prompt asking for the title of your post. Fill that up accordingly, hit enter, and your post will be created. 

Posts in Octopress are created as text files written in [Markdown](http://daringfireball.net/projects/markdown/) (i.e. they have a file extension of either ".md" or ".markdown"). Markdown is a simple markup language that allows you to specify things like lists, headers, quotes and the likes. You should learn it. 

## Step 4: Editing Your Post
The astute reader will realize that in the previous step, all we did was create the title of the post, and the post itself, but not the content of the post. Unfortunately brain-scanning technology hasn't yet been invented. We're told that Gary Lee is interested in working on that, but seeing as how he won't get his PhD until seven years later, and his bond won't be finished until six years on top of that, nope, it's not coming anytime soon.

The newly created post will be found in ```source/_posts```, and named according to Jekyll's naming conventions. Basically it looks like this:
```
YYYY-MM-DD-post-title.markdown
```
Nothing fanciful, but it does the job. Open the file, and you'll be greeted by some preamble that looks like this:
```yaml
---
layout: post
title: "Your Title"
date: 2011-07-03 5:59
comments: true
external-url:
categories:
---
```
It's really self-explanatory. Change the title, add your categories (in the format [category A, category B], if you have more than one), then write your post below the triple hyphens.

If you're still having difficulty, check out the [documentation from Octopress themselves](http://octopress.org/docs/blogging/).