# AriaSetup.xml

This file is quite self descriptive.

```xml
<?xml version="1.0" ?>

<Key>__512_alphanumeric_characters__</Key>
<AriaSetup version="__4_digit_value__">

  <Property name="vendor"           value="__full_brand_name__"/>
  <Property name="product"          value="__productname__"/>
  <Property name="productID"        value="__4_digit_value__"/>
  <Property name="product_full"     value="__brand__ __productname__"/>
  <Property name="version"          value="__4_digit_value__"/>

<!-- Path to .scl files directory -->
  <Property name="default_path_scl" value="Scales"/>
  <Property name="supportURL"       value="__http(s)_url_to_customer_support__"/>
  <Property name="default_bank"     value="__appname__.bank.xml"/>

<!-- TODO: Ignore Key? -->
  <Property name="default_bank_signed" value="0"/>

<!-- If to use D2D Windows renderer -->
  <Property name="usesD2D"             value="1"/>
<!--
  Possible additional properties:

  <Property name="guiPath" value="GUI/gui.xml"/>
  <Property name="registerURL" value="__http(s) url to product registration__"/>
  <Property name="blacklisted_banks" value="__4_digit_value__"/>
  <Property name="usesPalette" value="1"/>
  <Property name="paletteWidth_Windows" value="__3_digit_value__"/>
  <Property name="paletteWidth_OSXCarbon" value="__3_digit_value__"/>
  <Property name="paletteWidth_OSXCocoa" value="__3_digit_value__"/>
-->

  <Converters>
    <Converter extension="dls" program=""/>
    <Converter extension="sf2" program=""/>
    <Converter extension="wav" program=""/>
  </Converters>

<!-- ARIA Player have 16 slots (0 to 15) with midi_mode="4", no polyphony -->
  <Multi>
    <Slot id="00" midi_mode="1" polyphony="64" />
  </Multi>

  <Aliases>
<!-- GM2 Effect send (Reverb) -->
    <Alias source="91" destination="DID_AUXSEND0" transform="linear"/>
<!--
    ARIA Player have also an (unused) chorus
    <Alias source="93" destination="DID_AUXSEND1" transform="linear"/
-->
  </Aliases>

  <Effects>
<!-- ARIA Player have also `id` and `position` additional attributes -->
    <Effect name="Ambience" bankId="__4_digit_value__" bus="audio_aux0"/>
  </Effects>

</AriaSetup>
```
