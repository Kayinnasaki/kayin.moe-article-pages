---
title: 'Kayin Works'
process:
    markdown: true
    twig: true
visible: false
nodate: 1
header_image: '../header.webp'
header_class: frontheader
minheader_image: 'default'
---

<div markdown="1" style="margin-top:-50px">
[splitbox side="right"]
<div class="frontside" markdown="1">
### Recent Writing

{% include 'partials/recent.html.twig' with { 'taxonomy_type': 'category', 'taxonomy_': 'Blog', 'limit': 5 } %}
</div>
++++
<br>
<div style="display:flex" markdown="1">
<div class="frontavatardiv"><img class="frontavatar" src="/etc/icons/kayin.png"></div>
<div markdown="1">Hey! I'm **Kayin**, the Indie Game Developer who created [*I Wanna be the Guy*](https://iwbtg.kayin.moe), and [*I Wanna be the Guy: Gaiden*](https://kayin.itch.io/iwbtgg). I'm [tool tip="That's a lie"]currently working[/tool] on [*Brave Earth: Prologue*](/../brave-earth).</div>
</div>
If you want to know more about me, personally, you can check out my [About Page](/../about) or follow me on social media!

If you're interested in my thoughts on game design and other topics, please feel to read through [My Writing](/../posts). If you're not sure what to read, you could try...

* [Reaction Speeds in Gaming](/../reactions)
* [Metroid: Dread - How Metroid Lost its Way](/../metroid-dread)
* [Dragon's Dogma wants you to Choose](/../dragons-dogma-wants-you-to-choose)

You can also use the [Site Map](/../other-projects/sitemap) or my [Cohost Archive](/../cohost) to find more things to read!

Feel free to explore the site, and if you want, **hit the toggle on the red bar just under the logo** on the sidebar to toggle between **Dark** <span markdown="1" onclick="
        document.getElementById('656ce704adc484ac544535745594cbc1').togglePopover();
        neo();"
    class="tooltip" title="AND a secret theme...">and<span markdown="1" id="656ce704adc484ac544535745594cbc1" class="tiptext" popover="auto"><em>(AND a secret theme...)</em></span></span> **Light mode**!

[/splitbox]

!!! **07/11/2024** Recently Updates the themes to ones I've been tested. The old ones are still around, if you can find them! Feel free to send feedback to any of the usual places.

[center]
# Friends of the Site
[/center]

<div class="linkbox">
    <a href="https://zaratustra.itch.io/"><div style="background: url(links/zara.png); background-repeat: no-repeat;" class="box8831">Zaratustra Productions</div></a>
    <a href="https://surasshu.com/"><img class="img8831" src="links/surasshu.gif"></a>
    <a href="https://sylvie.website/"><div style="background: url(links/sylvie.png)" class="box8831">Sylvie Games</div></a>
    <a href="https://aria.garden/"><div style="background: url(links/aria.png)" class="box8831">Aria's Garden</div></a>
</div>
<div class="linkbox">
    <a href="https://blog.aurahack.jp/"><img class="img8831" src="links/aurahack.gif"></a>
    <a href="https://doodlemancy.com/"><img class="img8831" src="links/doodlemancy.png"></a>
    <a href="https://itsmelilyv.com/"><img class="img8831" src="https://itsmelilyv.com/assets/site_image/itsmelilyv_88x31.gif"></a>
    <a href="https://automatictiger.neocities.org/"><img class="img8831" src="https://automatictiger.neocities.org/images/AstreaLinkButton.png"></a>
</div>
[center]
### Link to my blog!
<div class="linkbox">
    <img class="img8831" src="links/iwasoncohost.gif">
    <img class="img8831" src="links/kayinworks.gif">
    <img class="img8831" src="links/debian.gif">
</div>
<textarea name="buttoncode" class="center" aria-label="Button code" style="color: #292929; resize: none;margin-top: 0px; font-size: 0.7rem; width: 168px; height: 40px; margin-bottom: 0.5rem;"><a href="https://kayin.moe"><img src="https://kayin.moe/links/kayinworks.gif"></a></textarea>
[/center]
</div>

<style>
    :root {
    --color-titlenubs: #a6222a;
    }

    html[data-theme="light"] {
    --color-bg: whitesmoke;
    --color-text: #1f1f1f;
    --color-title: #000000;
    --color-subhead: #7e0000;
    --color-link: #1579c7;
    --color-noticebg: #f4f8fa;
    --color-scroll: initial;
    --color-scroll2: initial;   
    }

    html[data-theme="neodark"] {
    --color-titlenubs: #ca2630;  
    }

    html[data-theme="neolight"] {
    --color-titlenubs: #ca2630;  
    }
    
    .img8831 {
        width:176px;
        height:62px;
        image-rendering: pixelated;
    }

    .box8831 {
        zoom: 2;
    }

    .box8831>span {
        filter: drop-shadow(1px 1px black);
    }

    .frontheader {
        mask-image: var(--front-gradiant);
        mask-image: linear-gradient(0deg, rgba(2,0,36,0) 0%, rgba(0,0,0,1) 10%, rgba(0,0,0,1) 100%) !important;
        height: 30em;
        padding-top: -10px;
        image-rendering: pixelated;
    }

    .frontheader[data-theme="light"] {
        mask-image: linear-gradient(0deg, rgba(2,0,36,0) 0%, rgba(0,0,0,1) 10%, rgba(0,0,0,1) 100%) !important;
    }

    .frontheader h2 {
        padding-top: 189px;
        font-size: 8em;
        color: #fff;
        font-family: Bitfont;
        word-spacing: -73px;
        filter: hue-rotate(var(--hue-rotate));
    }

    .frontheader h2::before {
        content: "[";
        color: var(--color-titlenubs); /* Make the opening bracket red */
    }

    .frontheader h2::after {
        content: "]";
        color: var(--color-titlenubs); /* Make the opening bracket red */
    }

    .frontside {
        width: 100%;
        display: block;
        text-align: left;
    }

    .frontavatar {
        float: left;
        border-radius: 5em;
        height: 110px;
        border-width: 3px;
        border-style: solid;
        margin: -11px 11px 10px 0px;
        filter: drop-shadow(5px 5px 5px #000A);
    }

    .frontavatardiv {
        min-width: 130px; 
    }

    @media (max-width:1199px) {
        .frontavatar {
            width: 65px;
            height: 65px;
            margin-top: 0px;
        }

        .frontavatardiv {
            min-width: 90px; 
        }
    }
</style>