## MVPokemon - Minimum Viable Pokemon

tl;dr This project is me documenting my attempts to make Pokemon Go on the web platform, 
mostly to see if a) it's possible and b) I'm able to do it. 

![Minimum Viable Jiggly Puff :D](http://soloblog.co.uk/wp-content/uploads/2013/11/jigglypuff.jpg)

### Approach
I'll prefer building out features by hand where possible,
and try to switch to libraries to help me only when I already understand the underlying tech or I need help. As an example, 
I'll probs use three.js instead of raw webgl because I pretty much get how webgl works already (at a simplistic level) so I don't
 need to learn that, and webgl can be cumbersome to write by hand. On the other hand, I'll try to do some collision detection/AR stuff by hand 
so I can learn how it works. I'm also gonna gloss over some of the difficult server sync-ing problems, at least in the short term, 
in favour of working out if the web platform can handle the basics!

### Ideas

#### For area-view 
- [Vizicities](https://github.com/UDST/vizicities#examples) for displaying local area
- [geolocation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/Using_geolocation) with watchLocation to track player position
- "randomly" display pokemon within camera frustum on map

#### For catch-view
- Html5 Media API to read camera
- Pipe it through to a canvas to overlay images of pokemon and pokeball
- Then need to use mouse/touch gestures to move the pokeball - [hammer.js](http://hammerjs.github.io/)?
- Can use mouse/touch event x+y for canvas picking, to only move pokeball with mouse gesture
- Will probably need third party library for the throw/bounce physics stuff 

#### Pokemon specific libs 
- [Pokedex!](https://www.npmjs.com/package/pokedex)
- [3d Pokemon models - export to three.js](https://clara.io/library?query=pokemon)

If there's a way of getting some [Project Tango](https://store.google.com/product/tango_tablet_development_kit) goodness into it, possibly making the AR catch-view fancier/more realistic, I will find it :P
