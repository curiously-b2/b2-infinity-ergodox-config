# b2-infinity-ergodox-config
Colemak-based keyboard layout for Infinity ErgoDox
-----
Since I've had several people ask, I figured I'd upload the KLL files for my custom config.  This is pretty much always a work in progress; I'm basically iterating on the layout and making changes as things become bothersome.

This is relatively mature at this point; I started iterating on this layout in October of 2015, so most of the little irritants have been worked out of the layout.

Note:  As of 2017-06-18, the main kiibohd controller trunk does not compile for the Infinity ErgoDox.  Here's what I found worked:
* Controller repo:  Use the 'old' branch
* KLL subrepo: Check out commit 2aed1e677e6d3a11f8b0548a9de1f6baf4f471da

In addition, I also changed the ergodox.bash build script in controller/Keyboard:

```
DefaultMap="b2-infinity-ergodox-config/baselineColemak lcdFuncMap"

PartialMaps[1]="b2-infinity-ergodox-config/qwertyOverlay"
PartialMaps[2]="b2-infinity-ergodox-config/navigationKeys"
PartialMaps[3]="b2-infinity-ergodox-config/fnKeysAndNumpad"
PartialMaps[4]="b2-infinity-ergodox-config/mediaKeys"
PartialMaps[5]="b2-infinity-ergodox-config/keyboardFunctions lcdFuncMap"

```
