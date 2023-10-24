# GUI

`GUI/aria_info.xml`:

```xml
<!--
  It's a GUI file, describing an (opaque?) image with a rectangle area
  of 775x330 size inside a 787x335 container area.
-->
<GUI w="787" h="335"  >
  <StaticImage  x="0" y="0" w="775" h="330" image="Infotab.png"/>
</GUI>
```

1st instrument set, `GUI/01-Kitchen-X.xml`:

```xml
<!--
  Like above, but having also the GUI controls for CCs and the like over
  a transparent (?) background image.
-->
<GUI w="775" h="335">
  <StaticImage x="0" y="0" w="775" h="330" image="Control.png" transparent="1"/>

  <!-- Other GUI widgets follows here (Sliders) -->
</GUI>
```

The GUI node accepts the following parameters:

| Name                    | Type    | Description / Values
| ---                     | ---     | ---
| generic_h / generic_w   | int     | TODO
| generic_s               | int     | TODO
| w / h                   | int     | size
| DrawingBoundaries       | int     | TODO
| color_back              | RGBA    | background color
| color_border            | RGBA    | border color
| color_DrawingBoundaries | RGBA    | TODO
| color_text              | RGBA    | text color
| font_size               | enum    | verysmall / small / normal / big / verybig
| idleThrottle            | int     | TODO
| image                   | string  | background image filename
