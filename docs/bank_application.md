# Application Bank

```xml
<?xml version="1.0" ?>

<Key>__512_alphanumeric_characters__</Key>

<AriaBank
  id="__4_digit_value__"
  name="__productname__"
  vendor="__full_brand_name__"
  product="__productname__"
  version="__4_digit_value__">

  <!-- Two effects in a graph fed by the same send mix  -->
  <Program name="Conv+Amb" type="effect" mode_offset="2000" export="0">

    <GUI target="*ARIA_EFFECTS" path="GUI/gui_ambience.xml"/>

    <Param id="19" value="0"/> <!-- like previously, Ambiance DRY is OFF -->

    <Element id="0" path="*Input"/>
    <Element id="1" path="*com.Garritan.Ambience"/>
    <Element id="2" path="*Output"/>

    <!-- MIDI/Param links -->
    <Link source="0" source_pin="m0" destination="1" destination_pin="m0"/>
    <Link source="1" source_pin="m0" destination="2" destination_pin="m0"/>

    <!-- Audio Connections  -->
    <Link source="0" source_pin="a0" destination="1" destination_pin="a0"/>
    <Link source="0" source_pin="a1" destination="1" destination_pin="a1"/>
    <Link source="1" source_pin="a0" destination="2" destination_pin="a0"/>
    <Link source="1" source_pin="a1" destination="2" destination_pin="a1"/>
  </Program>

  <Program type="effect" name="Detune" mode_offset="2000" export="0">
    <GUI target="*ARIA_EFFECTS" path="GUI/FX_detune.xml"/>
    <Param id="5" value="1"/>  <!-- like   DRY is OFF -->
    <Param id="2" value="0.5"/>

    <Element id="0" path="*Input"/>
    <Element id="1" path="*com.mda.Detune"/>
    <Element id="2" path="*Output"/>

    <!-- MIDI/Param links -->
    <Link source="0" source_pin="m0" destination="1" destination_pin="m0"/>
    <Link source="1" source_pin="m0" destination="2" destination_pin="m0"/>

    <!-- Audio Connections  -->
    <Link source="0" source_pin="a0" destination="1" destination_pin="a0"/>
    <Link source="0" source_pin="a1" destination="1" destination_pin="a1"/>
    <Link source="1" source_pin="a0" destination="2" destination_pin="a0"/>
    <Link source="1" source_pin="a1" destination="2" destination_pin="a1"/>
  </Program>

</AriaBank>
```
