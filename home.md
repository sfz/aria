# ARIA

ARIA XML UI are subdivided in 2 file types:

- Banks: main files to load the entire sample pack, including sfz files with samples
- GUI files: the various UI definitions

Following [Unreal Instruments Kitchen-X] as example. 

## ARIA XML Bank

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

## ARIA XML GUI file

Various definitions, here for the main info page image background `GUI/aria_info.xml`:
```xml
<GUI w="787" h="335"  >
    <StaticImage  x="0" y="0" w="775" h="330"  image="Infotab.png"/>
</GUI>
```

1st instrument set, `GUI/01-Kitchen-X.xml`:
```xml
<GUI w="775" h="335">

<StaticImage x="0" y="0" w="775" h="330" image="Control.png" transparent="1" />

<Slider param="07"   x="301"  y="128"  w="170" h="28" orientation="horizontal" image_handle="Fader_Large.png" image_bg="Fader_Back.png" />
<Slider param="10"   x="301"  y="188"  w="170" h="28" orientation="horizontal" image_handle="Fader_Large.png" image_bg="Fader_Back.png" />
<Slider param="20"   x="301"  y="247"  w="170" h="28" orientation="horizontal" image_handle="Fader_Large.png" image_bg="Fader_Back.png" />

<Slider param="24"   x="527"  y="80"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="25"   x="580"  y="80"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="26"   x="633"  y="80"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="27"   x="686"  y="80"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />

<Slider param="28"   x="527"  y="119"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="29"   x="580"  y="119"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="30"   x="633"  y="119"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="31"   x="686"  y="119"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />

<Slider param="46"   x="527"  y="158"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="47"   x="580"  y="158"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="48"   x="633"  y="158"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="49"   x="686"  y="158"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />

<Slider param="50"   x="527"  y="197"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="53"   x="580"  y="197"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="54"   x="633"  y="197"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="55"   x="686"  y="197"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />

<Slider param="56"   x="527"  y="236"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="57"   x="580"  y="236"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="58"   x="633"  y="236"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />
<Slider param="59"   x="686"  y="236"  w="6" h="35" orientation="vertical" image_handle="Fader_Small.png" image_bg="Fader_Back_Small.png" />

</GUI>
```


[Unreal Instruments Kitchen-X]: https://unreal-instruments.wixsite.com/unreal-instruments/kitchen-x