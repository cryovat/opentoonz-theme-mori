# Mori theme for OpenToonz

Mori is an experimental theme for [OpenToonz](https://github.com/opentoonz/opentoonz), attempting to give the software a
slightly more modern look (which is mostly an euphenism for picking things I like from the Creative Suite and Atom styles).

It is based on the bundled **gray_048** with custom modifications.

The default theme looks like this:

<a href="https://github.com/cryovat/opentoonz-theme-mori/blob/master/screenshots_ot_gray_048.png"><img src="https://github.com/cryovat/opentoonz-theme-mori/blob/master/screenshots_ot_gray_048.png" width="250px" /></a>

This theme looks roughly like this:

<a href="https://github.com/cryovat/opentoonz-theme-mori/raw/master/screenshot_ot_mori.png"><img src="https://github.com/cryovat/opentoonz-theme-mori/raw/master/screenshot_ot_mori.png" width="250px" /></a>


Apart from a tiny custom piece, icons come from three sources and are subject to their respective licenses:

 * Icons from the [OpenToonz](https://github.com/opentoonz/opentoonz) project
 * Material Design icons by [Google](https://github.com/google/material-design-icons)
 * Material Design icons by [Templarian](https://github.com/Templarian/MaterialDesign)

## Was this a good idea?

Not  really. I like to believe it looks better, but it's unfinished and slightly buggy. For some reason, the font styling of the main menu doesn't work at start, but sticks if you change theme to one of the built-ins and back to *mori*.

I like to think of this as a proof-of-concept that theming is *doable*, but will advice against it for a number of reasons:

 * Some of the icons are defined in the theme, but most are embedded directly into the executable.
 * Certain UI elements such as [panel title bars](https://github.com/opentoonz/opentoonz/blob/7e185111a8e317ccea5fd8060cc15a7d1527d660/toonz/sources/toonz/pane.cpp#L362) have hard coded rendering, so you'll be stuck trying to make things look nice less to it.
 * The UI handles changes to margins and padding gracefully, except for where it doesn't. Some positions and element sizes are hard coded and pose trouble.
 * The bundled themes seem to be split into parts that are clean and generally reusable, and parts that are very specific to certain components, giving me a feeling that they never intended for anyone to do this. :grin:

## Way forward

I might tweak this some more, but I think a better way forward is to update the OpenToonz codebase in either of these directions:

 * Drop style support from the app and use the OS native ones.
 * Move all colors and icon specifications from the code to Qt stylesheets.

In either case, I think people should stick to the built-in themes until the OpenToonz team has decided on an official strategy here.

## How to compile

Edit mori.less in Atom with the less-autocompile plugin installed. OpenToonz allows live-reloading of themes if you change to a different style and back.

## How to install

If you want to try it as-is, download [this archive](https://github.com/cryovat/opentoonz-theme-mori/raw/master/dist/mori.zip) and unzip it to:

> C:\OpenToonz 1.0 stuff\config\qss

Note that this has only been tested on Windows 10. I can't provide any kind of support, but pull requests are welcome. :wink:

