---
layout: post
title: "Creating a New Post"
date: 2013-07-29 11:37
comments: true
categories: [Tech Support]
---

We're running [Octopress](http://octopress.org/) on [Github Pages](http://pages.github.com/). If the previous sentence, or the links referred to in that sentence looked like Greek to you and you really only want to make one post, we highly recommend you approach someone from AAD, or Linan, or Kenneth, to help you publish your post. This method's been scientifically proven to cause less hair loss.

Really want to learn Greek? Let's get started then. This is a "Dummy's Guide", by the way. If you have a degree/major/minor in Computer Science, or are going to get one, it may be easier for you to follow the documentation provided by Octopress themselves in the link above.
<!--more-->

## Introduction to Octopress
Octopress is a blogging engine for hackers. It doesn't have a GUI like [Tumblr](http://tumblr.com/) or [Blogspot](http://blogspot.com/) with buttons for you to click and a nice space for you to upload photos and type your post. Everything's done from the command line, and posts are written in a text file. Let's break that down bit by bit. 

Octopress is built off a page management system called Jekyll. The reason why we don't set up Jekyll directly is not because we can't but is because Jekyll is one sonovabitch to get working, so we use Octopress. 

Octopress runs off Git and [Github](http://github.com/). Git is version control software. It looks at all your files, compares it to the "stock" version on a server and shows you the difference between the two, asking what changes you'd like to keep and what you'd like to throw away. Github is a website that stores all the Git data and makes life easier for people who find using Git from a command line too daunting.

It's important that you understand this before we go any further.

## Step 1: Get Permission
You'll need to be added as a collaborator in the repository in order to post. Create a Github account if you don't already have one, and drop a note to Kenneth or Linan to add you in.

Once again, I'll say that if the following decision chain matches your current frame of mind:

1. You're not good with Tech
2. You're not feeling particularly adventurous and don't feel the immediate need to learn about these things
3. You just want to make a one-off post
You'll be likely better off passing us your article and letting us do the heavy-lifting for you. No worries there.

## Step 2: Cloning Octopress
We'll start by making a copy of Octopress. If you're a command-line addict, run:
``` bash
git clone git://github.com/theleglessllama.github.io.git OEKR
cd OEKR
bundle install
```
in a directory of your choice. 

If you're not, visit our [Github Repository](http://github.com/theleglessllama.github.io) and click "Clone to Desktop". A dialog box will pop up asking you where you'd like to save the files. Both methods are identical.

If you've already cloned Octopress before and just want to add a new post now, be sure to run:
``` bash
git pull
```
from the Octopress directory. This updates your local copy with the latest copy from the server, if there's been any changes.

## Step 3: Creating a New Post
From here on you may shy away from the command line no longer. Open Terminal or [iTerm](http://www.iterm2.com/) (we don't really care about Windows, but if it pleases you, open that bloatware called MS-DOS Prompt) and type:
``` bash
rake new_post
```
This will return a prompt asking for the title of your post. Fill that up accordingly, hit enter, and your post will be created. 

Posts in Octopress are created as text files written in [Markdown](http://daringfireball.net/projects/markdown/) (i.e. they have a file extension of either ".md" or ".markdown"). 

Markdown is a simple markup language that allows you to specify things like lists, headers, quotes and the likes. You can and should learn it at the link above. It was written by the very guy who wrote the language, and it's really quite simple.

## Step 4: Editing Your Post
_The astute reader will realize that in the previous step, all we did was create the title of the post, and the post itself, but not the content of the post. Unfortunately brain-scanning technology hasn't yet been invented. We're told that Gary Lee is interested in working on that, but seeing as how he won't get his PhD until seven years later, and his bond won't be finished until six years on top of that, nope, it's not coming anytime soon._

The newly created post will be found in ```source/_posts```, and named according to Jekyll's naming conventions. Basically it looks like this:
```
YYYY-MM-DD-post-title.markdown
```
where ```post-title``` is a hyphen-delimited version of whatever you specified earlier in the title field. Nothing fanciful, but it does the job. 

Open the file, and you'll be greeted by a preamble that looks like this:
``` yaml
---
layout: post
title: "Your Title"
date: 2011-07-03 5:59
comments: true
external-url:
categories:
---
```
It's really self-explanatory. Let's break that down. 

Leave ```layout```, ```date``` and ```external-url``` unchanged. No hard feelings, but if you know what those do, you won't really be needing this guide. 

``title`` is whatever you want your title to be. It must be encapsulated in double quotes. Feel free to get creative, but keep it short.

``comments`` is a boolean (meaning it can be set to true or false) that enables or disables, well, comments. We won't insult your intelligence telling you what to do with this one.

``categories`` is a little more interesting. This allows you to tag your posts so there's some sense of order to them. You can write something like:
``` yaml
categories: Shit Kenneth Says
```
across posts, and it'll get grouped neatly for you in a link in the sidebar. If you want to add multiple categories:
``` yaml
categories: [Shit Kenneth Says, Shit Linan Says]
```
or
``` yaml
categories:
- Shit Kenneth Says
- Shit Linan Says
```
will do the job for you. Savvy?

Write your post after the ```---``` that signifies the end of the preamble. This can be as long as you'd like it to be. Just don't write us the Iliad, or the Odyssey, or 50 Shades of Gray.

## Step 5: Preview Your Post
_By now you're thinking that this whole posting thing is like taking off your suspenders, pants and undergarments just so you can fart. Hold on a little longer, and I'll show you why it's worth the trouble._

After you've written your post you'll likely want to see how it looks like. We're vain people, we understand. 

Go back to the command line and run:
``` bash
rake generate
rake preview
```
The terminal window will spit out a bunch of text that seems to be telling you that files are changed (wow!) and that it's going to preview your post for you (double wow!). 

After you're done with that, go back to your browser and navigate to [http://localhost:3000/](http://localhost:3000/), where you'll see a local version of the blog waiting for you in all it's glory.

_If you look at Jethro or Kenneth's computers, you'll find that we _navigate to an address like http://octopress.dev instead of the funny localhost and four digit number thing. That's because we're awesome. No really. But if you want to learn to be awesome, here's [another article]() on that for you._

Give your post a good look over, and if you're happy with what you see, we'll now move into deploying the post to the actual site.

If you'd like to make any changes, go ahead and update your content in the ```.markdown``` post file. This time, however, because ```rake preview``` is already running, you don't need to re-run it. Changes will automagically be detected and applied live in the browser. I know, I know.

## Step 6: Deploying
_We'd like to personally assure you that this is the most straightforward step in the entire damn tutorial._

Go back to the command line, turn off ```rake preview``` if it's running (That's ```Ctrl+C``` on Windows or ```CMD+C``` on OS X if you don't know how). Then type:
``` bash
rake deploy
git add .
git commit -m "New Post"
git push origin source
```
Go for a coffee while the command line window spits out stuff that doesn't make sense to you. 

Come back, visit [http://theleglessllama.github.io/](http://theleglessllama.github.io/) and give yourself a pat on the back. You're done.

In case you're wondering what we did in that line of text above (boy, your teacher is going to be so proud of you), here's what actually happened. 

We first told Octopress to generate a production version of the post you created. This checks it for any errors, tidies up everything, and makes sure the links, images, and stuff like that all work properly. 

Next, it takes the new post you've created and adds it to our live server. This process could take a bit of time depending on how fast your connection is.

Once that's done, the next three lines tell your computer to update the source files on the back-end of the server with the raw data of the post that you created. This is done so that other people who pull from the repository can make edits to your post if they'd like to.

## Why The Hassle?
At the back of your head there's this nagging concern that this is possibly the most overkill way to create a blogpost ever. If you don't think that's the case (for some reason), here's a quick workflow to prove our point:

1. Create Post
2. Edit Preamble
3. Write Post
4. Preview
5. Edit Post
6. Generate Post
7. Deploy Post

This process allows us to have incredibly granular control over the posting process. With the exception of (7), everything else doesn't require the Internet. You could be in the middle of the Nevada Desert happily writing a post - or many posts - and only push everything back onto the server once you felt like it (or you returned to civilization). 

In addition, multiple people can all be writing posts at the same time on their own computers, and we wouldn't get confused at all. We'd know who wrote exactly what, who changed what, and who's posting what. At any time if we're not comfortable with something, we can quickly roll-back to a previous version, and it'll all be seamless.

## Further Reading
If you're still having difficulty, check out the [documentation from Octopress themselves](http://octopress.org/docs/blogging/).

We'd like to think that we described it in a manner that's hopefully a bit more friendly for beginners, but well, we didn't write the book - they did. So there.