# ARIA XML files

The ARIA engine library uses XML files to describe the structure and functioning
of both application and instrument products.

The information in this documentation was extracted from the XML data in Plogue
products using the [ARIA engine], like [Alter/Ego], [chipsounds], [sforzando]
or Garritan [ARIA Player] and various free sfz based audio sample libraries.

## [AriaSetup].xml

Defines the application based on ARIA engine and loads
the default bank, e.g. `sforzando.bank.xml` and GUI, e.g. `GUI/gui.xml`.

## *.bank.xml

This file is used for both [applications] and [instruments] products,
and it can define audio, MIDI and/or GUI aspects of a product,
depending on the properties they use.

In case of instruments, it loads the related sfz file(s).
It's digitally signed and should not be altered,
but users who want to modify instruments can edit the .sfz and .xml files
this file points to.

## [GUI]/*.xml

One or more gui file(s) are usually located in a `GUI` directory for
any product type, instrument or application.
Contains various [Widgets] definitions.

## *.[ariax] presets

TODO

[ARIA engine]:  http://ariaengine.com
[Alter/Ego]:    https://www.plogue.com/products/alter-ego.html
[chipsounds]:   https://www.plogue.com/products/chipsounds.html
[sforzando]:    https://www.plogue.com/products/sforzando.html
[ARIA Player]:  https://makemusic.zendesk.com/hc/en-us/sections/7141874221463-ARIA-Player-Installers
[AriaSetup]:    ariasetup.md
[applications]: bank_application.md
[instruments]:  bank_instrument.md
[GUI]:          gui.md
[Widgets]:      widgets.md
[ariax]:        ariax.md
