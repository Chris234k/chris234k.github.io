---
layout: game
title: Battery Boy
pitch: An endless runner that changes based on the battery life of your device
collection: games
thumbnail: assets/images/batteryboy/thumbnail.png
trailer: https://www.youtube.com/embed/qqFoSA4W-Ag
grid-rank: 4
published: true
---

## [Petricore](http://petricoregames.com/)'s Third Game
Battery boy is an endless runner that changes with the battery life of your device. Drag your finger to move your character horizontally. The speed at which the character moves will increase as your score gets higher. Avoid obstacles, use powerups, gather coins. Customize your character and get the highest score possible.

While releasing your finger to stop is an additional degree of freedom we have over many endless runners, the other gameplay mechanics are quite similar. However, no development process is ever the same. Let me take you on a small journey through Battery Boy's development!

... One last thing before we go: Petricore does not work on games full time. This timeline is filled with months (years?) of contract work. We've had months where we almost exclusively worked on Battery Boy, and months where no more than a few days were spent on it. Just something to keep in mind if you're trying to plan your own game timeline :).

---

### Rhythmic Roots -- August 2016
Game jams at Petricore happen irregularly, maybe once every few months. If something interesting comes out of one we'll discuss and explore the idea more. Inside the monolithic Google Drive folder structure Petricore calls home there lies a folder "19 Aug 2016 Game Jam" which contains some of the very first assets for Battery Boy. Here's one such asset:
<div class="aspectratio">
<img src="/assets/images/batteryboy/early-concept.jpg" class="demo-gif">
</div>
If you're familiar with the present state of the game, this might make a remarkable amount of sense to you. In this game jam we've already established: battery tiers with color, the rough look of the main character, and the computer parts / tech-y theme. However, the one major element not depicted here is rhythm.

