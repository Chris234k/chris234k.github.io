---
layout: game
title: "Detroit Zoo: Postcard Pledge"
pitch: Pledge to improve yourself and the environment
collection: interactives
thumbnail: assets/images/interactives/dz.jpg
demo-gif: /assets/images/interactives/dz-demo.gif
published: true
--- 
## [Detroit Zoo](https://detroitzoo.org/)

Objectives:
- Highlight an issue: we can all help the environment
- Sense of community: you are not alone

These objectives split the interactive into two separate applications: Pledge and Display.

### Pledge -- Highlighting the Issue
The user can select from 4 main categories: resources, food, travel, and trash.
<div class="aspectratio">
<img src="/assets/images/interactives/dz.jpg" class="demo-gif">
</div>

Each category contains 4 subcategories. For example, travel contains: carpooling, community bike paths, avoiding car idling, and vehicle emissions. Each subcategory comes with a description, giving the user more information about how to act on their pledge.

After the user has selected a category and a subcategory, they begin to create their postcard:
1. Add your name
2. Choose a background (select from various pictures of Antarctica)
3. Take a picture of yourself (using a webcam)
4. Email it (enter your email)

We then send the personalized postcard to the appropriate email address. This literally gives the user something to take home with them, a gentle reminder of their pledge to help the environment. We send the key aspects of their pledge (name, category, and subcategory) over to the display applcation.

### Display -- Sense of Community
Here's an example of what would be shown if I pledged to "Use Renewable Energy Sources".
<div class="aspectratio">
<img src="/assets/images/interactives/dz-monitor.gif" class="demo-gif">
</div>

I was tasked with making the two applications communicate. The client, [Boston Productions](http://www.bostonproductions.com/), provided roughly the following objectives:
- See what others' have pledged
- Reset data on a regular or user controlled basis
- Communicate with numerous Pledge stations

The first two objectives are part of the same solution: store information in a file on the computer. Just keep a tally for each type of pledge. If they want to reset it, all they need to do is set the count to 0 in the file. All other information is discarded.

That third objective mandates some form of local communication. After a bit of experimenting with C#'s [Sockets](https://msdn.microsoft.com/en-us/library/system.net.sockets.socket(v=vs.110).aspx), I learned of Unity's [NetworkDiscovery](https://docs.unity3d.com/ScriptReference/Networking.NetworkDiscovery.html). The description of which is:

> ... allows Unity games to find each other on a local network. It can broadcast presence and listen for broadcasts ...

NetworkDiscovery turned out to be a great fit. The end result is a very simple client-server model. The Display application broadcasts regularly so that any number of Pledge applications can find it. Once a connection is established, the process is fairly straightforward. Pledge applications will send information about which pledges have been completed, and the Display will keep count and show a visual for each pledge.