 _____                               
|_   _|_ _ _ __ ___  ___ _   _ _ __  
  | |/ _` | '_ ` _ \/ __| | | | '_ \ 
  | | (_| | | | | | \__ \ |_| | | | |
  |_|\__,_|_| |_| |_|___/\__, |_| |_|
                         |___/       

Monospaced Programming Font for Linux and Windows
--------------------------------------------------------------------------------

VERSION 1.11 2015-01-21

CHANGES IN 1.11

  Changed capital "A" to be less pointy, more consistent between sizes.
  Expecting hate mail.

  Previously, unimplemented chars defaulted to print a blank space under X.
  Now those chars are not placed in the font at all in order to allow
  fontconfig to fall back to use a char from another font.  (Thanks, Allen,
  for pointing this out and testing the fix.)

CHANGES IN 1.10

  New size: 7x13.

  New size: 8x16 (replaces 8x17)

  Many changes in favor of a cleaner look.  In particular, replaced the
  double-story lowercase "g" with the single-story variety.

  Added the degree symbol.  (Enjoy, Sven!)

  Added the copyright symbol.

CHANGES IN 1.9

  Fixed the problem with inverted question mark facing the wrong way.  (Thanks
  to Swyter for reporting it.)

  Modified the small "w" and "g".

  Restored the original look for size 6x12 bold.

CHANGES IN 1.8

  Fixed a problem where chars showed up as boxes in xfontsel and some apps.

  Tweaks, esp. to 8x17 size

CHANGES IN 1.7

  Added two new sizes: tiny 5x9 and large 10x20.

  Retired size 7x12.  (If this presents major problem for you, get in touch.)

  Added a pixel to the height of the 6x11 size, making it 6x12.

  Added new chars for partial ISO8859-1 support, mainly covering the accented
  characters and currency symbols.  I consider these new characters to be BETA,
  since I don't use them so I'm not sure how they should look.  If you have
  feedback about them, please get in touch.

  Made many minor tweaks to character shapes.  In particular, the f, l, and t
  have a more "traditional" look.  Also, I've changed the w and y again.

FUTURE PLANS:

  Full CP437, ISO8859-1, Windows-1252 coverage

  Mac/ttf version

  Cyrillic

  Unified FON file containing all sizes in regular and bold

  Separate OEM and 1252 Windows versions


User feedback is welcomed and encouraged.

Enjoy!
