# Instrument Bank

Main file to load for all xml files definitions for the instrument.<br>
Following [Unreal Instruments Kitchen-X] as example.

## Example

Kitchen-X.bank.xml:

```xml
<?xml version="1.0" ?>

<Key>__512_alphanumeric_characters__</Key>
<AriaBank id="2532" name="Kitchen-X" vendor="ARIA OEM" product="Kitchen-X" version="1000">
  <Define name="$sample_dir" value="../Samples"/>

  <!-- branding for Aria Player and sforzando UIs -->
  <AriaGUI path="GUI/aria_info.xml" target="*ARIA_INFO"/>

  <AriaProgram name="01-Kitchen-X" gui="GUI/01-Kitchen-X.xml">
    <AriaElement path="Programs/01-Kitchen-X.sfz"/>
  </AriaProgram>

  <AriaProgram name="02-Chromatic Glass" gui="GUI/02-Chromatic Glass.xml">
    <AriaElement  path="Programs/02-Chromatic Glass.sfz"/>
  </AriaProgram>

  <AriaProgram name="03-Glass Harp"  gui="GUI/03-Glass Harp.xml">
    <AriaElement path="Programs/03-Glass Harp.sfz"/>
  </AriaProgram>
</AriaBank>
```

| Name    | Type   | Description / Value(s)
| ---     | ---    | ---
| id      | int    | 4 digit product identification number
| name    | string | instrument name
| vendor  | string | instrument vendor brand
| product | string | TODO: seems to be same as name
| version | int    | 4 digit version number

## Key

UID for the instrument. The tag is at the same root level as ARIABank.

## Define

Macro from XML that can be used as alternative of the `define` opcode in SFZ,
so it can be used in SFZ files set from [AriaProgram]\(s\), e.g.:
`default_path=$sample_dir/Cello/`

| Name  | Type   | Description / Value(s)
| ---   | ---    | ---
| name  | string | the name  of the define, e.g.: "$sample_dir"
| value | string | the value of the define, e.g.: "./some/path"

## AriaGUI

| Name   | Type   | Description / Value(s)
| ---    | ---    | ---
| path   | string | the path of the UI file, e.g.: "GUI/aria_info.xml"
| target | string | an UI page ID            e.g.: "*ARIA_INFO"

## AriaProgram

| Name | Type   | Description / Value(s)
| ---  | ---    | ---
| name | string | the name of the program, e.g.: "TableWarp2"
| gui  | string | the relative path to the UI file, e.g.: "GUI/GUI.xml"

#### AriaElement

Child node of AriaProgram

| Name | Type   | Description / Value(s)
| ---  | ---    | ---
| path | string | the relative path to the SFZ file, e.g.: "Programs/TableWarp2.sfz"


[AriaProgram]: #ariaprogram
[Unreal Instruments Kitchen-X]: https://unreal-instruments.wixsite.com/unreal-instruments/kitchen-x
