# Makkon Textures Documentation

![](tbsketch_43_2_2024-12-28_05-17-02.png)

This document will help you understand how to use more advanced textures in the Makkon Textures library.
## General use, texel density, nearest filtering

Every texture in this library was originally created for the mapping and modding community in Quake (1996) by id Software. As such, they are built in some specific ways.

*Texel Density*
Most textures are authored at 512x512 pixels, with some exceptions such as props and large ground cover. 
Intended [texel density](https://uploads-ssl.webflow.com/6280d2582095efc547d41220/62befe963aa1f205531b3057_DeepDive_TexelDensity_02.pdf) is **32 pixels per meter**. In some rare cases it can be a little higher, but never higher than 64 pixels per meter.

*Nearest Filtering*
These textures were built for and look best with Nearest Filtering. However, they have been tested with Linear if that is the intended look for your game. 
## Quake specific stuff that carried over that will be addressed in future updates

Textures made for Quake (1996) have a strict 15 character limit, and that carried over to the naming convention of this library. You can change them to however you want.

*Quake specific prefixes*

`+0` and `+a`
	 are used for animated textures in quake. `+0` is the first frame, and consecutive numbers are the following frames. `+a` is the "action" frame, such as when a button is pressed.
	Often texture sets will only have `+0` and `+a` and no other frames, such as a simple button.

curly bracket `{`
	 is what quake uses to denote a texture with an alpha, or transparency. Most editors won't like having this in a file name. In future updates, I'll try to find a way to have textures I publish here don't have this prefix.

asterisk `*`
	is what quake uses for liquids, like water or lava.

*Fullbright Pixels*
Quake uses specific colors in their 256 color palette that would appear bright even in full shadow, much like modern Emissive Textures. This texture library doesn't currently include emissive textures or masks, but will in a future update. 

## Makkon Texture standard prefixes

This library has standard prefixes to denote intended use, and for better categorization.

The following prefixes denote intended use, but these textures are generally more flexible for other uses.
`c_` 
	Common textures, for general use. These can work on walls, floors, and ceilings. 
`f_`
	Floor textures.
`w_`
	Wall textures. 
`win_` 
	Window textures, sometimes tiling, sometimes in an atlas.

The following prefixes are not guidelines, but the technical function of a texture. Using them outside of their intended use will yield poor results unless you specifically know what you're doing.
`st_`
	Dedicated stair textures. 2:1 ratio, they have a gap at the top of the sheet that you'll want to skip.
`t_`
	Trimsheet textures. Trimsheets are specialized detail textures, and are explained later in the document.

## Trimsheets, and how to use them *(READ THIS if you read nothing else!!!!)*

A trimsheet is a detail texture, typically used on edges like a trim (hence the name). Please, do not use a whole trimsheet on an entire wall.
Don't want to learn to use trimsheets? That's fine, don't use them! Your game will look best when you use textures for their intended use, and don't use textures for their unintended use.

Here's a youtube video on how to use a trimsheet texture, inside of the mapping software Trenchbroom. These principles carry over to other modeling/mapping software.
![](https://youtu.be/piiYIExIN6E?si=MiF660fpd98eKYQM)

## decals overview, edge decals, damage
## unique texture callouts
## stairs (all sets)
# concrete
waffle slabs
windows
panel sheet
# industrial
dumpsters
AC units
large doors
barrels
buttons
panel sheet
waffle slabs
trusses
# tech
doors and door kit
trusses (carry over from industrial?)
gothic
trims
brockets
”make a spire” tutorial?
this whole kit is insane and maybe needs an “advanced users” label?
# urban
tile trims
manholes and drains
roads (lanes, damage)
road signs
