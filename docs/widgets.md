# Widgets

## CommandButton

A button to run some command like open some webpage URL

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| command       | string | a command, edit / launch_url TODO
| data0         | string | command parameter e.g.: "http://www.someplace.com/"
| image         | string | the name of the image file (2 vertical frames button)
| inverted      | bool   | TODO

## GUIContainer

An abstract class / layout to contain GUI pages,
used in [TabView](#tabview) Panes

| Name    | Type   | Description / Value(s)
| ---     | ---    | ---
| eslot   | int    | TODO
| param   | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| path    | string | xml filename of the contained GUI or define macro ID
| xoffset | int    | TODO: might be border / margin / padding value
| yoffset | int    | TODO: might be border / margin / padding value

## Keyboard

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| param         | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| start_key     | int    | first note key, e.g.: 0
| end_key       | int    | last  note key, e.g.: 108
| offsetN       | int    | with N = 0 to 5, 6 in total TODO
| image         | string | filename for the enabled white keys when pressed and unpressed
| image2        | string | filename for the enabled black keys when pressed and unpressed
| image3        | string | TODO
| image4        | string | TODO

## Knob

| Name   | Type   | Description / Value(s)
| ---    | ---    | ---
| x / y  | int    | coordinates
| eslot  | int    | TODO
| param  | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| image  | string | the name of the image file (vertical frame images)
| frames | int    | number of image frames

## Label

A text label to display some value set from another control,
associated with the same `param`.

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| param         | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| alignment     | enum   | left / center / right, the text alignment inside the rect
| color_text    | RGBA   | text color
| factor        | int    | TODO
| format        | string | printf format string / FORMAT_LINEAR2DB / FORMAT_STEREOPAN
| transparent   | bool   | 1 or 0
| vdefault      | int    | TODO

## OnOffButton

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| param         | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| image         | string | the name of the image file (2 vertical frames button)

## OptionMenu

A LMB / RMB clickable label area to display a menu

| Name          | Type  | Description / Value(s)
| ---           | ---   | ---
| x / y / w / h | int   | coordinates and size
| param         | int   | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| alignment     | enum  | left / center / right, the text alignment inside the rect
| color_text    | RGBA  | e.g.: "#D7DAE0FF"
| font_size     | enum  | verysmall / small / normal / big / verybig
| transparent   | bool  | 1 or 0

### OptionItem

OptionMenu item

| Name  | Type   | Description / Value(s)
| ---   | ---    | ---
| name  | string | the menuitem label
| value | float  | the value associated e.g.: 0.5678

## \<PrefixName\>Menu

A combobox controlled by a spinner.
The control name prefix is custom, e.g. "FileMenu"

| Name                 | Type   | Description / Value(s)
| ---                  | ---    | ---
| x / y / w / h        | int    | coordinates and size
| eslot                | int    | TODO
| param                | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| target               | URL    | TODO: some effect URL, e.g.: "com.Vendor.Effectname"
| type                 | URL    | TODO: same as target
| alignment            | enum   | left / center / right, the text alignment inside the rect
| color_text           | RGBA   | text color
| entry_empty          |        | TODO: might be bool like transparent
| entry_import         |        | TODO: might be bool like transparent
| entry_reload         |        | TODO: might be bool like transparent
| font_size            | enum   | verysmall / small / normal / big / verybig
| image_next           | string | arrow image filename
| image_previous       | string | arrow image filename
| image_vertical_align |        | TODO: might be bool like transparent
| transparent          | bool   | 1 or 0

## PopupOverlay

Overlay widget, might be the one displayed when registering an instrument

| Name          | Type  | Description / Value(s)
| ---           | ---   | ---
| x / y / w / h | int   | coordinates and size
| color_back    | RGBA  | semitransparent background color (e.g.: #00000060)

## ProgressBar

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| image         | string | image filename for a 2 frames progress bar
|               |        | TODO: empty and full? Verify this


## Rect

A drawn rectangle

| Name          | Type  | Description / Value(s)
| ---           | ---   | ---
| x / y / w / h | int   | coordinates and size
| drawMode      | enum  | filled TODO
| fill_color    | RGBA  | fill color
| frameWidth    | int   | TODO

## Slider

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| param         | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| image_handle  | string | the name of the image file (slider handle)
| image_bg      | string | the name of the image file (slider trail)
| orientation   | enum   | horizontal / vertical

## SpecialDigitKnob

A clickable label that changes its value
when keeping pressed the LMB and moving the mouse left or right

| Name               | Type   | Description / Value(s)
| ---                | ---    | ---
| x / y / w / h      | int    | coordinates and size
| param              | int    | numeric or macro defined id e.g.: 10 or ID_SOMETHING
| alignment          | enum   | left / center / right, the text alignment inside the rect
| image              | string | the name of the image used for the numeric values
| minus_image        | string | the name of the image used to add a minus for negative values
| plus_image         | string | the name of the image used to add a plus  for positive values
| numbers            | int    | value size, e.g. 2 for 0-99 or 3 for 0-100
| nbh                | int    | the number image height
| nbw                | int    | the number image width
| vmin               | int    | minimum value, e.g."-100"
| vmax               | int    | maximum value, e.g."100"
| digit_min          | int    | minimum value, e.g."-100" TODO: what's the difference with vmin?
| digit_max          | int    | maximum value, e.g."100"  TODO: what's the difference with vmax?
| base               | int    | TODO
| granularity        | int    | TODO
| show_leading_zeros | int    | TODO, possible bool like transparent

## Splash

TODO: might be a splashscreen window

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| image         | string | the filename of the background image

## StaticImage

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| image         | string | the name of the image file
| transparent   | bool   | 1 or 0

## StaticText

Non variable [Label](#label) like control

| Name          | Type   | Description / Value(s)
| ---           | ---    | ---
| x / y / w / h | int    | coordinates and size
| alignment     | enum   | left / center / right, the text alignment inside the rect
| color_back    | RGBA   | background color
| color_border  | RGBA   | border color
| color_text    | RGBA   | text color
| font_size     | enum   | verysmall / small / normal / big / verybig
| text          | string | label displayed text
| transparent   | bool   | 1 or 0

## TabView

Tabbed control, with Panes as pages.

| Name             | Type   | Description / Value(s)
| ---              | ---    | ---
| x / y / w / h    | int    | coordinates and size
| id               | string | the control id
| color_selected   | RGBA   | TODO
| color_deselected | RGBA   | TODO
| image            | string | image filename of the button background (2 frames: clicked and released)
| position         | enum   | top / bottom TODO: other values?
| alignment        | enum   | left / center / right, tab button positions

### Pane

TabView' page pane.

| Name   | Type  | Description / Value(s)
| ---    | ---   | ---
| image  | image | filename of the pane   background, optional
| imageb | image | filename of the button background (2 frames: clicked and released)
