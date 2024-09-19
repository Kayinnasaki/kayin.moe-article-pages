---
title: 'Using CSS to make Discord Better'
date: '20-08-2024'
publish_date: '20-08-2024'
taxonomy:
  category:
    - 'Cohost'
  tag:
   - 'Chost-Repost'
---
![](0.png?lightbox)

Discord is truly a wretched app, and with each update they add more and more needless buttons, noise, and nonsense, likely at the behest of some talentless facebook middle manager that they hired, who makes more in a year than you've made in your entire life.

While nothing will fully stop the rapid enshittification of discord (and frankly other platforms), but we can mend the papercuts.

... At least on desktop.

Anyways in this, I'm going to talk about taking the above image, and using CSS to get to this.

![](1.png?lightbox)

## We love CSS around here

We love CSS around cohost! We love *CSS Crime*. In the era where almost every "native" application is a webpage in some kind of wrapper, using CSS can become *kinda punk*. The visual nature of CSS leads to a lot of low stakes comedy, like the [Github CSS Exploit](https://stevemats.medium.com/css-injection-on-github-profiles-from-unicode-exploits-to-new-bypass-techniques-f73f343f05d8). Malicious CSS attacks are *possible*, but generally speaking, CSS at worst is *street graffiti*.

If you're a developer, CSS kinda sucks, but that's another story. We're the proles today.

## Discord, CSS, changing CSS on Discord, and Caution

Discord, as a desktop app, is, like mentioned above, merely a web browser. As such, it can be freely styled by CSS. Discord doesn't easily allow this by default, but we have a few options. All the major discord mods(things like BetterDiscord and VenCord) allow you to add CSS freely. Those things are cool *and pretty safe*, but also allow a lot of *unsafe stuff*. You almost certainly won't get banned for just using BetterDiscord or VenCord, but you *could* be banned, or even hacked, for many of the 3rd party plugins they allow. Discord doesn't check if you're using a modified client, but they *do notice* if you're making illegal API calls. Running custom javascript in discord is *fun*, but comes with a *lot* of risks. If you go this route, I recommend being *extremely selective* which what features you enable. That said, I might value my discord account more than a lot of you.

Instead, I'm going to talk about [BeautifulDiscord](https://github.com/leovoel/BeautifulDiscord), because it's what *I* use, because it does *exactly* what I want it to, and nothing more. It gives me a CSS file I can edit. The whole thing is like 800 lines of python, mostly in two files. If you're a coder and wanted to, you could read and understand the whole thing pretty reasonably. Slim and simple.

A 3rd option real quick is to [*enable the inspector*](https://github.com/brunos3d/discord-enable-devtools) in Discord. We'll get to using browser inspectors, but the inspector and console attached to it used to be used constantly for (honestly pretty obvious) scams. I have a friend who uses the inspector to set their custom CSS manually every time they restart discord. This would be the "100% legit" way to do things if you wanted, since you're not actually modifying the client at all.

**Edit:** A 4th option I keep seeing is [openASAR](https://openasar.dev/), which rewrites parts of discord to be faster while giving options for themeing. This isn't one of those big plugin mods with a store system or something like BD or Ven, so while I haven't used it, I'd still recommend it as it has an easy install, performance gains, and nothing sketchy looking.

Regardless of which way you go, the parts after installing BeautifulDiscord should all be relevant.

### Installing BeautifulDiscord

This is the slightly annoying part, especially for the average user. BeautifulDiscord requires *python* to install. You can install it through [python.org](https://www.python.org/downloads/) or, if you're on windows(honestly, I'm not sure how some of this stuff works on Mac or Linux), use the Microsoft store. The Microsoft store version is largely fine and less confusing. It's the version I use, because I'm lazy. 

Just search for python and pick the highest current version (3.11 at the time of this writing).

So now we could do a bunch of stuff on the command-line, but instead I'm going to have you make two **.bat** files. Just open notepad or whatever and put in.

```py
py -i -m pip install -U https://github.com/leovoel/BeautifulDiscord/archive/master.zip
```

**py -m pip** tells python to use its native version of **pip** the python package manager. **install -U [url]** obviously is used to install the file at the given URL (as found on BeautifulDiscord's github). The **-U** means this will upgrade the package if it's out of date too. I have this file named **updateBeautifulDiscordCore.bat**, but you can save it as anything, as long as it ends in **.bat**.

Run it once. Now that the package is (hopefully) installed, we actually have to *use it* on discord. For that I make a second bat files.

```
py -i -m beautifuldiscord --css D:\bd\tweaks.css
```

**Don't** just fully copy and paste this one. This is where I put *my* files. I have this named as **updateDiscordBD.bat**

![](2.png?lightbox)


Change D:\bd\ to whatever you want. Change tweaks.css to whatever you want. You could do *C:\Users\[username]\Desktop\BeautifulDiscord\style.css* if you want. I like to keep the bat files in the same folder, with the css file, but they don't have to be. You'll be able to change this later if you want by editing(I assume most cohosters are savvy, but if you're not, you can just open the bat with notepad again. Just drag the file onto an empty notepad window) and rerunning the script.

Run this, with discord open. It should close discord and reopen it and... nothing should be different?

*I THINK BD will make the .css file for you, but if it doesn't just open notepad and make tweaks.css or style.css or whatever name you thought was cool*

Also as a note, every time discord updates, your changes may go away. To restore them, run **updateDiscordBD.bat** again. If that doesn't work, discord might have pushed a major update, in which case, you run **updateBeautifulDiscordCore.bat**, then **updateDiscordBD.bat** again. I haven't had to run Core in years, but sometimes it can take a bit for updates to happen so you can go check the github if you're curious.

## Figuring out CSS and what to Change

My recommendation here is to open up discord in a web browser(It works about the same in Firefox and Chrome). You could do the *client inspector* method above, but for ease of use, I usually test my changes in the browser first. Let's start with that annoying new button they added.

**Shift + Right Click on it** and then click **Inspect** 

![](3.png?lightbox)


The inspector can be overwhelming at first, but what we want to do is click around the html near where the inspector opened until we find something that seems to select as much as the element we want to block (generally a div, span, or button) as possible. We then look over to the style editor, and look for one *CSS Class* comes up earliest (ignore *element: {}*, it's useful a lot of stuff, but not what we're doing right now). If you lose where you are, you can use the element picker button on the top left of the inspector to point to the element you want to see.

![](4.png?lightbox)

**.channelAppLauncher_df39bd** seems good, and the big yellow box shows us the margin. This is important because when an object is taking up so much space, we want to make sure we get that space back.

I add *display: none;* to the CSS and... poof. That easy.

![](5.png?lightbox)


### Okay it's not that easy

First thing we need to do is copy all that into out **tweaks.css**(or the CSS editor of whatever mod you're using). All you should have to do is save the file and the results should appear in your client

```css
.channelAppLauncher_df39bd {
  margin-left: var(--spacing-16);
  margin-bottom: 24px;
  align-content: flex-end;
  position: relative;
  display: none;
}
```

okay actually we don't need all that though. We then cut out everything else but what we actually changed.

```css
.channelAppLauncher_df39bd {
  display: none;
}
```

That said, you can use this to change other values. Say you want a button to look SMALLER or something. I can't give you a whole CSS tutorial, but you have a lot of options.

You can also skip this step. If you unlock this feature in discord, you can hit **CTRL+SHIFT+I** to bring up the inspector, make your changes and simply... leave them there. You'll have to redo it when you restart discord but hey, the price of doing this with a vanilla install.

Not all things clean up easily. If you try and say remove the sticker button (you can post stickers from the emote menu why is it there!!!), you'll notice that...

![](6.png?lightbox)


... Oh shit that was all the buttons. Selecting the PRECISE element of something can be hard sometimes. If you mess up so bad you can't tell what's going on, you can always refresh the browser and try again.

So what do we do for *these buttons*? I like using *aria labels*, little accessibility hooks that are useful for reliably identifying certain elements. Instead of random lines of numbers and letters, you get names that get used by things like screen readers. This has the added benefit that you rarely have to redo these changes as discord updates.

![](7.png?lightbox)


```css
button[aria-label="Send a gift"] { display: none; }
button[aria-label="Open GIF picker"] { display: none; }
button[aria-label="Open sticker picker"] { display: none; }
button[aria-label="Start an Activity"] { display: none; }
div[aria-label^="Add Super Reaction"] { display: none; }
```

These are the codes I use on my end to keep things clean, but you can remove ones you want to keep or even kill the emoji button if you want ("Select Emoji", if you so desire). An important part is you actually have to note what element the aria-label is in. Most of these are buttons, but Super Reaction, which appears in a different place, is a div. You just have to look at what the label is actually inside of. 

Also hilarious I realize they removed that button anyways and I know longer need that line, but it still illustrates an important point!

To show some other examples, I find the message hover effect to be distracting so I have...

```css
.theme-dark {
  --background-message-hover: rgba(255, 255, 255, 0.00) !important;
}
```

Which makes the darkening effect totally transparent, effectively hiding it. But also here is the **!important**. CSS stands for *cascading stylesheets* so if you have like....

```css
body{
  background-color: red;
}

body{
  background-color: white;
}
```

The background color will be white because the last thing takes priority. If a hover effect is added dynamically to an element, its priority might be beneath our attempts to remove it. **!important** tells the CSS to not let anything override this property. The only thing that will override it is another, lower **!important**. This can be an important(lol) too when CSS hacking.

**Edit:** Also going to point to [this comment](https://cohost.org/Kayin/post/7374027-using-css-to-make-di#comment-e6fa17bd-5091-454d-a743-3dc04bec862f) which links to an excellent list of possible element ids to use to customize stuff

Anyways if you came into this unfamiliar with CSS and the inspector, this is a lot to take in but it's VERY learnable. Play around, break stuff, set horrible colors, make a mess. Mess with other websites! Use UBlockOrigin and these principles to block every annoying Twitter change! Download... god what do people use now, TamperMonkey??? Enforce your will upon your computer!

CSS is punk, and we should all strive to be a little more punk.
