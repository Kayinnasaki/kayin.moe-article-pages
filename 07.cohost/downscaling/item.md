---
title: 'Blogging and Downscaling on a Post Growth Internet'
date: '13-06-2023'
publish_date: '13-06-2023'
taxonomy:
  category:
    - 'Cohost'
  tag:
   - 'Chost-Repost'
   - 'Personal'
---

I figure some of you here would like this, as a lot of the my fellow cohosters are also filled with that post internet boom disillusionment.

My webspace is old. Like, really old. I have files on my webserver that were put there before some of my younger friends were *were even born*. No lie!

![](header.png?lightbox)
![This can't be safe and secure.](files.png?lightbox)

A set of coppermine php gallery files from 2003 to host my old art. Thanks to a close friend, who has always helped provide me with space on her various servers and VMs, I have had file continuity for now just over 20 years... and like that's cool, but that's *also bad*.

Like geologic layers of locks, my webserver became layers of old php files, different site revisions and a root directory filled with 2400 files and dozens of (often open) directories. Add atop this an aging, closed forum, mediawikis, and a wordpress site that was virtually never updated and I just had one big nasty security nightmare and it was a pain in the ass to try and back up anything.  What made this sting the most was occasional host outages. Not that it was ever a big deal, all hosts had outages... but I'd go to look up info on my wiki and it'd be down and then I'd have to think... "What if it never came back up? This would all be gone."

So something had to change.

## Beyond Old "Best Practices"

Old best practices was to get something proper and saleable. Use a mysql database. What if you got popular? What if you needed multiple servers? How are you going to **GROW**?

In the modern age where the web is dominated by huge companies, there is no "Growth" for a personal site, nor do many of us want it. We want a repository for our *things*, or *identity* and our *thoughts. So I decided right up, no mysql databases, no user accounts, no more fucking wordpress.*

Wordpress *especiall*y made me miserable. For something I update at most a few times of the year, I have spent hours fixing, tweaking, updating and debugging it. It's so huge and complicated that customizing and changing anything was a nightmare. I'd have to upgrade it for security reasons, only for it break my skin, and for me to have to figure out the arcane chaos of wordpress skin files. An absolute nightmare. What's worse was checking my apache logs *(don't do this, this is like googling your symptoms)* and seeing just how many hail mary attacks were constantly thrown at WP.

It had to go. I don't want to grow. I don't want to worry about SEO bullshit. I want a clean and simple experience that is a pleasure for me to update..

## New Update model and new tools

I had been using rsync to update a few projects (a private ~~adult~~ art gallery and my Map stuff) and found it enjoyable. I could sort my files locally and when stuff was right, hit a button and push an update. I liked this update model a lot, so I decided I wanted to set up a portable AMPP stack, with local copies of all my stuff. 

I ended up using Laragon for this, but in practice I could switch it to anything at any time. Even set up a dns redirect for kayin(dot)local so I could easily switch between online and offline copies just by changing the TLD. Just a local webserver and some bat files that I could easily back up by dragging and dropping some files.

![This feels so civilized](laragon.png?lightbox)

Secondly I wanted a flat file CMS. I debated using a lot of off-beat options, but settled on the Go-To everyone seems to like, Grav. Sometimes it's easier just to use whats popular, supported thing. The fun thing with Grav was... a base theme I'd use would rapidly end up not fitting my needs, but unlike wordpress, the code was simple enough that I could go in and change more than just the CSS. I was pretty easily able to add features and even custom formatting codes so I could layout images neatly. All and all just a pleasant experience. All I had to was hand convert all the blog posts I wanted.

This was a sad process because I realized I couldn't and shouldn't convert all of them. A lot of my old blog was trash, about dumb forum arguments or giving bad game design advice (or okay advice, but delivered poorly). I went from hundreds of posts to 25. While the process of web rot made me sad, this was a problem better left to the way back machine. That said, I tried my best to save important articles and maintain the same URL scheme for them (Like with the Reaction article). 

![I barely understand how .htaccess works](redirects.webp?lightbox)

What's great too is, while I don't do this yet, I can eventually set it up to send the grav files over, headless. No admin console, no users, no logging in. Just some images and text files. I don't want my data to matter!!!

## What Stays and what Goes

I've said before, maybe the idea that nothing on the web should ever die wasn't a great idea. That said I wanted to keep stuff that was important, no matter how stupid. Years ago I removed a bunch of old mugen tutorials someone asked me to host for them. These were from the mid 2000s and yet... someone asked me where they went in like 2017. They were still getting hits, so... 

![Shoutouts to Dark Dez](mugen.png?lightbox)

... I guess this is staying on my server forever. You know what? *cool*. Sometimes the web *needs* to rot, but not when something is still alive, somehow. There were a few other things like this (a lot of them you can find on my site's project page), but so much of it was trash that just didn't matter anymore.

... Old reaction memes from old form fights and stuff? That stuff had to go. I took it all, downloaded, backed it up, and locked it away, only to be added back if anyone ever asks.

Another switch was my personal wiki I used to track BE lore stuff. I realized I didn't need or even want it to be editable online, so I just... switched to SQLite, made the online copy read only and update it by pitching an sqlite file across the internet. This might seem incredibly stupid given the purpose of wikis, but the software serves me, I don't serve the software. It's what works for me, and trying to change things to serve the ideal of a wiki is pointless. Technically there is still a user account that could get compromised, but like, what are you even going to do with it?? There is no longer any data of value to steal.

The saddest loss is the IWBTG forums. I just cannot keep running unsecure versions of old forum software in perpetuity. I kept it up for years after closing it, so hopefully most of the things of value there have moved. I have the files and will keep them backed up, but it's too much of a liability

It's one of the things where if anyone in the community wanted to maintain it, I'd let them. I tried static site generation, but it didn't work nearly well enough. But a lot of people who were young idiots at the time said some dumb shit on there and sometimes it's just good to let people be free of their past.

![I'm not above loving big dumb Hero headers](new.png?lightbox)

So that's it, I got an empty root directory, neatly sorted files, and a CMS that I don't wanna punch in the face every time it updates. [If you wanna poke around the website](https://kayin.moe/) it's right there, though a lot of stuff I mentioned isn't actually public and it's the same old blog I had forever, just with less posts.

It's nothing new, outside the new layout I like a lot. But more important, I transformed something that gave me anxiety into something pleasant to use and maintain. All my important stuff is backed up now in multiple places and updating stuff can happen in private first so I can take my time, testing and refining things. 

A webspace made for a smaller, more sustainable web.