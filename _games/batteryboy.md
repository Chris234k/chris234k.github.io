---
layout: game
title: Battery Boy
pitch: An endless runner that changes based on the battery life of your device
collection: games
thumbnail: assets/images/batteryboy/thumbnail.png
trailer: https://www.youtube.com/embed/qqFoSA4W-Ag
grid-rank: 0
published: false
---

## [Petricore](http://petricoregames.com/)'s Third Game
The publishing deal had ended with our previous partner. Maybe halfway through development we set out to work with another publisher. One of us met with [iDreamSky](http://www.idreamsky.com/en) at [GDC](http://www.gdconf.com/), and the rest is history. iDreamSky only has publishing interests in China, so we thought it could be a cool opportunity to localize our work and reach a new market.

[GIF - GAMEPLAY, IS THE TRAILER ABOVE ENOUGH?]
Battery boy is an endless runner that changes with the battery life of your device. Drag your finger to move your character horizontally. The speed at which the character moves will increase as your score gets higher. Avoid obstacles and---- you've probably heard this one before. While dragging to move is an additional degree of freedom we have over many endless runners, the other gameplay mechanics are quite similar. Let me take you on a small journey through Battery Boy's development!

---

### Rhythmic Roots -- August 2016
The way we usually decide what games to work on is just by having game jams. These happen irregularly, maybe once every few months. If something interesting comes out of one we'll discuss and explore the idea more. Inside the monolithic Google Drive folder structure Petricore calls home there lies a folder "19 Aug 2016 Game Jam" which contains some of the very first assets for Battery Boy. Here's one such asset:
<div class="aspectratio">
<img src="/assets/images/batteryboy/early-concept.jpg" class="demo-gif">
</div>
If you're familiar with the game now, this might make a remarkable amount of sense to you. In this game jam we've already established: battery tiers with color, the rough look of the main character, and the computer parts / tech-y theme. However, the one major element not depicted here is rhythm.

At its conception, and through a lot of development, we thought Battery Boy would be a rhythm game with a cool twist: battery life.
<div class="aspectratio">
<img src="/assets/images/batteryboy/bfig-gameplay.gif" class="demo-gif">
</div>
You can't hear it (because the recording has no sound), but the movement of those green blocks is tied to the rhythm of the song. 
[WIP -- EXPLANATION OF RHYTHM]
At one point we even had [WWise](https://www.audiokinetic.com/products/wwise/) integration with MIDI tracks. The player could unlock instruments to use in place of the default configuations. This idea may sound good, but it didn't result in very good sounding music. Plus, of all platforms, mobile is probably the one you're least likely to have your game sound on.

If this description isn't clear, or maybe just doesn't sound that great, don't worry. Most people just weren't getting it, and with a closer look, we weren't really either. In the back of all our minds was the thought to remove rhythm entirely. The only thing stopping us was the amount of work we'd already put into it.

---

### Crazy Currencies -- February 2017
A little unsure what to do with rhythm, we explored other ways of using the battery life mechanic. We spoke with some local game developers at the [Indie Game Collective](http://www.indiegamecollective.org/). They echoed our concerns about having rhythm; they didn't know how it fit into the game either. One of the developers proposed creating a meta game around the battery life of the device; using it for progression instead of gameplay. This idea stuck. We already had battery life split into tiers: green, yellow, and red. Tiers correspond with percentage of battery remaining, i.e. less than 33% would be red. Each tier would gain a single type of currency you could only obtain by playing at that battery tier. These currencies would be used to purchase certain types of items, for example: some characters cost 400 green and 100 red, but 0 yellow.
<div>
<img src="/assets/images/batteryboy/bar.gif" class="demo-gif" style="max-width:150px">
</div>

Mobile games commonly have at least 2 types of currencies anyway: premium and in-game currency. Premium costs real money or ads to obtain. While "in-game" can come in many forms [FIRE EMBLEM] [ANIMAL CROSSING]. This led us to something closer to a material crafting system. Which is how I'd classify both of those games [BOTH IMPLIES ABOVE GAMES]. Having something sufficiently interesting to replace it, it's at this point that we felt confident enough to ditch rhythm.

---

### Finalizing Ideas -- From February 2017 to October 2017
(I'm out of alliterations for headings)

We tried to repurpose old ideas and create new ones around the core twist: device battery life changes the game. We settled on two primary implementations:
1. Gameplay is harder at lower battery
2. Currency can only be obtained at certain battery tiers
[WELL HOW IS THE GAMEPLAY HARDER, HUH?]
[WHAT EVEN ARE CURRENCIES?]

Our previous games, [Mind the Arrow](/games/mindthearrow/) and [Gelato Flicker](/games/gelatoflicker/), lacked complexity within monetization. We wanted to try something more robust.
<div class="aspectratio">
<video autoplay loop src="/assets/images/batteryboy/shop.mp4"></video>
</div>
[SHOP EXPLANO] x characters, x skins, x accessories, x songs

[TODO: WHY ARE ALL VIDEOS CENTERED HORIZONTALLY]
[CONSIDER TURNING THESE INTO A SINGLE VIDEO WITH 3 PARTS]
<div class="aspectratio">
<video autoplay loop src="/assets/images/batteryboy/powerup-boost.mp4"></video>
<video autoplay loop src="/assets/images/batteryboy/powerup-shield.mp4"></video>
<video autoplay loop src="/assets/images/batteryboy/powerup-magnet.mp4"></video>
</div>
[POWERUP EXPLANO]

When looking at monetization systems for other games, particularly [Crossy Road](http://www.crossyroad.com/) and [Sling Kong](http://protostargames.com/sling-kong/), we noticed that they commonly implement a lottery system to unlock cosmetic items. Crossy Road features an actual prize machine, while Sling Kong is closer to pachinko. We decided to make our version just a bit more skill based---- pinball!
<div class="aspectratio">
<video autoplay loop src="/assets/images/batteryboy/pinball.mp4"></video>
</div>
When making a minigame, I always have this concern: it is just _another_ set of mechanics for players to bounce off of. Thankfully, pinball seems common or intuitive enough for most people to understand how it works. We deliberately tried to keep it to a "one touch" style of game. But don't misunderstand me, we still had to do several iterations on the tutorial for pinball alone. At some point in development, we decided to split pinball into 3 different cases: green, yellow, and red. The color of the case corresponds to which type of currency you pay to play it.

The success of rewarded video ads in Gelato Flicker led us to bring it into Battery Boy as well. The system is fairly simple to implement, and is very effective. In Gelato Flicker, we saw about 30% of all games played converting to revive ads.
<div class="aspectratio">
<video autoplay loop src="/assets/images/batteryboy/ad-prompt.mp4"></video>
</div>
Offer the user an ad to revive and continue playing. Works great when score is something the player cares about. Supporting this idea, is that you're able to connect to Facebook and see your friends' scores as you pass them.

[FACEBOOK HIGH SCORES?]

---

### Chinese Release -- October 2017
[THE STATE THE GAME WAS IN AT RELEASE]
[LITTLE BIT OF DATA]
[TALK ABOUT THE UPDATES?]
[STILL NOT FULLY RELEASED]

---

### A Tiny Postmortem -- March 2018
- Battery Boy stands as a solid and varied take on an endless runner. Which is increasingly more difficult to do, given the saturation of the genre.
- I wish we'd gone further with the "currencies as materials" concept. The current system strikes me as an awkward halfway point that comes with more confusion than either extreme.
- Difficulty increasing with lower battery is too subtle. I worry many players don't notice it. Doesn't mean the game needs to be harder, just that the visual effect should be more pronounced.
- Being able to connect to Facebook and get rewarded for beating your friends scores is seriously cool. Worth exploring in other games. Works especially well because you move past your friends' high scores; might be difficult to implement in more abstract scoring games.
- We're at least partially guilty of the [second-system effect](https://en.wikipedia.org/wiki/Second-system_effect) on the shop. Just because we could build a shop doesn't mean we should have. Basically, time would have been better spent making the battery life more pronounced.
- Two major holiday updates were planned to shortly follow the release: Halloween and Christmas. Neither update occurred. A non-trivial amount of work was put into these: 3d models for accesories, skins for many characters, etc. Not much to say, it just sucks.
