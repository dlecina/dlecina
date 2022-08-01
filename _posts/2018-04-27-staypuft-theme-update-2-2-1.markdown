---
title: StayPuft theme update 2.2.1
date: '2018-04-27 23:54:11'
tags:
- staypuft
- ghost-tag
---

It's finally time to release the next major update to [StayPuft](https://github.com/dlecina/StayPuft), my programming-oriented theme for [Ghost](https://ghost.org/).

It's been hard to find the time to do this, and it's only gotten harder as both Ghost and [Casper](https://github.com/TryGhost/Casper) were updated more and more. When I finally managed to get around to it, I found that the best course of action was to rewrite the whole thing from scratch (or rather, from the latest version of Casper), and I am quite happy with that decision, as the theme now has more features than ever and looks better than it's ever had. The code quality has also improved, so it should be a lot easier to keep up with updates now, too.

## Features

* Responsive design.
* Custom [⚡AMP](https://blog.ghost.org/custom-amp-themes/) theme.
* Post comments using [Disqus](http://disqus.com/).
* In-site search using [GhostHunter](https://github.com/i11ume/ghostHunter).
* Support for [Font Awesome](https://github.com/FortAwesome/Font-Awesome).
* Syntax highlighting using [Prism](https://github.com/LeaVerou/prism/), with Markdown support.

## Ghost 1.22.3

The new version has been tested against Ghost 1.22.3 (i.e. that's the version I'm currently running), but should work on any version beyond Ghost 1.2.0 at the time of writing. It might also work on older or newer versions, but I make no guarantees. If you would like to know what has changed on the backend, you can check out the [Ghost releases page](https://github.com/TryGhost/Ghost/releases) and the [Ghost dev blog](https://dev.ghost.org/tag/releases/).

If you need help upgrading Ghost itself, just follow the instructions in their own [Support page](https://docs.ghost.org/docs/upgrade).

## Installing StayPuft

If you're not yet using StayPuft and would like to try it out, just take a look at the Installation section over at [GitHub](https://github.com/dlecina/StayPuft#installation).

## Updating StayPuft

To update the theme, just follow the Installation instructions as normal. You may *not* copy over your existing `partials/disqus.hbs` and `partials/sidebar-external.hbs` as the format and file structure has changed slightly. It should not take much time to rebuild those, anyway. Please understand.

![Please understand](https://media.giphy.com/media/DwpavZaqZHExG/giphy.gif)

### Prism

The Markdown syntax for Prism has changed slightly, due to breaking changes in the backend 😞. On the other hand, the [File Highlight](http://prismjs.com/plugins/file-highlight/) plugin is now supported 😄. See the [Prism Demo](https://davidlecina.com/blog/prism-demo/) for details.