# ARIABank

Main file to load for all xml files definitions for the instrument.

Example:

Kitchen-X.bank.xml:
```xml
<?xml version="1.0" ?>
<Key>D07DD103417771BBCAAAF84CD0CCDA8E3D097FEF5D4384E61BC67B9DC46F85650536CF152993B1E9168E3B77FD612BD9A2850579BA362883F87CC4B5429B521459455F1D28C77F88410D7999D5BA12771A7F3BBB1E7C2CFF1AE396F921C9DD8C28400CBC855760752346BF2877670D27F8C979FA310D13F762AA7DEB46DE6E11CF487FC46AB8532236B009CE9E4ED9A84E8681B4408BE84EB16FA3AC15F34AEE9DE587A2569E70568901566989C5F87A14568958CC663E6F5BB4AB83F817AF1C545E93BBB5B0DB936371D4B1BAD6DFF8B9A93AAABE29BE6B58981861EFC3B1D49042F8FB8DBAF323C3AF33329761D4C175C2F228372E18F6AA069CFA094C8781</Key>
<AriaBank id="2532" name="Kitchen-X" vendor="ARIA OEM" product="Kitchen-X" version="1000" >
  <Define name="$sample_dir" value="../Samples"/>
  <!-- branding for Aria Player and sforzando UIs -->
  <AriaGUI path="GUI/aria_info.xml"  target="*ARIA_INFO" />	
  <AriaProgram  name="01-Kitchen-X"       gui="GUI/01-Kitchen-X.xml">       <AriaElement  path="Programs/01-Kitchen-X.sfz"/>       </AriaProgram>
  <AriaProgram  name="02-Chromatic Glass" gui="GUI/02-Chromatic Glass.xml"> <AriaElement  path="Programs/02-Chromatic Glass.sfz"/> </AriaProgram>
  <AriaProgram  name="03-Glass Harp"      gui="GUI/03-Glass Harp.xml">      <AriaElement  path="Programs/03-Glass Harp.sfz"/>      </AriaProgram>
</AriaBank>

```

```
id      : int, TODO
name    : string, instrument name
vendor  : string, instrument vendor brand
product : string, TODO: seems to be same as name
version : int,    4 digit version number
```

## Key

UID for the instrument. The tag is at the same root level as ARIABank.

## Define

Some macro value similar to `define` opcode in SFZ.
```
name  : string, the name  of the define, e.g.: "$sample_dir"
value : string, the value of the define, e.g.: "./some/path" 
```

## AriaGUI

```
path   : string, the path of the UI file, e.g.: "GUI/aria_info.xml"
target : string, an UI page ID            e.g.: "*ARIA_INFO"
```

## AriaProgram

```
name : string, the name of the program, e.g.: "TableWarp2"
gui  : string, the relative path to the UI file, e.g.: "GUI/GUI.xml"
```

#### AriaElement

Child node of AriaProgram

```
path : string, the relative path to the SFZ file, e.g.: "Programs/TableWarp2.sfz"
```