At its conception, and through a lot of development, we thought Battery Boy would be a rhythm game with a cool twist: battery life.
<div class="aspectratio">
<img src="/assets/images/batteryboy/bfig-gameplay.gif" class="demo-gif">
</div>
You can't hear it (because the recording has no sound), but the movement of those green blocks is tied to the rhythm of the song.
At one point we even had [Wwise](https://www.audiokinetic.com/products/wwise/) integration with MIDI tracks. The player could unlock instruments to use in place of the default configuations. This idea may sound good, but it didn't result in very good sounding music. Plus, who keeps their sound on while playing mobile games?. I am not saying "don't make mobile rhythm games", there are plenty of examples to the contrary! Just that with our resources (we don't have an internal audio person) and objectives (making an endless runner) we were not able to pull it off. Your milage may vary :)

If you're thinking "Chris, how do those blocks even move with the rhythm?". Don't worry, many players asked us the same question. In the back of all our minds was the thought to remove rhythm entirely. The only thing stopping us was the amount of work we'd already put into it.

---

### Crazy Currencies -- February 2017
A little unsure what to do with rhythm, we explored other ways of using the battery life mechanic. We spoke with some local game developers at the [Indie Game Collective](http://www.indiegamecollective.org/). They echoed our concerns about having rhythm; they didn't know how it fit into the game either. One of the developers proposed creating a metagame around the battery life of the device; using it for progression instead of gameplay. This idea stuck. We already had battery life split into tiers: green, yellow, and red. Tiers correspond with percentage of battery remaining, i.e. battery life of 20% would be red. Each tier would gain a single type of currency you could only obtain by playing at that battery tier. These currencies would be used to purchase certain types of items, for example: some characters cost 400 green and 100 red, but 0 yellow.
<div>
<img src="/assets/images/batteryboy/bar.gif" class="demo-gif" style="max-width:150px">
</div>

Mobile games commonly have at least 2 types of currencies anyway: premium and in-game currency. Premium costs real money or ads to obtain. While "in-game" can come in many forms. For example, here's a walkthrough our artist, [Christina Andriano](https://twitter.com/mobstergoose), put together from [Animal Crossing: Pocket Camp](https://ac-pocketcamp.com/en-US/site).
<div class="aspectratio">
<img src="/assets/images/batteryboy/ac-pc.jpg" class="demo-gif">
</div>
This led us to something closer to a material crafting system, which is the category I'd put Animal Crossing: Pocket Camp into. Having something sufficiently interesting to replace it, it's at this point that we felt confident enough to ditch rhythm. 

... But I'm skipping a lot of details. Removing rhythm took significant time and was not something the team agreed upon all at once. Changing the soul of a game is very difficult on a small team, as we all had a hand in its design. Our lead designer, [Oliver Awat](https://twitter.com/oliverawat), led the charge. He proposed that we essentially go back to prototyping on the core gameplay. As part of that proposal, he created a small spreadsheet to give us a brief look at the impact the changes would have. The contents of that spreadsheet are in the following table (emphasis his):

| Changes                          | Gameplay Mechanics | Visual Changes | Meta  |
| -------------------------------- | :----------------: | :------------: | :---: |
| Scaling Difficulty (SR)          | X                  |                | X     |
| Multiple Lanes                   | X                  | X              |       |
| _More Coin Collection_           | X                  | X              |       |
| Daily Challenges                 | X                  |                | X     |
| *__<u>Time Pressure</u>__*       | X                  | X              |       |
| Power Ups                        | X                  |                |       |
| *__More control over movement__* | X                  |                |       |
| Circuit-based turning            | X                  | X              |       |
| Events                           |                    |                | X     |
| Always Moving **?**              | X                  | X              |       |

I believe the emphasis corresponds with the ideas he thought were most valuable, because those are the ones that made it into the game.

Removing rhythm meant changing the way the obstacles moved, which (in turn) meant changing how the player moved. With only a few attempts at building a new control scheme, we had a completely different game. We did not want to do the typical "3-lane" runner (think Subway Surfers), this led us to the freedom of dragging anywhere on the screen horizontally. What naturally followed was that, in some situations, it did not feel right to be constantly moving. Since the character could be anywhere horizontally, we gave players the ability to release their finger from the screen to stop---- giving them more time to react. This system felt immediately more fun and interesting than the old one, which was very slow and had an odd pacing to it. With the obstacles no longer moving to the beat, all we had left was the MIDI instruments. This is really the point at which we felt confident enough to remove rhythm; only after it stood alone, clearly marked as a relic of the past.

---

### Finalizing Ideas -- February 2017 to October 2017
(I'm out of alliterations for headings)

We tried to repurpose old ideas and create new ones around the core twist: device battery life changes the game. We settled on two primary implementations:
1. Currencies can only be obtained at certain battery tiers (green at high battery, etc)
2. Gameplay is harder at lower battery

Our previous games, [Mind the Arrow](/games/mindthearrow/) and [Gelato Flicker](/games/gelatoflicker/), lacked complexity within monetization. We wanted to try something more robust.
<div class="aspectratio">
<video autoplay muted loop src="/assets/images/batteryboy/shop.mp4"></video>
</div>
What we settled on was a shop. The shop contains:

- 10 characters
- 40 skins (4 unique to each character)
- 21 accesories (all characters can wear)
- 2 songs

The player picks a character and can customize them with one item from each type. In the above demo, you see me equip the: cube character, dice skin, and aviator accessory.

<br>
<br>

Powerups, powerups, powerups. Powerups? We ended up with----what I think----is a fairly standard set of powerups. We settled on three: boost, shield, and magnet. In Battery Boy, you cannot miss any of the powerups. They appear directly in your path and you're pretty much forced to get them. However, which powerup will appear is random. I personally spent a lot of time on the boost and magnet, trying to make them stand out from the rest of the game. You can (hopefully) guess how they work, but here are some demos anyway:
<div class="aspectratio">
<video autoplay muted loop src="/assets/images/batteryboy/powerup-boost.mp4"></video>
</div>
Hit a boost to fly through obstacles! -- The player loses control and flys rapidly through a number of obstacles, giving them a bunch of score. (I'm very proud of how the visuals came out on this one!)

<br>
<br>

<div class="aspectratio">
<video autoplay muted loop src="/assets/images/batteryboy/powerup-shield.mp4"></video>
</div>
Pickup a shield to take an extra hit! -- A hexagonal shield forms around the player, preventing them from taking any damage. Character begins to blink and then becomes vulernable again after hitting an obstacle.

<br>
<br>

<div class="aspectratio">
<video autoplay muted loop src="/assets/images/batteryboy/powerup-magnet.mp4"></video>
</div>
A magnet will pull nearby coins to you. Never miss another coin! -- This is only sort of true, you can actually still miss coins (whoops!). I personally think this is the weakest of the three powerups in terms of gameplay. Part of the way I tried to improve the game feel of the magnet was the animation for collecting a coin. It curves upwards towards its resting place in the UI.

<br>
<br>

When looking at monetization systems for other games, particularly [Crossy Road](http://www.crossyroad.com/) and [Sling Kong](http://protostargames.com/sling-kong/), we noticed that they commonly implement a lottery system to unlock cosmetic items. Crossy Road features an actual prize machine, while Sling Kong is closer to pachinko. We decided to make our version just a bit more skill based---- pinball!
<div class="aspectratio">
<video autoplay muted loop src="/assets/images/batteryboy/pinball.mp4"></video>
</div>
When making a minigame, I always have this concern: it is just _another_ set of mechanics for players to bounce off of. Thankfully, pinball seems common or intuitive enough for most people to understand how it works. We deliberately tried to keep it to a "one touch" style of game. But don't misunderstand me, we still had to do several iterations on the tutorial for pinball alone. At some point in development, we decided to split pinball into 3 different cases: green, yellow, and red. The color of the case corresponds to which type of currency you pay to play it.

<br>
<br>

The success of rewarded video ads in Gelato Flicker led us to bring it into Battery Boy as well. The system is fairly simple to implement, and is very effective. In Gelato Flicker, we saw about 30% of all games played converting to revive ads.
<div class="aspectratio">
<video autoplay muted loop src="/assets/images/batteryboy/ad-prompt.mp4"></video>
</div>
Offer the user an ad to revive and continue playing. Works great when score is something the player cares about. Supporting this idea, is that you're able to connect to Facebook and see your friends' scores as you pass them.

---

### Publishing Potential -- March 2017
(I lied, I found one more alliteration)

The publishing deal had ended with our previous partner. Maybe halfway through development we set out to work with another publisher. Our CEO, [Ryan Canuel](https://twitter.com/RyanCanuel), attended [GDC 2017](http://www.gdconf.com/) and presented Battery Boy at [The Big Indie Pitch](http://www.bigindiepitch.com/past-events/). It was there that we first came in contact with [iDreamSky](https://www.idreamsky.com/en). iDreamSky only has publishing interests in China, so we thought it could be a cool opportunity to localize our work and reach a new market.

A brief publishing timeline (all dates in 2017):
- March 2 - The Big Indie Pitch
- March 6 - First build sent to iDreamSky
- March 16 - iDreamSky expresses interest in working with us
- May 19 - Begin discussing release plans
- June 10 - Monetization, design feedback, SDK integration, localization, bugs, etc (the meat of dev time)
- September 9 - Marketing assets, bugs
- September 28 - Trailer complete (by [Sarah Spiers](https://twitter.com/sspiers_k) & [Renzo Heredia](https://twitter.com/RenzoGHeredia))
- October 30 - Chinese Release
- November 3 - "Best New Games" feature by Apple
 
That puts us at just about 8 months of time between first contact and Chinese release. It is at this point that I want to mention again, that we do not work on games full time a Petricore. The work here is less than 2 months of dev hours. We were working on a number of work for hire projects at the same time, the summer was quite busy for us!

---

### A Tiny Postmortem -- April 2018
- Battery Boy stands as a solid and varied take on an endless runner. Which is increasingly more difficult to do, given the saturation of the genre.
- I wish we'd gone further with the "currencies as materials" concept. The current system strikes me as an awkward halfway point that comes with more confusion than either extreme.
- Difficulty increasing with lower battery is too subtle. I worry many players don't notice it. Doesn't mean the game needs to be harder, just that the visual effect should be more pronounced.
- Being able to connect to Facebook and get rewarded for beating your friends scores is seriously cool. Worth exploring in other games. Works especially well because you move past your friends' high scores; might be difficult to implement in more abstract scoring games.
- We're at least partially guilty of the [second-system effect](https://en.wikipedia.org/wiki/Second-system_effect) on the shop. Just because we could build a shop doesn't mean we should have. Basically, time would have been better spent making the battery life more pronounced.
- Two major holiday updates were planned to shortly follow the release: Halloween and Christmas. Neither update occurred. A non-trivial amount of work was put into these: 3d models for accesories, skins for many characters, etc. Not much to say, it just sucks.
