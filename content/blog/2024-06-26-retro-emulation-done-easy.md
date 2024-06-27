---
title: Retro emulation done easy
description: Consider a mini PC for your retro gaming needs
date: 2024-06-26
tags:
  - longform
  - video games
  - retro
  - emulation
---

After a year enjoying the comfort of playing old games on my TV, I can fully recommend my retro gaming setup: a mini PC running Batocera Linux.

---

For a long time I've been using a Raspberry Pi 3 running [RetroPie](https://retropie.org.uk/), and it certainly got the job done on anything less powerful than the N64. But over time I was dealing with a lot of *little* annoyances to this setup that just accumulated over the years.

A lot of it just came down to the defaults. **I don't like Retropie's default settings.** Whenever I messed up a config or an update did something unexpected, I would end up needing to reinstall Retropie and go through the process of changing all the configurations back the way I needed to fit my needs. This meant an hour+ of setting up networking settings, finicky controller pairings, Retroarch configs and more.

Eventually, I moved over to [Batocera](https://batocera.org/). *Everything just works*, straight from the Linux image. If you have a semi-popular controller to use with it, chances are it'll just work correctly once you plug it in or set the controller to Bluetooth pairing mode. PS4 controller? That touch pad area is automatically configured to be a mouse or cursor depending on the system! If you don't want to mess with options and menus, chances are you'll be just fine with most of Batocera's defaults (though your hardware may nessesitate changing video/audio settings).

And for the things you do want to change, chances are it's in the main menu. All the things in Retropie that I had to manually tinker in config files and Retroarch are now just Batocera's main menu at the start. The interface is so polished, it's amazing that this is the work of hobbyists.

You don't even really have to mess with Retroarch's infamous UI to do things like set up resolution, video filters, save state settings, etc. Even core-specific settings can be accessed at the system level from these menus. Within a few minutes of flipping through settings on the main menu, I end up with an amazing retro gaming experience without ever touching Retroarch's UI.

So now that I'm done gushing about Batocera, I found one more way to take the experience further: using a higher powered PC to play on. The old Pi 3 is good at the older stuff, but for some arcade games, Dreamcast games, PS2 and Gamecube, I needed more power.

But not *that* much power.

That's where online auctions come in. It turns out there are thousands of old, under-utilized mini PCs that will fit neatly next to your other consoles and television, and cost under $100 that are pleanty powerful enough to run your favorite 3D retro games.

Stick Batocera on one of these modest 6+ year old machines with laptop components and this will beat any Raspberry Pi retro gaming setup.

It's not a MiSTer, but perfect hardware recreation is not something I can personally discern from modern emulators running on powerful enough computers. If you notice the difference in sound or timing, that's actually pretty amazing--but for me, an $80 computer and a few different controllers depending on the system get me all the way there.

Last thing: save states are a big deal to me and one of my favorite features of this setup is **"Auto Save/Load"**. Turn it on, and you can start and leave your games at any time, and just resume from where you left off without worrying about in-game saves or manually saving and loading states. In my busier days it feels good to get in a few minutes of a game, and then be able to get back to it later, no fuss.