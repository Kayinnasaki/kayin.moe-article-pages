---
title: 'Quality of Life'
date: '18-01-2025'
publish_date: '18-01-2025'
comments: 3lfzcugjdtk2u
taxonomy:
  category:
    - Blog
  tag:
    - 'Game Design'
    - Games
---

I try not to argue *exact language* much. I try to keep my approach to language as a descriptivist. Language evolves in terrible and funny ways. *Metroidvania* is an awful term, but it's a term with history I will use long before I use the term *Search Action*(a genre name that has the same appeal as calling hotdogs *Intestined Scraps*). Sure, some phrases like [Backtracking](../backtracking/) are too misguided for me to tolerate, but **Quality-of-Life** isn't like that. So called *QoL changes* can mean a lot of of things to a lot of people, but I'm going to talk about *a* way I see it used a lot. [tool tip="The usages I get exposed to are surely extremely biased"]Maybe the most common way[/tool].

We often treat Quality-of-Life changes like freebies. Changes that are *only* an improvement. Changes that don't change the *actual game* (the definition of 'actual' will vary wildly depending on who you ask). Changes that just make things *nicer*, more enjoyable, smoother. Changes that simply add up over time to make something a *better game*. Less menuing, automating repetitive tasks, smoothing out randomness... generally just adding consistency where the controls, UI, or meta-systems are fighting you. They just make things better, right?

# There are no free lunches

Here is the point where I am tempted to say something catchy like *"there is no such thing as a Quality-of-Life change"*. Unfortunately, that's a bit too reductive. Instead I will say: 

If you're a designer, you should **pretend** that there is no such thing as a Quality-of-Life change. 

... Because for every change that *might* actually be a strict improvement, 10 changes happen with consequences that went unconsidered. That doesn't make these changes even necessarily a net negative, but it's important we at least know what is happening in our game! If a change seems so obviously good, we should at least be a little suspicious, and ask why we didn't do it that way to begin with!

I feel like the consequences of supposed "QoL" changes are most obvious in competitive games, so lets start there. When [input buffers](https://glossary.infil.net/?t=Buffer) got introduced to 2D Fighting Games, many argued they would just let players *get to the real game* faster, and that is true..[tool tip="There is no such thing s as the 'real game'"]ish[/tool].

... But they also changed the games, fundamentally. They changed what was rewarded. The modern way we talk about frame data falls out of this changes. Some people think the focus on frame data is simply *because we know better now*, but when we bring modern players and mentalities to old games, they don't [tool tip="Though new players DO figure out some cool new shit"]change the fundamental nature[/tool] of the games.

Being assured of a first-possible-frame input for any normal fundamentally changes the risk reward of pressure. Removing things like variable wake-up timing *strengthens* [okizeme](https://glossary.infil.net/?t=Okizeme) and [setplay](https://glossary.infil.net/?t=Set%20Play). It increases the necessity to be *optimal* rather than *improvisational* because optimal is now *realistically achievable*.

Starcraft had a similar arc going into Starcraft 2. Larger control groups, auto-mining workers, better path finding... hell, even changing how many workers you start with all seem like obvious positive "Quality of Life" changes. Yet it quickly became obvious that these changes lead to a fundamentally different game. [tool tip="This is apparently still true to some extent, but I am less familiar with modern SC2"]Early on[/tool], the so called "Ball of Death" became the end game strategy, easily controlling giant armies, all bound to one control group. While the game had plenty of room for skill and strategy, *tactics* took a deep hit, and years of patching later the game is still found lacking in those departments compared to Brood War.

The changes made to SC2 or modern fighting games weren't bad ones. In many ways they were necessary ones for the future of both genres... but neither genre really fully came to grips with what those "Quality of Life" changes were really doing to their games. They tried to adjust, but never nearly enough. SC2 tries to add little bits of optional micro to tons of units, but none of that strains people to the point where *shit can just go wrong*. SC:BW professional games, even at the *highest* level, are filled with mistakes at every moment. Commanding an army is hard and SC1 captures that struggle on all levels of play.

Some modern fighting games try to address these issues, but can't compare to the chaos of old fighting games, which are messy enough to have drops on simple BnBs, weird scrambles, and a degree of instability that has to be strategically planned around. Extremely new games like SF6 try to add new complicating elements like [tool tip="... 'Just frame', but it's like a 3-5 frame window"]Just Frame[/tool] bonus tricks to try and add difficulty, while also trying to move a lot of the "combo skill" into situational resource awareness. These are [tool tip="Resource management is my favorite part of SF6"]neat ideas[/tool], but ones that came almost a decade late. Nothing has even come close to mixing up the rigid situations that arise from modern frame data, which often feel less like a fight and more like strategic stock investments.

Single Player games seem like they'd get a free pass, but even small changes can encourage unfortunate player behavior. A classic is how old school PC saving worked. Quick Saves and Loads subtly encourage save scumming, tedious encounter optimizations and players being extremely greedy. You could resist this temptation, but the line between "quick saves" and "using the autosaves between levels" a jump in difficulty that tempts many enough for them to give in. It took the modern, perpetual save systems to eventually course correct, letting people *relax a little*. You want just enough control and convenience that the player becomes okay with failure.

Often when modernizing old games there is a temptation to remove "outdated" design models... Item pickup weight limits, or a lack of auto-map or whatever. Yet the tension of playing Demon's Souls and not having enough item load to carry an item out of a level was, good or bad, *an experience*. In games without any kind of limit, people just compulsively pick up everything and horde. Is this the behavior you want? *Maybe*. I don't know if I wish I had pickup limits in Elden Ring, but I sure thought about my inventory a whole lot less.

Things go even farther to systems like auto loot-processing where the question begins to become *why*? Why are we optimizing mechanics to the point they're [tool tip="I hear this is what the history of Monster Hunter is like, but having not played any I don't feel comfortable ACTUALLY writing about it"]basically gone from the game[/tool]? Things stop being about "Quality of Life" and become questions of genuine design goals. What's the point of intentionally introducing complications only to eventually sand over? We get modern metroidvanias with color coded blocks, and color coded attacks, with color coded map icons because of "QoL"... but then all we do is reduce games to a check list. Have we just [replaced the fantasy of exploration with busywork](../the-mechanics-of-a-metroidvania-are-tools-not-the-destination/)? Is this really a higher *Quality-of-Life*?

Our job is to make problems for the player to solve, not make problems and then immediately solve them for ourselves. If we have desire to do that, then *the initial problem probably shouldn't exist at all*... Probably.

Even button-press reducing changes can introduce undesirable behavior. Do you *want* the player to be swapping their class or equipment around all the time, for every encounter, now that you've made it easier to do so? Maybe! But that isn't *Quality of Life*, that is, again, a genuine *design question*. If you don't want them switching around so wildly, what's a more pleasant way than crummy UI to stop them? Does including a quick restart in your roguelike encourage restart-scumming? What are they looking for? Can you minimize whatever variance they're looking for to discourage this behavior?

So I'm not going to sit here and say "Don't say Quality of life!" like I will with [tool tip="No, for real, it's a fucking useless, meaningless term 99% of the time"]"backtracking"[/tool]... but instead look at QoL problems like any other. What is your change encouraging, and what is it discouraging? Were there any positives, even if unintended, from the old behavior? How could that be preserved? If it can't be, is the sacrifice worth it? Or, to a bigger extreme, if it might not be worth it, has your change gone far enough? Maybe you don't need to preserve what you had, maybe you need to *obliterate it* with a new, powerful idea. Not a QoL change. Real change.
