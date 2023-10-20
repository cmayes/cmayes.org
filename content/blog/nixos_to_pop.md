+++
title = "NixOS Is Not My Type"
date = 2023-10-19

[taxonomies]
tags = ["linux"]
+++

[NixOS](https://nixos.org/) has an intriguing approach to package management, but I don't like the tradeoffs.

<!-- more -->

After being frustrated by the tangle of .debs, [Snap packages](https://snapcraft.io/), 
and [Flatpaks](https://www.flatpak.org/) on my recently re-installed [Ubuntu](https://ubuntu.com/) machine, I decided 
to try something new. I'd heard a fair amount of enthusiasm (and some [controversy][nixos-drone]) for NixOS, so I 
decided to give it a try.

I hadn't done a lot of detailed reading on how NixOS is structured aside from the high-level "declarative configuration"
claims (which did sound nice). I like that you can define a reproducible configuration in a couple of config files.

What I don't like is the lack of a standard [LSB-style filesystem hierarchy][fhs]. It could have been simulated with
symlinks similar to the Debian "alternatives" approach, but the OS is firm that all of the libraries and executables
need to be in NixOS-specific spots and any new libraries must be linked or re-linked against the same, essentially 
requiring a special configuration file for each one.

One thing that Nix (the packaging system) and thereby NixOS has going for it is a lot of dedicated users that have 
written [many such configuration files][nix-packages], about 80,000 at current count. But as anyone who has ever 
forked a software project knows, custom work needs to be actively maintained, especially if the upstream project 
is active. I initially tried to use Nix packages where available but switched to Flatpak versions when the Nix 
packages were not up-to-date.

I reached my limit today when I was wrestling with getting Nix Python configs working with IDEA. I'm sure this works
great if you're doing everything in the terminal, but I do not. It was time to move back to a more conventional
distribution.

I spent the afternoon installing and setting up [Pop!_OS](https://pop.system76.com/) (that underscore makes
Obsidian unhappy). It's built on Ubuntu, and I do like Debian-based distributions. The configuration setup
has been much smoother than with NixOS. It's nice to have a stable, well-supported distribution. It seems like
Pop!_OS uses .debs with a fallback to Flatpaks, which was how I'd been handling oddball packages in both 
Ubuntu and NixOS. This is promising.

So far so good with Pop!_OS. The download was for an "LTS" tagged as being released in April of 2022, so I'm a 
little concerned that packages will be old. As a long-time Debian user, though, I'm used to working around
ancient package versions. I also like that the maintainer, [System76](https://system76.com/), is based in
Denver, as am I! They seem like a good company, too.

[nixos-drone]: https://www.theregister.com/2023/09/08/nixcon_drops_anduril_industries_as/
[nix-packages]: https://search.nixos.org/packages?ref=itsfoss.com
[fhs]: https://www.wikiwand.com/en/Filesystem_Hierarchy_Standard
