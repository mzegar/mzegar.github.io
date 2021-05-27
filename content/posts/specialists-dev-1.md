+++
author = "Matthew Zegar"
title = "The Specialists Reloaded"
date = "2021-05-26"
description = "talkin' specialists"
tags = [
    "Specialists",
    "s&box"
]
+++

I've had access to s&box for a little bit... here are my thoughts on s&box, alongside a showcase of what I've been
working on.

##### "The Specialists Reloaded"

The first time I ever played the Half-Life 1 mod "The Specialists", I was extremely surprised how much it overhauled the
base Half-Life experience. It had it all: fast movement, bullet-time, and source-like gun play. So this is exactly what I'm
going to be bringing to s&box.

Here are a few quick gifs of some movement mechanics I've managed to bring over from the original mod...


Backflipping off walls
![walljump](/images/specialists-dev-1/1.gif)

Dive into prone
![dive](/images/specialists-dev-1/2.gif)

##### S&box Thoughts

S&box is going to be a game changer. Here's a quick summary of why I think so...
- The developer experience is really really nice
  - Hot reloadable C# code
  - C# provides IDE auto complete and auto formatting
- Valve's updated tools are extremely well done and easy to pickup
  - Modeldoc, Hammer, etc.
- Source 2 as a base
  - It's freaking Source 2!!
    
However, I am a bit scared with one design choice that may lead to quite a few problems in the future. Inheritance hell.
Almost every single class you'll be creating will extend some class that extends another class that extends another class that...
you get the point. An example would be the movement code I've written so far for my mod. This movement class is "forced" to
extend from a bunch of classes.

```
ReloadedMovementController -> WalkController -> BasePlayerController -> PawnController
```

This is definitely a deliberate choice made by the folks over at FacePunch, as they clearly have experience with engines that
mostly minimize this issue such as Unity. It'll be interesting to see how it pans out. Regardless, I'm probably out of my lane
right now (as I'm just a uni student with a few months of internship experience using Unity).

##### What's next?

I'm waiting for goldsrc importing to be implemented as I'm going to be using the original "The Specialists" models initially.
