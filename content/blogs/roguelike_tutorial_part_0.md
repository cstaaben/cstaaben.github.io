---
title: "Roguelike Tutorial - The beginning… and the end?"
date: 2023-02-05T01:26:25-08:00
draft: false
tags: [”roguelike”, “tutorial”, “go”, “python”, “series”,”erebor”]
categories: [”Series”, “Roguelike”,”Erebor”]
disqus_title: roguelike_tutorial_part_0
---

## Inspiration

I’ve always had an interest in text-based games. It’s always felt like these
games needed to be much more engaging than their graphically-gifted counterparts
because there were fewer pretty things to look at. They had to engage your
imagination, or at least your interest, to such an extent that you would
continue to play. It originally started when I was learning that I was good at
writing (for a small town high school student), and only grew the more I started
using, and learning about, computers. Initially, it was just those text-based
adventures that described the scene in the room you were in and presented you
with a list of options. Then, I discovered roguelikes. These were the some of
the most challenging and captivating games I had played and despite how
frustrated they would make me, I kept coming back. Life forced me to put things
on the back-burner for quite a while but now, secure enough in my career to
start prioritizing my own health and family over work, I am drawn back to this
genre with an experienced developer’s cant. These are new problems that I’ve not
had to solve and while they may not be terribly complex, they are new and
intriguing in that they are a definitive shift away from what I have to solve in
my day-to-day.

## Plotting the course

In an evening of perusing the web for information about procedurally generated
mazes and the various algorithms to find the route through said mazes, I
stumbled upon [RogueBasin](http://www.roguebasin.com/index.php/Main_Page) and
while reading through their articles on some of the major roguelikes, I
discovered a series of
articles: [Roguelike Tutorials](http://rogueliketutorials.com/). I will be
loosely following this series and doing my best to convert the Python to Go.
I’ve
found [https://github.com/Joakker/tcod-go](https://github.com/Joakker/tcod-go),
“a wrapper of the libtcod library,” which I hope will be enough. Who knows,
maybe I’ll go down the rabbit hole of porting some of the tools from libtcod
into Go as part of this series, or a follow-up series.

A quick note before we dive in: the code for this project in its current state
can be found
here: [https://github.com/cstaaben/erebor](https://github.com/cstaaben/erebor)

I decided to call my game Erebor, based on the dwarven mountain/fortress/city
from J.R.R. Tolkien’s “The Hobbit.” Moria really seemed fascinating, and Angband
was already taken. Hopefully no fans of his work are going to metaphorically
crucify me for using The Lonely Mountain as my setting!

## My first lesson

Now, obviously, I wrote the above sections prior to actually starting the work.
But I didn’t feel they constituted a worthy introduction post and, at the time,
I didn’t have much to add to flesh it out. My thought was to take notes and
write this post as I developed the game. That approach lasted all the way until
the end of the first section for the roguelike tutorial.

At first, I had some normal struggles: installing libtcod and SDL2 on a MacBook
Pro with an M1 Pro chip was a series of failed experiments until I built them
from source, getting pkg-config to look in the right place to find those
packages, translating the Python code and libtcod API calls into the Go library
equivalents, and following a basic tutorial while organizing the code to allow
me to build upon it without crazy amounts of refactoring in the future. But when
I reached the first real functionality of the game (moving the character around
the screen), the weaknesses it the library become very apparent. I'm not sure
what version of libtcod it was last compiled with and what’s changed since but
given the lack of updates to that library, I can only assume they did not stay
abreast of those changes. Unfortunately, updating what appears to be a mostly
abandoned library does not fall under the umbrella of this series (nor do I have
the desire to learn that particular curve at this moment, sadly).

After some research, I’ve found recommendations to use other terminal libraries,
or terminal emulators, written in pure Go or supporting Go bindings. I also did
some further digging into the roguelike “genre” (I use that term very loosely
here) and development process and realized something pretty major. I don’t want
to just follow a tutorial and make something that tons of other people are
cranking out. I want to make something new. It doesn’t have to be good or
exciting or popular. But I want it to be new, and I want to do it right. I'm
still set on doing it in Go, but I’m more than likely going to be writing my own
generation, pathfinding, and FOV algorithms. It’s a bit more than I initially
expected to undertake but I’m ok with that. I’ll still follow the tutorial but
only as a checklist, really, to ensure I spend time creating all the same things
I would have if I used the libtcod library.

This series may stretch much longer now and it may take me a long time to
finish. But I’m going to stick with it until I can release a finished product.
I’m not going to guarantee that each post between now and that future completion
date will be about Erebor because I’ve got a marriage to maintain, and two kids
to raise. Sometimes, I won’t have a lot of time to dedicate to the project. But
I will continue to chip away at it in whatever way I can and post meaningful
updates as I do.
