# Reference — TA Build Tree

How units actually get into the game: which constructor builds
what, **laid out in the exact 2-column × 3-row grid TA shows**
in the in-game build menu. Derived from
`gamedata/sidedata.tdf`'s `[CANBUILD]` table plus every
`download/*.tdf` `[MENUENTRY]` registration, merged the way the
engine merges them at boot.

- **45 builders** across 2 sides.
- **575 `(builder, unit)` pairs total**, of which
  **101** come from `download/*.tdf` (marked ⬇️).

Each builder block below shows that constructor's build menu
**one page at a time**, with each page laid out as a 2-column
× 3-row table. Slots are numbered left-to-right, top-to-bottom
(`button 0` = top-left, `button 5` = bottom-right). Empty slots
on a page render as `·`.

- See [TA unit IDs](ta-units.md) for full per-unit stats.
- See [TDF: `[MENUENTRY]`](https://github.com/coreprime/kbot/blob/main/docs/formats/tdf.md#menuentry--build-menu-extension)
  in the kbot docs for the format that ships the ⬇️ additions.
- See [Gamedata: `sidedata.tdf`](https://github.com/coreprime/kbot/blob/main/docs/formats/gamedata.md#canbuild-build-menus)
  in the kbot docs for the static `[CANBUILD]` table.

> [!TIP]
> **Hover any thumbnail** for its `UnitName`. The portraits are
> the same files used by [ta-units.md](ta-units.md).

## Contents

- [Arm](#arm)
  - [Commander](#arm---commander)
  - [Basic factories (tier 1)](#arm---basic-factories-tier-1)
  - [Construction units (mobile, tier 1)](#arm---construction-units-mobile-tier-1)
  - [Advanced Construction (mobile, tier 2)](#arm---advanced-construction-mobile-tier-2)
  - [Utility (mine layers, hover pads)](#arm---utility-mine-layers-hover-pads)
  - [Advanced factories (tier 2)](#arm---advanced-factories-tier-2)
- [Core](#core)
  - [Commander](#core---commander)
  - [Basic factories (tier 1)](#core---basic-factories-tier-1)
  - [Construction units (mobile, tier 1)](#core---construction-units-mobile-tier-1)
  - [Advanced Construction (mobile, tier 2)](#core---advanced-construction-mobile-tier-2)
  - [Utility (mine layers, hover pads)](#core---utility-mine-layers-hover-pads)
  - [Advanced factories (tier 2)](#core---advanced-factories-tier-2)
  - [Krogoth gantry](#core---krogoth-gantry)

---

## ARM

22 builders across 6 tiers.


### Arm — Commander

#### `ARMCOM` — Commander

_Commander_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armcom.png" width="80" alt="Commander" title="ARMCOM" /><br/><sub><code>ARMCOM</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsolar.png" width="48" alt="Solar Collector" title="ARMSOLAR" /><br/><code>ARMSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/armwin.png" width="48" alt="Wind Generator" title="ARMWIN" /><br/><code>ARMWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armestor.png" width="48" alt="Energy Storage" title="ARMESTOR" /><br/><code>ARMESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armmstor.png" width="48" alt="Metal Storage" title="ARMMSTOR" /><br/><code>ARMMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmex.png" width="48" alt="Metal Extractor" title="ARMMEX" /><br/><code>ARMMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmakr.png" width="48" alt="Metal Maker" title="ARMMAKR" /><br/><code>ARMMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armllt.png" width="48" alt="L.L.T." title="ARMLLT" /><br/><code>ARMLLT</code><br/><sub>L.L.T.</sub></td><td valign="top" align="center"><img src="img/ta-units/armrad.png" width="48" alt="Radar Tower" title="ARMRAD" /><br/><code>ARMRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsonar.png" width="48" alt="Sonar Station" title="ARMSONAR" /><br/><code>ARMSONAR</code><br/><sub>Sonar Station</sub></td><td valign="top" align="center"><img src="img/ta-units/armtide.png" width="48" alt="Tidal Generator" title="ARMTIDE" /><br/><code>ARMTIDE</code><br/><sub>Tidal Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armuwes.png" width="48" alt="Underwater Energy Storage" title="ARMUWES" /><br/><code>ARMUWES</code><br/><sub>Underwater Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armuwms.png" width="48" alt="Underwater Metal Storage" title="ARMUWMS" /><br/><code>ARMUWMS</code><br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armuwmex.png" width="48" alt="Underwater Metal Extractor" title="ARMUWMEX" /><br/><code>ARMUWMEX</code><br/><sub>Underwater Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armfmkr.png" width="48" alt="Floating Metal Maker" title="ARMFMKR" /><br/><code>ARMFMKR</code><br/><sub>Floating Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armtl.png" width="48" alt="Torpedo Launcher" title="ARMTL" /><br/><code>ARMTL</code><br/><sub>Torpedo Launcher</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>19</b> buildable units across <b>4</b> pages.</sub>
</td>
</tr>
</table>



### Arm — Basic factories (tier 1)

#### `ARMAP` — Aircraft Plant

_Produces Aircraft_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armap.png" width="80" alt="Aircraft Plant" title="ARMAP" /><br/><sub><code>ARMAP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center"><img src="img/ta-units/armpeep.png" width="48" alt="Peeper" title="ARMPEEP" /><br/><code>ARMPEEP</code><br/><sub>Peeper</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfig.png" width="48" alt="Freedom Fighter" title="ARMFIG" /><br/><code>ARMFIG</code><br/><sub>Freedom Fighter</sub></td><td valign="top" align="center"><img src="img/ta-units/armthund.png" width="48" alt="Thunder" title="ARMTHUND" /><br/><code>ARMTHUND</code><br/><sub>Thunder</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armatlas.png" width="48" alt="Atlas" title="ARMATLAS" /><br/><code>ARMATLAS</code><br/><sub>Atlas</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>5</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `ARMLAB` — Kbot Lab

_Produces Kbots_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armlab.png" width="80" alt="Kbot Lab" title="ARMLAB" /><br/><sub><code>ARMLAB</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center"><img src="img/ta-units/armpw.png" width="48" alt="Peewee" title="ARMPW" /><br/><code>ARMPW</code><br/><sub>Peewee</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armrock.png" width="48" alt="Rocko" title="ARMROCK" /><br/><code>ARMROCK</code><br/><sub>Rocko</sub></td><td valign="top" align="center"><img src="img/ta-units/armham.png" width="48" alt="Hammer" title="ARMHAM" /><br/><code>ARMHAM</code><br/><sub>Hammer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armjeth.png" width="48" alt="Jethro" title="ARMJETH" /><br/><code>ARMJETH</code><br/><sub>Jethro</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armwar.png" width="48" alt="Warrior" title="ARMWAR" /><br/><code>ARMWAR</code> ⬇️<br/><sub>Warrior</sub></td><td valign="top" align="center"><img src="img/ta-units/armflea.png" width="48" alt="Flea" title="ARMFLEA" /><br/><code>ARMFLEA</code> ⬇️<br/><sub>Flea</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>7</b> buildable units across <b>2</b> pages; <b>2</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `ARMSY` — Shipyard

_Produces Ships_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armsy.png" width="80" alt="Shipyard" title="ARMSY" /><br/><sub><code>ARMSY</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center"><img src="img/ta-units/armpt.png" width="48" alt="Skeeter" title="ARMPT" /><br/><code>ARMPT</code><br/><sub>Skeeter</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armroy.png" width="48" alt="Crusader" title="ARMROY" /><br/><code>ARMROY</code><br/><sub>Crusader</sub></td><td valign="top" align="center"><img src="img/ta-units/armtship.png" width="48" alt="Hulk" title="ARMTSHIP" /><br/><code>ARMTSHIP</code><br/><sub>Hulk</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsub.png" width="48" alt="Lurker" title="ARMSUB" /><br/><code>ARMSUB</code><br/><sub>Lurker</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>5</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `ARMVP` — Vehicle Plant

_Produces Vehicles_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armvp.png" width="80" alt="Vehicle Plant" title="ARMVP" /><br/><sub><code>ARMVP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td valign="top" align="center"><img src="img/ta-units/armfav.png" width="48" alt="Jeffy" title="ARMFAV" /><br/><code>ARMFAV</code><br/><sub>Jeffy</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armflash.png" width="48" alt="Flash" title="ARMFLASH" /><br/><code>ARMFLASH</code><br/><sub>Flash</sub></td><td valign="top" align="center"><img src="img/ta-units/armstump.png" width="48" alt="Stumpy" title="ARMSTUMP" /><br/><code>ARMSTUMP</code><br/><sub>Stumpy</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsam.png" width="48" alt="Samson" title="ARMSAM" /><br/><code>ARMSAM</code><br/><sub>Samson</sub></td><td valign="top" align="center"><img src="img/ta-units/armmlv.png" width="48" alt="Podger" title="ARMMLV" /><br/><code>ARMMLV</code><br/><sub>Podger</sub></td></tr>
</table>


<sub><b>6</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>



### Arm — Construction units (mobile, tier 1)

#### `ARMCA` — Construction Aircraft

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armca.png" width="80" alt="Construction Aircraft" title="ARMCA" /><br/><sub><code>ARMCA</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsolar.png" width="48" alt="Solar Collector" title="ARMSOLAR" /><br/><code>ARMSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/armwin.png" width="48" alt="Wind Generator" title="ARMWIN" /><br/><code>ARMWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armestor.png" width="48" alt="Energy Storage" title="ARMESTOR" /><br/><code>ARMESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armmstor.png" width="48" alt="Metal Storage" title="ARMMSTOR" /><br/><code>ARMMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmex.png" width="48" alt="Metal Extractor" title="ARMMEX" /><br/><code>ARMMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmakr.png" width="48" alt="Metal Maker" title="ARMMAKR" /><br/><code>ARMMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armllt.png" width="48" alt="L.L.T." title="ARMLLT" /><br/><code>ARMLLT</code><br/><sub>L.L.T.</sub></td><td valign="top" align="center"><img src="img/ta-units/armrad.png" width="48" alt="Radar Tower" title="ARMRAD" /><br/><code>ARMRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armaap.png" width="48" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><code>ARMAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armgeo.png" width="48" alt="Geothermal Powerplant" title="ARMGEO" /><br/><code>ARMGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhlt.png" width="48" alt="Sentinel" title="ARMHLT" /><br/><code>ARMHLT</code><br/><sub>Sentinel</sub></td><td valign="top" align="center"><img src="img/ta-units/armrl.png" width="48" alt="Defender" title="ARMRL" /><br/><code>ARMRL</code><br/><sub>Defender</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armdrag.png" width="48" alt="Dragon&#39;s Teeth" title="ARMDRAG" /><br/><code>ARMDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/armguard.png" width="48" alt="Guardian" title="ARMGUARD" /><br/><code>ARMGUARD</code><br/><sub>Guardian</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>19</b> buildable units across <b>4</b> pages.</sub>
</td>
</tr>
</table>


#### `ARMCH` — Construction Hovercraft

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armch.png" width="80" alt="Construction Hovercraft" title="ARMCH" /><br/><sub><code>ARMCH</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsolar.png" width="48" alt="Solar Collector" title="ARMSOLAR" /><br/><code>ARMSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/armwin.png" width="48" alt="Wind Generator" title="ARMWIN" /><br/><code>ARMWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armestor.png" width="48" alt="Energy Storage" title="ARMESTOR" /><br/><code>ARMESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armmstor.png" width="48" alt="Metal Storage" title="ARMMSTOR" /><br/><code>ARMMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmex.png" width="48" alt="Metal Extractor" title="ARMMEX" /><br/><code>ARMMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmakr.png" width="48" alt="Metal Maker" title="ARMMAKR" /><br/><code>ARMMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armllt.png" width="48" alt="L.L.T." title="ARMLLT" /><br/><code>ARMLLT</code><br/><sub>L.L.T.</sub></td><td valign="top" align="center"><img src="img/ta-units/armrad.png" width="48" alt="Radar Tower" title="ARMRAD" /><br/><code>ARMRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armgeo.png" width="48" alt="Geothermal Powerplant" title="ARMGEO" /><br/><code>ARMGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhlt.png" width="48" alt="Sentinel" title="ARMHLT" /><br/><code>ARMHLT</code><br/><sub>Sentinel</sub></td><td valign="top" align="center"><img src="img/ta-units/armrl.png" width="48" alt="Defender" title="ARMRL" /><br/><code>ARMRL</code><br/><sub>Defender</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armdrag.png" width="48" alt="Dragon&#39;s Teeth" title="ARMDRAG" /><br/><code>ARMDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/armguard.png" width="48" alt="Guardian" title="ARMGUARD" /><br/><code>ARMGUARD</code><br/><sub>Guardian</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsonar.png" width="48" alt="Sonar Station" title="ARMSONAR" /><br/><code>ARMSONAR</code><br/><sub>Sonar Station</sub></td><td valign="top" align="center"><img src="img/ta-units/armtide.png" width="48" alt="Tidal Generator" title="ARMTIDE" /><br/><code>ARMTIDE</code><br/><sub>Tidal Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armuwes.png" width="48" alt="Underwater Energy Storage" title="ARMUWES" /><br/><code>ARMUWES</code><br/><sub>Underwater Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armuwms.png" width="48" alt="Underwater Metal Storage" title="ARMUWMS" /><br/><code>ARMUWMS</code><br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armuwmex.png" width="48" alt="Underwater Metal Extractor" title="ARMUWMEX" /><br/><code>ARMUWMEX</code><br/><sub>Underwater Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armfmkr.png" width="48" alt="Floating Metal Maker" title="ARMFMKR" /><br/><code>ARMFMKR</code><br/><sub>Floating Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfrt.png" width="48" alt="Defender - NS" title="ARMFRT" /><br/><code>ARMFRT</code><br/><sub>Defender - NS</sub></td><td valign="top" align="center"><img src="img/ta-units/armfdrag.png" width="48" alt="Floating Dragon&#39;s Teeth" title="ARMFDRAG" /><br/><code>ARMFDRAG</code><br/><sub>Floating Dragon&#39;s Teeth</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfhlt.png" width="48" alt="Stingray" title="ARMFHLT" /><br/><code>ARMFHLT</code><br/><sub>Stingray</sub></td><td valign="top" align="center"><img src="img/ta-units/armtl.png" width="48" alt="Torpedo Launcher" title="ARMTL" /><br/><code>ARMTL</code><br/><sub>Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>29</b> buildable units across <b>5</b> pages.</sub>
</td>
</tr>
</table>


#### `ARMCK` — Construction KBot

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armck.png" width="80" alt="Construction KBot" title="ARMCK" /><br/><sub><code>ARMCK</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsolar.png" width="48" alt="Solar Collector" title="ARMSOLAR" /><br/><code>ARMSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/armwin.png" width="48" alt="Wind Generator" title="ARMWIN" /><br/><code>ARMWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armestor.png" width="48" alt="Energy Storage" title="ARMESTOR" /><br/><code>ARMESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armmstor.png" width="48" alt="Metal Storage" title="ARMMSTOR" /><br/><code>ARMMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmex.png" width="48" alt="Metal Extractor" title="ARMMEX" /><br/><code>ARMMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmakr.png" width="48" alt="Metal Maker" title="ARMMAKR" /><br/><code>ARMMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armllt.png" width="48" alt="L.L.T." title="ARMLLT" /><br/><code>ARMLLT</code><br/><sub>L.L.T.</sub></td><td valign="top" align="center"><img src="img/ta-units/armrad.png" width="48" alt="Radar Tower" title="ARMRAD" /><br/><code>ARMRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armgeo.png" width="48" alt="Geothermal Powerplant" title="ARMGEO" /><br/><code>ARMGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhlt.png" width="48" alt="Sentinel" title="ARMHLT" /><br/><code>ARMHLT</code><br/><sub>Sentinel</sub></td><td valign="top" align="center"><img src="img/ta-units/armrl.png" width="48" alt="Defender" title="ARMRL" /><br/><code>ARMRL</code><br/><sub>Defender</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armdrag.png" width="48" alt="Dragon&#39;s Teeth" title="ARMDRAG" /><br/><code>ARMDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/armguard.png" width="48" alt="Guardian" title="ARMGUARD" /><br/><code>ARMGUARD</code><br/><sub>Guardian</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>19</b> buildable units across <b>4</b> pages.</sub>
</td>
</tr>
</table>


#### `ARMCS` — Construction Ship

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armcs.png" width="80" alt="Construction Ship" title="ARMCS" /><br/><sub><code>ARMCS</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td valign="top" align="center"><img src="img/ta-units/armtl.png" width="48" alt="Torpedo Launcher" title="ARMTL" /><br/><code>ARMTL</code><br/><sub>Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armtide.png" width="48" alt="Tidal Generator" title="ARMTIDE" /><br/><code>ARMTIDE</code><br/><sub>Tidal Generator</sub></td><td valign="top" align="center"><img src="img/ta-units/armsonar.png" width="48" alt="Sonar Station" title="ARMSONAR" /><br/><code>ARMSONAR</code><br/><sub>Sonar Station</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armllt.png" width="48" alt="L.L.T." title="ARMLLT" /><br/><code>ARMLLT</code><br/><sub>L.L.T.</sub></td><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfrt.png" width="48" alt="Defender - NS" title="ARMFRT" /><br/><code>ARMFRT</code> ⬇️<br/><sub>Defender - NS</sub></td><td valign="top" align="center"><img src="img/ta-units/armuwes.png" width="48" alt="Underwater Energy Storage" title="ARMUWES" /><br/><code>ARMUWES</code> ⬇️<br/><sub>Underwater Energy Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfmkr.png" width="48" alt="Floating Metal Maker" title="ARMFMKR" /><br/><code>ARMFMKR</code> ⬇️<br/><sub>Floating Metal Maker</sub></td><td valign="top" align="center"><img src="img/ta-units/armuwms.png" width="48" alt="Underwater Metal Storage" title="ARMUWMS" /><br/><code>ARMUWMS</code> ⬇️<br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfhlt.png" width="48" alt="Stingray" title="ARMFHLT" /><br/><code>ARMFHLT</code> ⬇️<br/><sub>Stingray</sub></td><td valign="top" align="center"><img src="img/ta-units/armuwmex.png" width="48" alt="Underwater Metal Extractor" title="ARMUWMEX" /><br/><code>ARMUWMEX</code> ⬇️<br/><sub>Underwater Metal Extractor</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfdrag.png" width="48" alt="Floating Dragon&#39;s Teeth" title="ARMFDRAG" /><br/><code>ARMFDRAG</code> ⬇️<br/><sub>Floating Dragon&#39;s Teeth</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>13</b> buildable units across <b>3</b> pages; <b>7</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `ARMCSA` — Construction Seaplane

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armcsa.png" width="80" alt="Construction Seaplane" title="ARMCSA" /><br/><sub><code>ARMCSA</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsolar.png" width="48" alt="Solar Collector" title="ARMSOLAR" /><br/><code>ARMSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/armwin.png" width="48" alt="Wind Generator" title="ARMWIN" /><br/><code>ARMWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armestor.png" width="48" alt="Energy Storage" title="ARMESTOR" /><br/><code>ARMESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armmstor.png" width="48" alt="Metal Storage" title="ARMMSTOR" /><br/><code>ARMMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmex.png" width="48" alt="Metal Extractor" title="ARMMEX" /><br/><code>ARMMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmakr.png" width="48" alt="Metal Maker" title="ARMMAKR" /><br/><code>ARMMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armllt.png" width="48" alt="L.L.T." title="ARMLLT" /><br/><code>ARMLLT</code><br/><sub>L.L.T.</sub></td><td valign="top" align="center"><img src="img/ta-units/armrad.png" width="48" alt="Radar Tower" title="ARMRAD" /><br/><code>ARMRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armgeo.png" width="48" alt="Geothermal Powerplant" title="ARMGEO" /><br/><code>ARMGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhlt.png" width="48" alt="Sentinel" title="ARMHLT" /><br/><code>ARMHLT</code><br/><sub>Sentinel</sub></td><td valign="top" align="center"><img src="img/ta-units/armrl.png" width="48" alt="Defender" title="ARMRL" /><br/><code>ARMRL</code><br/><sub>Defender</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armdrag.png" width="48" alt="Dragon&#39;s Teeth" title="ARMDRAG" /><br/><code>ARMDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/armguard.png" width="48" alt="Guardian" title="ARMGUARD" /><br/><code>ARMGUARD</code><br/><sub>Guardian</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsonar.png" width="48" alt="Sonar Station" title="ARMSONAR" /><br/><code>ARMSONAR</code><br/><sub>Sonar Station</sub></td><td valign="top" align="center"><img src="img/ta-units/armtide.png" width="48" alt="Tidal Generator" title="ARMTIDE" /><br/><code>ARMTIDE</code><br/><sub>Tidal Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armuwes.png" width="48" alt="Underwater Energy Storage" title="ARMUWES" /><br/><code>ARMUWES</code><br/><sub>Underwater Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armuwms.png" width="48" alt="Underwater Metal Storage" title="ARMUWMS" /><br/><code>ARMUWMS</code><br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armuwmex.png" width="48" alt="Underwater Metal Extractor" title="ARMUWMEX" /><br/><code>ARMUWMEX</code><br/><sub>Underwater Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armfmkr.png" width="48" alt="Floating Metal Maker" title="ARMFMKR" /><br/><code>ARMFMKR</code><br/><sub>Floating Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfrt.png" width="48" alt="Defender - NS" title="ARMFRT" /><br/><code>ARMFRT</code><br/><sub>Defender - NS</sub></td><td valign="top" align="center"><img src="img/ta-units/armfdrag.png" width="48" alt="Floating Dragon&#39;s Teeth" title="ARMFDRAG" /><br/><code>ARMFDRAG</code><br/><sub>Floating Dragon&#39;s Teeth</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfhlt.png" width="48" alt="Stingray" title="ARMFHLT" /><br/><code>ARMFHLT</code><br/><sub>Stingray</sub></td><td valign="top" align="center"><img src="img/ta-units/armtl.png" width="48" alt="Torpedo Launcher" title="ARMTL" /><br/><code>ARMTL</code><br/><sub>Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>29</b> buildable units across <b>5</b> pages.</sub>
</td>
</tr>
</table>


#### `ARMCV` — Construction Vehicle

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armcv.png" width="80" alt="Construction Vehicle" title="ARMCV" /><br/><sub><code>ARMCV</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsolar.png" width="48" alt="Solar Collector" title="ARMSOLAR" /><br/><code>ARMSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/armwin.png" width="48" alt="Wind Generator" title="ARMWIN" /><br/><code>ARMWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armestor.png" width="48" alt="Energy Storage" title="ARMESTOR" /><br/><code>ARMESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/armmstor.png" width="48" alt="Metal Storage" title="ARMMSTOR" /><br/><code>ARMMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmex.png" width="48" alt="Metal Extractor" title="ARMMEX" /><br/><code>ARMMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmakr.png" width="48" alt="Metal Maker" title="ARMMAKR" /><br/><code>ARMMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armllt.png" width="48" alt="L.L.T." title="ARMLLT" /><br/><code>ARMLLT</code><br/><sub>L.L.T.</sub></td><td valign="top" align="center"><img src="img/ta-units/armrad.png" width="48" alt="Radar Tower" title="ARMRAD" /><br/><code>ARMRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armgeo.png" width="48" alt="Geothermal Powerplant" title="ARMGEO" /><br/><code>ARMGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhlt.png" width="48" alt="Sentinel" title="ARMHLT" /><br/><code>ARMHLT</code><br/><sub>Sentinel</sub></td><td valign="top" align="center"><img src="img/ta-units/armrl.png" width="48" alt="Defender" title="ARMRL" /><br/><code>ARMRL</code><br/><sub>Defender</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armdrag.png" width="48" alt="Dragon&#39;s Teeth" title="ARMDRAG" /><br/><code>ARMDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/armguard.png" width="48" alt="Guardian" title="ARMGUARD" /><br/><code>ARMGUARD</code><br/><sub>Guardian</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>19</b> buildable units across <b>4</b> pages.</sub>
</td>
</tr>
</table>


#### `ARMPLAT` — Seaplane Platform

_Builds Seaplanes_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armplat.png" width="80" alt="Seaplane Platform" title="ARMPLAT" /><br/><sub><code>ARMPLAT</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center"><img src="img/ta-units/armsehak.png" width="48" alt="Seahawk" title="ARMSEHAK" /><br/><code>ARMSEHAK</code><br/><sub>Seahawk</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsfig.png" width="48" alt="Tornado" title="ARMSFIG" /><br/><code>ARMSFIG</code><br/><sub>Tornado</sub></td><td valign="top" align="center"><img src="img/ta-units/armhawk.png" width="48" alt="Hawk" title="ARMHAWK" /><br/><code>ARMHAWK</code><br/><sub>Hawk</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlance.png" width="48" alt="Lancet" title="ARMLANCE" /><br/><code>ARMLANCE</code><br/><sub>Lancet</sub></td><td valign="top" align="center"><img src="img/ta-units/armseap.png" width="48" alt="Albatross" title="ARMSEAP" /><br/><code>ARMSEAP</code><br/><sub>Albatross</sub></td></tr>
</table>


<sub><b>6</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>



### Arm — Advanced Construction (mobile, tier 2)

#### `ARMACA` — Adv. Construction Aircraft

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armaca.png" width="80" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><sub><code>ARMACA</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armarad.png" width="48" alt="Advanced Radar Tower" title="ARMARAD" /><br/><code>ARMARAD</code><br/><sub>Advanced Radar Tower</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfus.png" width="48" alt="Fusion Reactor" title="ARMFUS" /><br/><code>ARMFUS</code><br/><sub>Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmoho.png" width="48" alt="Moho Mine" title="ARMMOHO" /><br/><code>ARMMOHO</code><br/><sub>Moho Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armbrtha.png" width="48" alt="Big Bertha" title="ARMBRTHA" /><br/><code>ARMBRTHA</code><br/><sub>Big Bertha</sub></td><td valign="top" align="center"><img src="img/ta-units/armsilo.png" width="48" alt="Retaliator" title="ARMSILO" /><br/><code>ARMSILO</code><br/><sub>Retaliator</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armanni.png" width="48" alt="Annihilator" title="ARMANNI" /><br/><code>ARMANNI</code><br/><sub>Annihilator</sub></td><td valign="top" align="center"><img src="img/ta-units/armamd.png" width="48" alt="Protector" title="ARMAMD" /><br/><code>ARMAMD</code><br/><sub>Protector</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armasp.png" width="48" alt="Air Repair Pad" title="ARMASP" /><br/><code>ARMASP</code><br/><sub>Air Repair Pad</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/armflak.png" width="48" alt="Flakker" title="ARMFLAK" /><br/><code>ARMFLAK</code> ⬇️<br/><sub>Flakker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfort.png" width="48" alt="Fortification Wall" title="ARMFORT" /><br/><code>ARMFORT</code> ⬇️<br/><sub>Fortification Wall</sub></td><td valign="top" align="center"><img src="img/ta-units/armamb.png" width="48" alt="Ambusher" title="ARMAMB" /><br/><code>ARMAMB</code> ⬇️<br/><sub>Ambusher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armckfus.png" width="48" alt="Cloakable Fusion Reactor" title="ARMCKFUS" /><br/><code>ARMCKFUS</code> ⬇️<br/><sub>Cloakable Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmmkr.png" width="48" alt="Moho Metal Maker" title="ARMMMKR" /><br/><code>ARMMMKR</code> ⬇️<br/><sub>Moho Metal Maker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armtarg.png" width="48" alt="Targeting Facility" title="ARMTARG" /><br/><code>ARMTARG</code> ⬇️<br/><sub>Targeting Facility</sub></td><td valign="top" align="center"><img src="img/ta-units/armvulc.png" width="48" alt="Vulcan" title="ARMVULC" /><br/><code>ARMVULC</code> ⬇️<br/><sub>Vulcan</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/armemp.png" width="48" alt="Stunner" title="ARMEMP" /><br/><code>ARMEMP</code> ⬇️<br/><sub>Stunner</sub></td></tr>
</table>


<sub><b>17</b> buildable units across <b>4</b> pages; <b>8</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `ARMACK` — Adv. Construction Kbot

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armack.png" width="80" alt="Adv. Construction Kbot" title="ARMACK" /><br/><sub><code>ARMACK</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/armarad.png" width="48" alt="Advanced Radar Tower" title="ARMARAD" /><br/><code>ARMARAD</code><br/><sub>Advanced Radar Tower</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfus.png" width="48" alt="Fusion Reactor" title="ARMFUS" /><br/><code>ARMFUS</code><br/><sub>Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmoho.png" width="48" alt="Moho Mine" title="ARMMOHO" /><br/><code>ARMMOHO</code><br/><sub>Moho Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armbrtha.png" width="48" alt="Big Bertha" title="ARMBRTHA" /><br/><code>ARMBRTHA</code><br/><sub>Big Bertha</sub></td><td valign="top" align="center"><img src="img/ta-units/armsilo.png" width="48" alt="Retaliator" title="ARMSILO" /><br/><code>ARMSILO</code><br/><sub>Retaliator</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armanni.png" width="48" alt="Annihilator" title="ARMANNI" /><br/><code>ARMANNI</code><br/><sub>Annihilator</sub></td><td valign="top" align="center"><img src="img/ta-units/armamd.png" width="48" alt="Protector" title="ARMAMD" /><br/><code>ARMAMD</code><br/><sub>Protector</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armasp.png" width="48" alt="Air Repair Pad" title="ARMASP" /><br/><code>ARMASP</code><br/><sub>Air Repair Pad</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/armflak.png" width="48" alt="Flakker" title="ARMFLAK" /><br/><code>ARMFLAK</code> ⬇️<br/><sub>Flakker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfort.png" width="48" alt="Fortification Wall" title="ARMFORT" /><br/><code>ARMFORT</code> ⬇️<br/><sub>Fortification Wall</sub></td><td valign="top" align="center"><img src="img/ta-units/armamb.png" width="48" alt="Ambusher" title="ARMAMB" /><br/><code>ARMAMB</code> ⬇️<br/><sub>Ambusher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armckfus.png" width="48" alt="Cloakable Fusion Reactor" title="ARMCKFUS" /><br/><code>ARMCKFUS</code> ⬇️<br/><sub>Cloakable Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmmkr.png" width="48" alt="Moho Metal Maker" title="ARMMMKR" /><br/><code>ARMMMKR</code> ⬇️<br/><sub>Moho Metal Maker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armtarg.png" width="48" alt="Targeting Facility" title="ARMTARG" /><br/><code>ARMTARG</code> ⬇️<br/><sub>Targeting Facility</sub></td><td valign="top" align="center"><img src="img/ta-units/armvulc.png" width="48" alt="Vulcan" title="ARMVULC" /><br/><code>ARMVULC</code> ⬇️<br/><sub>Vulcan</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/armemp.png" width="48" alt="Stunner" title="ARMEMP" /><br/><code>ARMEMP</code> ⬇️<br/><sub>Stunner</sub></td></tr>
</table>


<sub><b>17</b> buildable units across <b>4</b> pages; <b>8</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `ARMACSUB` — Advanced Construction Sub

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armacsub.png" width="80" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><sub><code>ARMACSUB</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td><td valign="top" align="center"><img src="img/ta-units/armason.png" width="48" alt="Advanced Sonar Station" title="ARMASON" /><br/><code>ARMASON</code><br/><sub>Advanced Sonar Station</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armuwfus.png" width="48" alt="Underwater Fusion Plant" title="ARMUWFUS" /><br/><code>ARMUWFUS</code><br/><sub>Underwater Fusion Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armatl.png" width="48" alt="Advanced Torpedo Launcher" title="ARMATL" /><br/><code>ARMATL</code><br/><sub>Advanced Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armplat.png" width="48" alt="Seaplane Platform" title="ARMPLAT" /><br/><code>ARMPLAT</code><br/><sub>Seaplane Platform</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>5</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `ARMACV` — Adv. Construction Vehicle

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armacv.png" width="80" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><sub><code>ARMACV</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/armarad.png" width="48" alt="Advanced Radar Tower" title="ARMARAD" /><br/><code>ARMARAD</code><br/><sub>Advanced Radar Tower</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfus.png" width="48" alt="Fusion Reactor" title="ARMFUS" /><br/><code>ARMFUS</code><br/><sub>Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmoho.png" width="48" alt="Moho Mine" title="ARMMOHO" /><br/><code>ARMMOHO</code><br/><sub>Moho Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armbrtha.png" width="48" alt="Big Bertha" title="ARMBRTHA" /><br/><code>ARMBRTHA</code><br/><sub>Big Bertha</sub></td><td valign="top" align="center"><img src="img/ta-units/armsilo.png" width="48" alt="Retaliator" title="ARMSILO" /><br/><code>ARMSILO</code><br/><sub>Retaliator</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armanni.png" width="48" alt="Annihilator" title="ARMANNI" /><br/><code>ARMANNI</code><br/><sub>Annihilator</sub></td><td valign="top" align="center"><img src="img/ta-units/armamd.png" width="48" alt="Protector" title="ARMAMD" /><br/><code>ARMAMD</code><br/><sub>Protector</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armasp.png" width="48" alt="Air Repair Pad" title="ARMASP" /><br/><code>ARMASP</code><br/><sub>Air Repair Pad</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/armflak.png" width="48" alt="Flakker" title="ARMFLAK" /><br/><code>ARMFLAK</code> ⬇️<br/><sub>Flakker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfort.png" width="48" alt="Fortification Wall" title="ARMFORT" /><br/><code>ARMFORT</code> ⬇️<br/><sub>Fortification Wall</sub></td><td valign="top" align="center"><img src="img/ta-units/armamb.png" width="48" alt="Ambusher" title="ARMAMB" /><br/><code>ARMAMB</code> ⬇️<br/><sub>Ambusher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armckfus.png" width="48" alt="Cloakable Fusion Reactor" title="ARMCKFUS" /><br/><code>ARMCKFUS</code> ⬇️<br/><sub>Cloakable Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/armmmkr.png" width="48" alt="Moho Metal Maker" title="ARMMMKR" /><br/><code>ARMMMKR</code> ⬇️<br/><sub>Moho Metal Maker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armtarg.png" width="48" alt="Targeting Facility" title="ARMTARG" /><br/><code>ARMTARG</code> ⬇️<br/><sub>Targeting Facility</sub></td><td valign="top" align="center"><img src="img/ta-units/armvulc.png" width="48" alt="Vulcan" title="ARMVULC" /><br/><code>ARMVULC</code> ⬇️<br/><sub>Vulcan</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/armemp.png" width="48" alt="Stunner" title="ARMEMP" /><br/><code>ARMEMP</code> ⬇️<br/><sub>Stunner</sub></td></tr>
</table>


<sub><b>17</b> buildable units across <b>4</b> pages; <b>8</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>



### Arm — Utility (mine layers, hover pads)

#### `ARMHP` — Hovercraft Platform

_Builds Hovercraft_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armhp.png" width="80" alt="Hovercraft Platform" title="ARMHP" /><br/><sub><code>ARMHP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center"><img src="img/ta-units/armsh.png" width="48" alt="Skimmer" title="ARMSH" /><br/><code>ARMSH</code><br/><sub>Skimmer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armanac.png" width="48" alt="Anaconda" title="ARMANAC" /><br/><code>ARMANAC</code><br/><sub>Anaconda</sub></td><td valign="top" align="center"><img src="img/ta-units/armah.png" width="48" alt="Swatter" title="ARMAH" /><br/><code>ARMAH</code><br/><sub>Swatter</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmh.png" width="48" alt="Wombat" title="ARMMH" /><br/><code>ARMMH</code><br/><sub>Wombat</sub></td><td valign="top" align="center"><img src="img/ta-units/armthovr.png" width="48" alt="Bear" title="ARMTHOVR" /><br/><code>ARMTHOVR</code><br/><sub>Bear</sub></td></tr>
</table>


<sub><b>6</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `ARMMLV` — Podger

_Mine Layer Vehicle_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armmlv.png" width="80" alt="Podger" title="ARMMLV" /><br/><sub><code>ARMMLV</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmine1.png" width="48" alt="Tiny" title="ARMMINE1" /><br/><code>ARMMINE1</code><br/><sub>Tiny</sub></td><td valign="top" align="center"><img src="img/ta-units/armmine2.png" width="48" alt="Area Mine" title="ARMMINE2" /><br/><code>ARMMINE2</code><br/><sub>Area Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmine3.png" width="48" alt="Focused Mine" title="ARMMINE3" /><br/><code>ARMMINE3</code><br/><sub>Focused Mine</sub></td><td valign="top" align="center"><img src="img/ta-units/armmine4.png" width="48" alt="HE Area Mine" title="ARMMINE4" /><br/><code>ARMMINE4</code><br/><sub>HE Area Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmine5.png" width="48" alt="Precision Mine" title="ARMMINE5" /><br/><code>ARMMINE5</code><br/><sub>Precision Mine</sub></td><td valign="top" align="center"><img src="img/ta-units/armmine6.png" width="48" alt="Nuclear Mine" title="ARMMINE6" /><br/><code>ARMMINE6</code><br/><sub>Nuclear Mine</sub></td></tr>
</table>


<sub><b>6</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>



### Arm — Advanced factories (tier 2)

#### `ARMAAP` — Adv. Aircraft Plant

_Produces Aircraft_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armaap.png" width="80" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><sub><code>ARMAAP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center"><img src="img/ta-units/armbrawl.png" width="48" alt="Brawler" title="ARMBRAWL" /><br/><code>ARMBRAWL</code><br/><sub>Brawler</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armpnix.png" width="48" alt="Phoenix" title="ARMPNIX" /><br/><code>ARMPNIX</code><br/><sub>Phoenix</sub></td><td valign="top" align="center"><img src="img/ta-units/armlance.png" width="48" alt="Lancet" title="ARMLANCE" /><br/><code>ARMLANCE</code><br/><sub>Lancet</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armhawk.png" width="48" alt="Hawk" title="ARMHAWK" /><br/><code>ARMHAWK</code><br/><sub>Hawk</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armawac.png" width="48" alt="Eagle" title="ARMAWAC" /><br/><code>ARMAWAC</code> ⬇️<br/><sub>Eagle</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>6</b> buildable units across <b>2</b> pages; <b>1</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `ARMALAB` — Adv. Kbot Lab

_Produces Kbots_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armalab.png" width="80" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><sub><code>ARMALAB</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center"><img src="img/ta-units/armzeus.png" width="48" alt="Zeus" title="ARMZEUS" /><br/><code>ARMZEUS</code><br/><sub>Zeus</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfido.png" width="48" alt="Fido" title="ARMFIDO" /><br/><code>ARMFIDO</code><br/><sub>Fido</sub></td><td valign="top" align="center"><img src="img/ta-units/armvader.png" width="48" alt="Invader" title="ARMVADER" /><br/><code>ARMVADER</code><br/><sub>Invader</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armaser.png" width="48" alt="Eraser" title="ARMASER" /><br/><code>ARMASER</code><br/><sub>Eraser</sub></td><td valign="top" align="center"><img src="img/ta-units/armfast.png" width="48" alt="Zipper" title="ARMFAST" /><br/><code>ARMFAST</code><br/><sub>Zipper</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmav.png" width="48" alt="Maverick" title="ARMMAV" /><br/><code>ARMMAV</code> ⬇️<br/><sub>Maverick</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmark.png" width="48" alt="Marky" title="ARMMARK" /><br/><code>ARMMARK</code> ⬇️<br/><sub>Marky</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armamph.png" width="48" alt="Pelican" title="ARMAMPH" /><br/><code>ARMAMPH</code> ⬇️<br/><sub>Pelican</sub></td><td valign="top" align="center"><img src="img/ta-units/armsnipe.png" width="48" alt="Shooter" title="ARMSNIPE" /><br/><code>ARMSNIPE</code> ⬇️<br/><sub>Shooter</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armspy.png" width="48" alt="Infiltrator" title="ARMSPY" /><br/><code>ARMSPY</code> ⬇️<br/><sub>Infiltrator</sub></td><td valign="top" align="center"><img src="img/ta-units/armdecom.png" width="48" alt="Decoy Commander" title="ARMDECOM" /><br/><code>ARMDECOM</code> ⬇️<br/><sub>Decoy Commander</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armfark.png" width="48" alt="FARK" title="ARMFARK" /><br/><code>ARMFARK</code> ⬇️<br/><sub>FARK</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>13</b> buildable units across <b>3</b> pages; <b>7</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `ARMASY` — Adv. Shipyard

_Produces Ships_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armasy.png" width="80" alt="Adv. Shipyard" title="ARMASY" /><br/><sub><code>ARMASY</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armacsub.png" width="48" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><code>ARMACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td valign="top" align="center"><img src="img/ta-units/armcarry.png" width="48" alt="Colossus" title="ARMCARRY" /><br/><code>ARMCARRY</code><br/><sub>Colossus</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsubk.png" width="48" alt="Piranha" title="ARMSUBK" /><br/><code>ARMSUBK</code><br/><sub>Piranha</sub></td><td valign="top" align="center"><img src="img/ta-units/armmship.png" width="48" alt="Ranger" title="ARMMSHIP" /><br/><code>ARMMSHIP</code><br/><sub>Ranger</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armcrus.png" width="48" alt="Conqueror" title="ARMCRUS" /><br/><code>ARMCRUS</code><br/><sub>Conqueror</sub></td><td valign="top" align="center"><img src="img/ta-units/armbats.png" width="48" alt="Millenium" title="ARMBATS" /><br/><code>ARMBATS</code><br/><sub>Millenium</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armsjam.png" width="48" alt="Escort" title="ARMSJAM" /><br/><code>ARMSJAM</code> ⬇️<br/><sub>Escort</sub></td><td valign="top" align="center"><img src="img/ta-units/armaas.png" width="48" alt="Archer" title="ARMAAS" /><br/><code>ARMAAS</code> ⬇️<br/><sub>Archer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armscram.png" width="48" alt="Fibber" title="ARMSCRAM" /><br/><code>ARMSCRAM</code> ⬇️<br/><sub>Fibber</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>9</b> buildable units across <b>2</b> pages; <b>3</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `ARMAVP` — Adv. Vehicle Plant

_Produces Vehicles_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/armavp.png" width="80" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><sub><code>ARMAVP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td valign="top" align="center"><img src="img/ta-units/armcroc.png" width="48" alt="Triton" title="ARMCROC" /><br/><code>ARMCROC</code><br/><sub>Triton</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armbull.png" width="48" alt="Bulldog" title="ARMBULL" /><br/><code>ARMBULL</code><br/><sub>Bulldog</sub></td><td valign="top" align="center"><img src="img/ta-units/armjam.png" width="48" alt="Jammer" title="ARMJAM" /><br/><code>ARMJAM</code><br/><sub>Jammer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmart.png" width="48" alt="Luger" title="ARMMART" /><br/><code>ARMMART</code><br/><sub>Luger</sub></td><td valign="top" align="center"><img src="img/ta-units/armspid.png" width="48" alt="Spider" title="ARMSPID" /><br/><code>ARMSPID</code><br/><sub>Spider</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armseer.png" width="48" alt="Seer" title="ARMSEER" /><br/><code>ARMSEER</code><br/><sub>Seer</sub></td><td valign="top" align="center"><img src="img/ta-units/armmerl.png" width="48" alt="Merl" title="ARMMERL" /><br/><code>ARMMERL</code><br/><sub>Merl</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armmanni.png" width="48" alt="Penetrator" title="ARMMANNI" /><br/><code>ARMMANNI</code> ⬇️<br/><sub>Penetrator</sub></td><td valign="top" align="center"><img src="img/ta-units/armyork.png" width="48" alt="Phalanx" title="ARMYORK" /><br/><code>ARMYORK</code> ⬇️<br/><sub>Phalanx</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/armscab.png" width="48" alt="Scarab" title="ARMSCAB" /><br/><code>ARMSCAB</code> ⬇️<br/><sub>Scarab</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/armlatnk.png" width="48" alt="Panther" title="ARMLATNK" /><br/><code>ARMLATNK</code> ⬇️<br/><sub>Panther</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>12</b> buildable units across <b>4</b> pages; <b>4</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


---

## CORE

23 builders across 7 tiers.


### Core — Commander

#### `CORCOM` — Commander

_Commander_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corcom.png" width="80" alt="Commander" title="CORCOM" /><br/><sub><code>CORCOM</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsolar.png" width="48" alt="Solar Collector" title="CORSOLAR" /><br/><code>CORSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/corwin.png" width="48" alt="Wind Generator" title="CORWIN" /><br/><code>CORWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corestor.png" width="48" alt="Energy Storage" title="CORESTOR" /><br/><code>CORESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/cormstor.png" width="48" alt="Metal Storage" title="CORMSTOR" /><br/><code>CORMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormex.png" width="48" alt="Metal Extractor" title="CORMEX" /><br/><code>CORMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormakr.png" width="48" alt="Metal Maker" title="CORMAKR" /><br/><code>CORMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corllt.png" width="48" alt="Light Laser Tower" title="CORLLT" /><br/><code>CORLLT</code><br/><sub>Light Laser Tower</sub></td><td valign="top" align="center"><img src="img/ta-units/corrad.png" width="48" alt="Radar Tower" title="CORRAD" /><br/><code>CORRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsonar.png" width="48" alt="Sonar Station" title="CORSONAR" /><br/><code>CORSONAR</code><br/><sub>Sonar Station</sub></td><td valign="top" align="center"><img src="img/ta-units/cortide.png" width="48" alt="Tidal Generator" title="CORTIDE" /><br/><code>CORTIDE</code><br/><sub>Tidal Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coruwes.png" width="48" alt="Underwater Energy Storage" title="CORUWES" /><br/><code>CORUWES</code><br/><sub>Underwater Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/coruwms.png" width="48" alt="Underwater Metal Storage" title="CORUWMS" /><br/><code>CORUWMS</code><br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coruwmex.png" width="48" alt="Underwater Metal Extractor" title="CORUWMEX" /><br/><code>CORUWMEX</code><br/><sub>Underwater Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/corfmkr.png" width="48" alt="Floating Metal Maker" title="CORFMKR" /><br/><code>CORFMKR</code><br/><sub>Floating Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/cortl.png" width="48" alt="Torpedo Launcher" title="CORTL" /><br/><code>CORTL</code><br/><sub>Torpedo Launcher</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/corplas.png" width="48" alt="Immolator; //c" title="CORPLAS" /><br/><code>CORPLAS</code> ⬇️<br/><sub>Immolator; //c</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>20</b> buildable units across <b>5</b> pages; <b>1</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>



### Core — Basic factories (tier 1)

#### `CORAP` — Aircraft Plant

_Produces Aircraft_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corap.png" width="80" alt="Aircraft Plant" title="CORAP" /><br/><sub><code>CORAP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center"><img src="img/ta-units/corfink.png" width="48" alt="Fink" title="CORFINK" /><br/><code>CORFINK</code><br/><sub>Fink</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corveng.png" width="48" alt="Avenger" title="CORVENG" /><br/><code>CORVENG</code><br/><sub>Avenger</sub></td><td valign="top" align="center"><img src="img/ta-units/corshad.png" width="48" alt="Shadow" title="CORSHAD" /><br/><code>CORSHAD</code><br/><sub>Shadow</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corvalk.png" width="48" alt="Valkyrie" title="CORVALK" /><br/><code>CORVALK</code><br/><sub>Valkyrie</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>5</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `CORLAB` — Kbot Lab

_Produces Kbots_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corlab.png" width="80" alt="Kbot Lab" title="CORLAB" /><br/><sub><code>CORLAB</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center"><img src="img/ta-units/corak.png" width="48" alt="A.K." title="CORAK" /><br/><code>CORAK</code><br/><sub>A.K.</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corstorm.png" width="48" alt="Storm" title="CORSTORM" /><br/><code>CORSTORM</code><br/><sub>Storm</sub></td><td valign="top" align="center"><img src="img/ta-units/corthud.png" width="48" alt="Thud" title="CORTHUD" /><br/><code>CORTHUD</code><br/><sub>Thud</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corcrash.png" width="48" alt="Crasher" title="CORCRASH" /><br/><code>CORCRASH</code><br/><sub>Crasher</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>5</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `CORSY` — Shipyard

_Produces Ships_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corsy.png" width="80" alt="Shipyard" title="CORSY" /><br/><sub><code>CORSY</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center"><img src="img/ta-units/corpt.png" width="48" alt="Searcher" title="CORPT" /><br/><code>CORPT</code><br/><sub>Searcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corroy.png" width="48" alt="Enforcer" title="CORROY" /><br/><code>CORROY</code><br/><sub>Enforcer</sub></td><td valign="top" align="center"><img src="img/ta-units/cortship.png" width="48" alt="Envoy" title="CORTSHIP" /><br/><code>CORTSHIP</code><br/><sub>Envoy</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsub.png" width="48" alt="Snake" title="CORSUB" /><br/><code>CORSUB</code><br/><sub>Snake</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>5</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `CORVP` — Vehicle Plant

_Produces Vehicles_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corvp.png" width="80" alt="Vehicle Plant" title="CORVP" /><br/><sub><code>CORVP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td valign="top" align="center"><img src="img/ta-units/corfav.png" width="48" alt="Weasel" title="CORFAV" /><br/><code>CORFAV</code><br/><sub>Weasel</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corgator.png" width="48" alt="Instigator" title="CORGATOR" /><br/><code>CORGATOR</code><br/><sub>Instigator</sub></td><td valign="top" align="center"><img src="img/ta-units/corraid.png" width="48" alt="Raider" title="CORRAID" /><br/><code>CORRAID</code><br/><sub>Raider</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormist.png" width="48" alt="Slasher" title="CORMIST" /><br/><code>CORMIST</code><br/><sub>Slasher</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/cormlv.png" width="48" alt="Spoiler" title="CORMLV" /><br/><code>CORMLV</code> ⬇️<br/><sub>Spoiler</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlevlr.png" width="48" alt="Leveler" title="CORLEVLR" /><br/><code>CORLEVLR</code> ⬇️<br/><sub>Leveler</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>7</b> buildable units across <b>3</b> pages; <b>2</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>



### Core — Construction units (mobile, tier 1)

#### `CORCA` — Construction Aircraft

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corca.png" width="80" alt="Construction Aircraft" title="CORCA" /><br/><sub><code>CORCA</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsolar.png" width="48" alt="Solar Collector" title="CORSOLAR" /><br/><code>CORSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/corwin.png" width="48" alt="Wind Generator" title="CORWIN" /><br/><code>CORWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corestor.png" width="48" alt="Energy Storage" title="CORESTOR" /><br/><code>CORESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/cormstor.png" width="48" alt="Metal Storage" title="CORMSTOR" /><br/><code>CORMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormex.png" width="48" alt="Metal Extractor" title="CORMEX" /><br/><code>CORMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormakr.png" width="48" alt="Metal Maker" title="CORMAKR" /><br/><code>CORMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corllt.png" width="48" alt="Light Laser Tower" title="CORLLT" /><br/><code>CORLLT</code><br/><sub>Light Laser Tower</sub></td><td valign="top" align="center"><img src="img/ta-units/corrad.png" width="48" alt="Radar Tower" title="CORRAD" /><br/><code>CORRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/coraap.png" width="48" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><code>CORAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corgeo.png" width="48" alt="Geothermal Powerplant" title="CORGEO" /><br/><code>CORGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhlt.png" width="48" alt="Gaat Gun" title="CORHLT" /><br/><code>CORHLT</code><br/><sub>Gaat Gun</sub></td><td valign="top" align="center"><img src="img/ta-units/corrl.png" width="48" alt="Pulverizer" title="CORRL" /><br/><code>CORRL</code><br/><sub>Pulverizer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cordrag.png" width="48" alt="Dragon&#39;s Teeth" title="CORDRAG" /><br/><code>CORDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/corpun.png" width="48" alt="Punisher" title="CORPUN" /><br/><code>CORPUN</code><br/><sub>Punisher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center"><img src="img/ta-units/corvipe.png" width="48" alt="Viper" title="CORVIPE" /><br/><code>CORVIPE</code><br/><sub>Viper</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corplas.png" width="48" alt="Immolator; //c" title="CORPLAS" /><br/><code>CORPLAS</code> ⬇️<br/><sub>Immolator; //c</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>21</b> buildable units across <b>5</b> pages; <b>1</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORCH` — Construction Hovercraft

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corch.png" width="80" alt="Construction Hovercraft" title="CORCH" /><br/><sub><code>CORCH</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsolar.png" width="48" alt="Solar Collector" title="CORSOLAR" /><br/><code>CORSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/corwin.png" width="48" alt="Wind Generator" title="CORWIN" /><br/><code>CORWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corestor.png" width="48" alt="Energy Storage" title="CORESTOR" /><br/><code>CORESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/cormstor.png" width="48" alt="Metal Storage" title="CORMSTOR" /><br/><code>CORMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormex.png" width="48" alt="Metal Extractor" title="CORMEX" /><br/><code>CORMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormakr.png" width="48" alt="Metal Maker" title="CORMAKR" /><br/><code>CORMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corllt.png" width="48" alt="Light Laser Tower" title="CORLLT" /><br/><code>CORLLT</code><br/><sub>Light Laser Tower</sub></td><td valign="top" align="center"><img src="img/ta-units/corrad.png" width="48" alt="Radar Tower" title="CORRAD" /><br/><code>CORRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corgeo.png" width="48" alt="Geothermal Powerplant" title="CORGEO" /><br/><code>CORGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhlt.png" width="48" alt="Gaat Gun" title="CORHLT" /><br/><code>CORHLT</code><br/><sub>Gaat Gun</sub></td><td valign="top" align="center"><img src="img/ta-units/corrl.png" width="48" alt="Pulverizer" title="CORRL" /><br/><code>CORRL</code><br/><sub>Pulverizer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cordrag.png" width="48" alt="Dragon&#39;s Teeth" title="CORDRAG" /><br/><code>CORDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/corpun.png" width="48" alt="Punisher" title="CORPUN" /><br/><code>CORPUN</code><br/><sub>Punisher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsonar.png" width="48" alt="Sonar Station" title="CORSONAR" /><br/><code>CORSONAR</code><br/><sub>Sonar Station</sub></td><td valign="top" align="center"><img src="img/ta-units/cortide.png" width="48" alt="Tidal Generator" title="CORTIDE" /><br/><code>CORTIDE</code><br/><sub>Tidal Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coruwes.png" width="48" alt="Underwater Energy Storage" title="CORUWES" /><br/><code>CORUWES</code><br/><sub>Underwater Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/coruwms.png" width="48" alt="Underwater Metal Storage" title="CORUWMS" /><br/><code>CORUWMS</code><br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coruwmex.png" width="48" alt="Underwater Metal Extractor" title="CORUWMEX" /><br/><code>CORUWMEX</code><br/><sub>Underwater Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/corfmkr.png" width="48" alt="Floating Metal Maker" title="CORFMKR" /><br/><code>CORFMKR</code><br/><sub>Floating Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfrt.png" width="48" alt="Stinger" title="CORFRT" /><br/><code>CORFRT</code><br/><sub>Stinger</sub></td><td valign="top" align="center"><img src="img/ta-units/corfdrag.png" width="48" alt="Floating Dragon&#39;s Teeth" title="CORFDRAG" /><br/><code>CORFDRAG</code><br/><sub>Floating Dragon&#39;s Teeth</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfhlt.png" width="48" alt="Thunderbolt" title="CORFHLT" /><br/><code>CORFHLT</code><br/><sub>Thunderbolt</sub></td><td valign="top" align="center"><img src="img/ta-units/cortl.png" width="48" alt="Torpedo Launcher" title="CORTL" /><br/><code>CORTL</code><br/><sub>Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center"><img src="img/ta-units/corvipe.png" width="48" alt="Viper" title="CORVIPE" /><br/><code>CORVIPE</code><br/><sub>Viper</sub></td></tr>
</table>


<sub><b>30</b> buildable units across <b>5</b> pages.</sub>
</td>
</tr>
</table>


#### `CORCK` — Construction Kbot

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corck.png" width="80" alt="Construction Kbot" title="CORCK" /><br/><sub><code>CORCK</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsolar.png" width="48" alt="Solar Collector" title="CORSOLAR" /><br/><code>CORSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/corwin.png" width="48" alt="Wind Generator" title="CORWIN" /><br/><code>CORWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corestor.png" width="48" alt="Energy Storage" title="CORESTOR" /><br/><code>CORESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/cormstor.png" width="48" alt="Metal Storage" title="CORMSTOR" /><br/><code>CORMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormex.png" width="48" alt="Metal Extractor" title="CORMEX" /><br/><code>CORMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormakr.png" width="48" alt="Metal Maker" title="CORMAKR" /><br/><code>CORMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corllt.png" width="48" alt="Light Laser Tower" title="CORLLT" /><br/><code>CORLLT</code><br/><sub>Light Laser Tower</sub></td><td valign="top" align="center"><img src="img/ta-units/corrad.png" width="48" alt="Radar Tower" title="CORRAD" /><br/><code>CORRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corgeo.png" width="48" alt="Geothermal Powerplant" title="CORGEO" /><br/><code>CORGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhlt.png" width="48" alt="Gaat Gun" title="CORHLT" /><br/><code>CORHLT</code><br/><sub>Gaat Gun</sub></td><td valign="top" align="center"><img src="img/ta-units/corrl.png" width="48" alt="Pulverizer" title="CORRL" /><br/><code>CORRL</code><br/><sub>Pulverizer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cordrag.png" width="48" alt="Dragon&#39;s Teeth" title="CORDRAG" /><br/><code>CORDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/corpun.png" width="48" alt="Punisher" title="CORPUN" /><br/><code>CORPUN</code><br/><sub>Punisher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center"><img src="img/ta-units/corvipe.png" width="48" alt="Viper" title="CORVIPE" /><br/><code>CORVIPE</code><br/><sub>Viper</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corplas.png" width="48" alt="Immolator; //c" title="CORPLAS" /><br/><code>CORPLAS</code> ⬇️<br/><sub>Immolator; //c</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>21</b> buildable units across <b>5</b> pages; <b>1</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORCS` — Construction Ship

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corcs.png" width="80" alt="Construction Ship" title="CORCS" /><br/><sub><code>CORCS</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td valign="top" align="center"><img src="img/ta-units/cortl.png" width="48" alt="Torpedo Launcher" title="CORTL" /><br/><code>CORTL</code><br/><sub>Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cortide.png" width="48" alt="Tidal Generator" title="CORTIDE" /><br/><code>CORTIDE</code><br/><sub>Tidal Generator</sub></td><td valign="top" align="center"><img src="img/ta-units/corsonar.png" width="48" alt="Sonar Station" title="CORSONAR" /><br/><code>CORSONAR</code><br/><sub>Sonar Station</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfrt.png" width="48" alt="Stinger" title="CORFRT" /><br/><code>CORFRT</code> ⬇️<br/><sub>Stinger</sub></td><td valign="top" align="center"><img src="img/ta-units/coruwes.png" width="48" alt="Underwater Energy Storage" title="CORUWES" /><br/><code>CORUWES</code> ⬇️<br/><sub>Underwater Energy Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfmkr.png" width="48" alt="Floating Metal Maker" title="CORFMKR" /><br/><code>CORFMKR</code> ⬇️<br/><sub>Floating Metal Maker</sub></td><td valign="top" align="center"><img src="img/ta-units/coruwms.png" width="48" alt="Underwater Metal Storage" title="CORUWMS" /><br/><code>CORUWMS</code> ⬇️<br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfhlt.png" width="48" alt="Thunderbolt" title="CORFHLT" /><br/><code>CORFHLT</code> ⬇️<br/><sub>Thunderbolt</sub></td><td valign="top" align="center"><img src="img/ta-units/coruwmex.png" width="48" alt="Underwater Metal Extractor" title="CORUWMEX" /><br/><code>CORUWMEX</code> ⬇️<br/><sub>Underwater Metal Extractor</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfdrag.png" width="48" alt="Floating Dragon&#39;s Teeth" title="CORFDRAG" /><br/><code>CORFDRAG</code> ⬇️<br/><sub>Floating Dragon&#39;s Teeth</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>11</b> buildable units across <b>3</b> pages; <b>7</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORCSA` — Construction Seaplane

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corcsa.png" width="80" alt="Construction Seaplane" title="CORCSA" /><br/><sub><code>CORCSA</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsolar.png" width="48" alt="Solar Collector" title="CORSOLAR" /><br/><code>CORSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/corwin.png" width="48" alt="Wind Generator" title="CORWIN" /><br/><code>CORWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corestor.png" width="48" alt="Energy Storage" title="CORESTOR" /><br/><code>CORESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/cormstor.png" width="48" alt="Metal Storage" title="CORMSTOR" /><br/><code>CORMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormex.png" width="48" alt="Metal Extractor" title="CORMEX" /><br/><code>CORMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormakr.png" width="48" alt="Metal Maker" title="CORMAKR" /><br/><code>CORMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corllt.png" width="48" alt="Light Laser Tower" title="CORLLT" /><br/><code>CORLLT</code><br/><sub>Light Laser Tower</sub></td><td valign="top" align="center"><img src="img/ta-units/corrad.png" width="48" alt="Radar Tower" title="CORRAD" /><br/><code>CORRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corgeo.png" width="48" alt="Geothermal Powerplant" title="CORGEO" /><br/><code>CORGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhlt.png" width="48" alt="Gaat Gun" title="CORHLT" /><br/><code>CORHLT</code><br/><sub>Gaat Gun</sub></td><td valign="top" align="center"><img src="img/ta-units/corrl.png" width="48" alt="Pulverizer" title="CORRL" /><br/><code>CORRL</code><br/><sub>Pulverizer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cordrag.png" width="48" alt="Dragon&#39;s Teeth" title="CORDRAG" /><br/><code>CORDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/corpun.png" width="48" alt="Punisher" title="CORPUN" /><br/><code>CORPUN</code><br/><sub>Punisher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsonar.png" width="48" alt="Sonar Station" title="CORSONAR" /><br/><code>CORSONAR</code><br/><sub>Sonar Station</sub></td><td valign="top" align="center"><img src="img/ta-units/cortide.png" width="48" alt="Tidal Generator" title="CORTIDE" /><br/><code>CORTIDE</code><br/><sub>Tidal Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coruwes.png" width="48" alt="Underwater Energy Storage" title="CORUWES" /><br/><code>CORUWES</code><br/><sub>Underwater Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/coruwms.png" width="48" alt="Underwater Metal Storage" title="CORUWMS" /><br/><code>CORUWMS</code><br/><sub>Underwater Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coruwmex.png" width="48" alt="Underwater Metal Extractor" title="CORUWMEX" /><br/><code>CORUWMEX</code><br/><sub>Underwater Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/corfmkr.png" width="48" alt="Floating Metal Maker" title="CORFMKR" /><br/><code>CORFMKR</code><br/><sub>Floating Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfrt.png" width="48" alt="Stinger" title="CORFRT" /><br/><code>CORFRT</code><br/><sub>Stinger</sub></td><td valign="top" align="center"><img src="img/ta-units/corfdrag.png" width="48" alt="Floating Dragon&#39;s Teeth" title="CORFDRAG" /><br/><code>CORFDRAG</code><br/><sub>Floating Dragon&#39;s Teeth</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfhlt.png" width="48" alt="Thunderbolt" title="CORFHLT" /><br/><code>CORFHLT</code><br/><sub>Thunderbolt</sub></td><td valign="top" align="center"><img src="img/ta-units/cortl.png" width="48" alt="Torpedo Launcher" title="CORTL" /><br/><code>CORTL</code><br/><sub>Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center"><img src="img/ta-units/corvipe.png" width="48" alt="Viper" title="CORVIPE" /><br/><code>CORVIPE</code><br/><sub>Viper</sub></td></tr>
</table>


<sub><b>30</b> buildable units across <b>5</b> pages.</sub>
</td>
</tr>
</table>


#### `CORCV` — Construction Vehicle

_Tech Level 1_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corcv.png" width="80" alt="Construction Vehicle" title="CORCV" /><br/><sub><code>CORCV</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsolar.png" width="48" alt="Solar Collector" title="CORSOLAR" /><br/><code>CORSOLAR</code><br/><sub>Solar Collector</sub></td><td valign="top" align="center"><img src="img/ta-units/corwin.png" width="48" alt="Wind Generator" title="CORWIN" /><br/><code>CORWIN</code><br/><sub>Wind Generator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corestor.png" width="48" alt="Energy Storage" title="CORESTOR" /><br/><code>CORESTOR</code><br/><sub>Energy Storage</sub></td><td valign="top" align="center"><img src="img/ta-units/cormstor.png" width="48" alt="Metal Storage" title="CORMSTOR" /><br/><code>CORMSTOR</code><br/><sub>Metal Storage</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormex.png" width="48" alt="Metal Extractor" title="CORMEX" /><br/><code>CORMEX</code><br/><sub>Metal Extractor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormakr.png" width="48" alt="Metal Maker" title="CORMAKR" /><br/><code>CORMAKR</code><br/><sub>Metal Maker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corllt.png" width="48" alt="Light Laser Tower" title="CORLLT" /><br/><code>CORLLT</code><br/><sub>Light Laser Tower</sub></td><td valign="top" align="center"><img src="img/ta-units/corrad.png" width="48" alt="Radar Tower" title="CORRAD" /><br/><code>CORRAD</code><br/><sub>Radar Tower</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corgeo.png" width="48" alt="Geothermal Powerplant" title="CORGEO" /><br/><code>CORGEO</code><br/><sub>Geothermal Powerplant</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhlt.png" width="48" alt="Gaat Gun" title="CORHLT" /><br/><code>CORHLT</code><br/><sub>Gaat Gun</sub></td><td valign="top" align="center"><img src="img/ta-units/corrl.png" width="48" alt="Pulverizer" title="CORRL" /><br/><code>CORRL</code><br/><sub>Pulverizer</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cordrag.png" width="48" alt="Dragon&#39;s Teeth" title="CORDRAG" /><br/><code>CORDRAG</code><br/><sub>Dragon&#39;s Teeth</sub></td><td valign="top" align="center"><img src="img/ta-units/corpun.png" width="48" alt="Punisher" title="CORPUN" /><br/><code>CORPUN</code><br/><sub>Punisher</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td valign="top" align="center"><img src="img/ta-units/corvipe.png" width="48" alt="Viper" title="CORVIPE" /><br/><code>CORVIPE</code><br/><sub>Viper</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 5</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corplas.png" width="48" alt="Immolator; //c" title="CORPLAS" /><br/><code>CORPLAS</code> ⬇️<br/><sub>Immolator; //c</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>21</b> buildable units across <b>5</b> pages; <b>1</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORPLAT` — Seaplane Platform

_Builds Seaplanes_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corplat.png" width="80" alt="Seaplane Platform" title="CORPLAT" /><br/><sub><code>CORPLAT</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center"><img src="img/ta-units/corhunt.png" width="48" alt="Hunter" title="CORHUNT" /><br/><code>CORHUNT</code><br/><sub>Hunter</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsfig.png" width="48" alt="Voodoo" title="CORSFIG" /><br/><code>CORSFIG</code><br/><sub>Voodoo</sub></td><td valign="top" align="center"><img src="img/ta-units/corvamp.png" width="48" alt="Vamp" title="CORVAMP" /><br/><code>CORVAMP</code><br/><sub>Vamp</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cortitan.png" width="48" alt="Titan" title="CORTITAN" /><br/><code>CORTITAN</code><br/><sub>Titan</sub></td><td valign="top" align="center"><img src="img/ta-units/corseap.png" width="48" alt="Typhoon" title="CORSEAP" /><br/><code>CORSEAP</code><br/><sub>Typhoon</sub></td></tr>
</table>


<sub><b>6</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>



### Core — Advanced Construction (mobile, tier 2)

#### `CORACA` — Adv. Construction Aircraft

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/coraca.png" width="80" alt="Adv. Construction Aircraft" title="CORACA" /><br/><sub><code>CORACA</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corarad.png" width="48" alt="Advanced Radar Tower" title="CORARAD" /><br/><code>CORARAD</code><br/><sub>Advanced Radar Tower</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfus.png" width="48" alt="Fusion Power Plant" title="CORFUS" /><br/><code>CORFUS</code><br/><sub>Fusion Power Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/cormoho.png" width="48" alt="Moho Mine" title="CORMOHO" /><br/><code>CORMOHO</code><br/><sub>Moho Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corint.png" width="48" alt="Intimidator" title="CORINT" /><br/><code>CORINT</code><br/><sub>Intimidator</sub></td><td valign="top" align="center"><img src="img/ta-units/cordoom.png" width="48" alt="Doomsday Machine" title="CORDOOM" /><br/><code>CORDOOM</code><br/><sub>Doomsday Machine</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsilo.png" width="48" alt="Silencer" title="CORSILO" /><br/><code>CORSILO</code><br/><sub>Silencer</sub></td><td valign="top" align="center"><img src="img/ta-units/corfmd.png" width="48" alt="Fortitude Missile Defense" title="CORFMD" /><br/><code>CORFMD</code><br/><sub>Fortitude Missile Defense</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corasp.png" width="48" alt="Air Repair Pad" title="CORASP" /><br/><code>CORASP</code><br/><sub>Air Repair Pad</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/corflak.png" width="48" alt="Cobra" title="CORFLAK" /><br/><code>CORFLAK</code> ⬇️<br/><sub>Cobra</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfort.png" width="48" alt="Fortification Wall" title="CORFORT" /><br/><code>CORFORT</code> ⬇️<br/><sub>Fortification Wall</sub></td><td valign="top" align="center"><img src="img/ta-units/cortoast.png" width="48" alt="Toaster" title="CORTOAST" /><br/><code>CORTOAST</code> ⬇️<br/><sub>Toaster</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corckfus.png" width="48" alt="Cloakable Fusion Reactor" title="CORCKFUS" /><br/><code>CORCKFUS</code> ⬇️<br/><sub>Cloakable Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormmkr.png" width="48" alt="Moho Metal Maker" title="CORMMKR" /><br/><code>CORMMKR</code> ⬇️<br/><sub>Moho Metal Maker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cortarg.png" width="48" alt="Targeting Facility" title="CORTARG" /><br/><code>CORTARG</code> ⬇️<br/><sub>Targeting Facility</sub></td><td valign="top" align="center"><img src="img/ta-units/corbuzz.png" width="48" alt="Buzzsaw" title="CORBUZZ" /><br/><code>CORBUZZ</code> ⬇️<br/><sub>Buzzsaw</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/cortron.png" width="48" alt="Neutron" title="CORTRON" /><br/><code>CORTRON</code> ⬇️<br/><sub>Neutron</sub></td></tr>
</table>


<sub><b>17</b> buildable units across <b>4</b> pages; <b>8</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORACK` — Adv. Construction Kbot

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corack.png" width="80" alt="Adv. Construction Kbot" title="CORACK" /><br/><sub><code>CORACK</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td valign="top" align="center"><img src="img/ta-units/corarad.png" width="48" alt="Advanced Radar Tower" title="CORARAD" /><br/><code>CORARAD</code><br/><sub>Advanced Radar Tower</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfus.png" width="48" alt="Fusion Power Plant" title="CORFUS" /><br/><code>CORFUS</code><br/><sub>Fusion Power Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/cormoho.png" width="48" alt="Moho Mine" title="CORMOHO" /><br/><code>CORMOHO</code><br/><sub>Moho Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corint.png" width="48" alt="Intimidator" title="CORINT" /><br/><code>CORINT</code><br/><sub>Intimidator</sub></td><td valign="top" align="center"><img src="img/ta-units/cordoom.png" width="48" alt="Doomsday Machine" title="CORDOOM" /><br/><code>CORDOOM</code><br/><sub>Doomsday Machine</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsilo.png" width="48" alt="Silencer" title="CORSILO" /><br/><code>CORSILO</code><br/><sub>Silencer</sub></td><td valign="top" align="center"><img src="img/ta-units/corfmd.png" width="48" alt="Fortitude Missile Defense" title="CORFMD" /><br/><code>CORFMD</code><br/><sub>Fortitude Missile Defense</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corasp.png" width="48" alt="Air Repair Pad" title="CORASP" /><br/><code>CORASP</code><br/><sub>Air Repair Pad</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/corflak.png" width="48" alt="Cobra" title="CORFLAK" /><br/><code>CORFLAK</code> ⬇️<br/><sub>Cobra</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfort.png" width="48" alt="Fortification Wall" title="CORFORT" /><br/><code>CORFORT</code> ⬇️<br/><sub>Fortification Wall</sub></td><td valign="top" align="center"><img src="img/ta-units/cortoast.png" width="48" alt="Toaster" title="CORTOAST" /><br/><code>CORTOAST</code> ⬇️<br/><sub>Toaster</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corckfus.png" width="48" alt="Cloakable Fusion Reactor" title="CORCKFUS" /><br/><code>CORCKFUS</code> ⬇️<br/><sub>Cloakable Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormmkr.png" width="48" alt="Moho Metal Maker" title="CORMMKR" /><br/><code>CORMMKR</code> ⬇️<br/><sub>Moho Metal Maker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cortarg.png" width="48" alt="Targeting Facility" title="CORTARG" /><br/><code>CORTARG</code> ⬇️<br/><sub>Targeting Facility</sub></td><td valign="top" align="center"><img src="img/ta-units/corbuzz.png" width="48" alt="Buzzsaw" title="CORBUZZ" /><br/><code>CORBUZZ</code> ⬇️<br/><sub>Buzzsaw</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corgant.png" width="48" alt="Krogoth Gantry" title="CORGANT" /><br/><code>CORGANT</code> ⬇️<br/><sub>Krogoth Gantry</sub></td><td valign="top" align="center"><img src="img/ta-units/cortron.png" width="48" alt="Neutron" title="CORTRON" /><br/><code>CORTRON</code> ⬇️<br/><sub>Neutron</sub></td></tr>
</table>


<sub><b>18</b> buildable units across <b>4</b> pages; <b>9</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORACSUB` — Advanced Construction Sub

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/coracsub.png" width="80" alt="Advanced Construction Sub" title="CORACSUB" /><br/><sub><code>CORACSUB</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td><td valign="top" align="center"><img src="img/ta-units/corason.png" width="48" alt="Advanced Sonar Station" title="CORASON" /><br/><code>CORASON</code><br/><sub>Advanced Sonar Station</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coruwfus.png" width="48" alt="Underwater Fusion Plant" title="CORUWFUS" /><br/><code>CORUWFUS</code><br/><sub>Underwater Fusion Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/coratl.png" width="48" alt="Advanced Torpedo Launcher" title="CORATL" /><br/><code>CORATL</code><br/><sub>Advanced Torpedo Launcher</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corplat.png" width="48" alt="Seaplane Platform" title="CORPLAT" /><br/><code>CORPLAT</code><br/><sub>Seaplane Platform</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>5</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `CORACV` — Adv. Construction Vehicle

_Tech Level 2_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/coracv.png" width="80" alt="Adv. Construction Vehicle" title="CORACV" /><br/><sub><code>CORACV</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/corarad.png" width="48" alt="Advanced Radar Tower" title="CORARAD" /><br/><code>CORARAD</code><br/><sub>Advanced Radar Tower</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfus.png" width="48" alt="Fusion Power Plant" title="CORFUS" /><br/><code>CORFUS</code><br/><sub>Fusion Power Plant</sub></td><td valign="top" align="center"><img src="img/ta-units/cormoho.png" width="48" alt="Moho Mine" title="CORMOHO" /><br/><code>CORMOHO</code><br/><sub>Moho Mine</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corint.png" width="48" alt="Intimidator" title="CORINT" /><br/><code>CORINT</code><br/><sub>Intimidator</sub></td><td valign="top" align="center"><img src="img/ta-units/cordoom.png" width="48" alt="Doomsday Machine" title="CORDOOM" /><br/><code>CORDOOM</code><br/><sub>Doomsday Machine</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsilo.png" width="48" alt="Silencer" title="CORSILO" /><br/><code>CORSILO</code><br/><sub>Silencer</sub></td><td valign="top" align="center"><img src="img/ta-units/corfmd.png" width="48" alt="Fortitude Missile Defense" title="CORFMD" /><br/><code>CORFMD</code><br/><sub>Fortitude Missile Defense</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corasp.png" width="48" alt="Air Repair Pad" title="CORASP" /><br/><code>CORASP</code><br/><sub>Air Repair Pad</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/corflak.png" width="48" alt="Cobra" title="CORFLAK" /><br/><code>CORFLAK</code> ⬇️<br/><sub>Cobra</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corfort.png" width="48" alt="Fortification Wall" title="CORFORT" /><br/><code>CORFORT</code> ⬇️<br/><sub>Fortification Wall</sub></td><td valign="top" align="center"><img src="img/ta-units/cortoast.png" width="48" alt="Toaster" title="CORTOAST" /><br/><code>CORTOAST</code> ⬇️<br/><sub>Toaster</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corckfus.png" width="48" alt="Cloakable Fusion Reactor" title="CORCKFUS" /><br/><code>CORCKFUS</code> ⬇️<br/><sub>Cloakable Fusion Reactor</sub></td><td valign="top" align="center"><img src="img/ta-units/cormmkr.png" width="48" alt="Moho Metal Maker" title="CORMMKR" /><br/><code>CORMMKR</code> ⬇️<br/><sub>Moho Metal Maker</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cortarg.png" width="48" alt="Targeting Facility" title="CORTARG" /><br/><code>CORTARG</code> ⬇️<br/><sub>Targeting Facility</sub></td><td valign="top" align="center"><img src="img/ta-units/corbuzz.png" width="48" alt="Buzzsaw" title="CORBUZZ" /><br/><code>CORBUZZ</code> ⬇️<br/><sub>Buzzsaw</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/cortron.png" width="48" alt="Neutron" title="CORTRON" /><br/><code>CORTRON</code> ⬇️<br/><sub>Neutron</sub></td></tr>
</table>


<sub><b>17</b> buildable units across <b>4</b> pages; <b>8</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>



### Core — Utility (mine layers, hover pads)

#### `CORHP` — Hovercraft Platform

_Builds Hovercraft_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corhp.png" width="80" alt="Hovercraft Platform" title="CORHP" /><br/><sub><code>CORHP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center"><img src="img/ta-units/corsh.png" width="48" alt="Scrubber" title="CORSH" /><br/><code>CORSH</code><br/><sub>Scrubber</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsnap.png" width="48" alt="Snapper" title="CORSNAP" /><br/><code>CORSNAP</code><br/><sub>Snapper</sub></td><td valign="top" align="center"><img src="img/ta-units/corah.png" width="48" alt="Slinger" title="CORAH" /><br/><code>CORAH</code><br/><sub>Slinger</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormh.png" width="48" alt="Nixer" title="CORMH" /><br/><code>CORMH</code><br/><sub>Nixer</sub></td><td valign="top" align="center"><img src="img/ta-units/corthovr.png" width="48" alt="Turtle" title="CORTHOVR" /><br/><code>CORTHOVR</code><br/><sub>Turtle</sub></td></tr>
</table>


<sub><b>6</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>


#### `CORMLV` — Spoiler

_Mine Layer Vehicle_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/cormlv.png" width="80" alt="Spoiler" title="CORMLV" /><br/><sub><code>CORMLV</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormine1.png" width="48" alt="M-104" title="CORMINE1" /><br/><code>CORMINE1</code><br/><sub>M-104</sub></td><td valign="top" align="center"><img src="img/ta-units/cormine2.png" width="48" alt="M-209" title="CORMINE2" /><br/><code>CORMINE2</code><br/><sub>M-209</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormine3.png" width="48" alt="M-303" title="CORMINE3" /><br/><code>CORMINE3</code><br/><sub>M-303</sub></td><td valign="top" align="center"><img src="img/ta-units/cormine4.png" width="48" alt="M-420" title="CORMINE4" /><br/><code>CORMINE4</code><br/><sub>M-420</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormine5.png" width="48" alt="M-515" title="CORMINE5" /><br/><code>CORMINE5</code><br/><sub>M-515</sub></td><td valign="top" align="center"><img src="img/ta-units/cormine6.png" width="48" alt="M-610" title="CORMINE6" /><br/><code>CORMINE6</code><br/><sub>M-610</sub></td></tr>
</table>


<sub><b>6</b> buildable units across <b>1</b> page.</sub>
</td>
</tr>
</table>



### Core — Advanced factories (tier 2)

#### `CORAAP` — Adv. Aircraft Plant

_Produces Aircraft_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/coraap.png" width="80" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><sub><code>CORAAP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center"><img src="img/ta-units/corape.png" width="48" alt="Rapier" title="CORAPE" /><br/><code>CORAPE</code><br/><sub>Rapier</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cortitan.png" width="48" alt="Titan" title="CORTITAN" /><br/><code>CORTITAN</code><br/><sub>Titan</sub></td><td valign="top" align="center"><img src="img/ta-units/corhurc.png" width="48" alt="Hurricane" title="CORHURC" /><br/><code>CORHURC</code><br/><sub>Hurricane</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corvamp.png" width="48" alt="Vamp" title="CORVAMP" /><br/><code>CORVAMP</code><br/><sub>Vamp</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corawac.png" width="48" alt="Vulture" title="CORAWAC" /><br/><code>CORAWAC</code> ⬇️<br/><sub>Vulture</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>6</b> buildable units across <b>2</b> pages; <b>1</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORALAB` — Adv. Kbot Lab

_Produces Kbots_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/coralab.png" width="80" alt="Adv. Kbot Lab" title="CORALAB" /><br/><sub><code>CORALAB</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center"><img src="img/ta-units/corpyro.png" width="48" alt="Pyro" title="CORPYRO" /><br/><code>CORPYRO</code><br/><sub>Pyro</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corcan.png" width="48" alt="The Can" title="CORCAN" /><br/><code>CORCAN</code><br/><sub>The Can</sub></td><td valign="top" align="center"><img src="img/ta-units/corroach.png" width="48" alt="Roach" title="CORROACH" /><br/><code>CORROACH</code><br/><sub>Roach</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corspec.png" width="48" alt="Spectre" title="CORSPEC" /><br/><code>CORSPEC</code><br/><sub>Spectre</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/corfast.png" width="48" alt="Freaker" title="CORFAST" /><br/><code>CORFAST</code> ⬇️<br/><sub>Freaker</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormort.png" width="48" alt="Morty" title="CORMORT" /><br/><code>CORMORT</code> ⬇️<br/><sub>Morty</sub></td><td valign="top" align="center"><img src="img/ta-units/corhrk.png" width="48" alt="Dominator" title="CORHRK" /><br/><code>CORHRK</code> ⬇️<br/><sub>Dominator</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corvoyr.png" width="48" alt="Voyeur" title="CORVOYR" /><br/><code>CORVOYR</code> ⬇️<br/><sub>Voyeur</sub></td><td valign="top" align="center"><img src="img/ta-units/corsumo.png" width="48" alt="Sumo" title="CORSUMO" /><br/><code>CORSUMO</code> ⬇️<br/><sub>Sumo</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/coramph.png" width="48" alt="Gimp" title="CORAMPH" /><br/><code>CORAMPH</code> ⬇️<br/><sub>Gimp</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 4</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corspy.png" width="48" alt="Parasite" title="CORSPY" /><br/><code>CORSPY</code> ⬇️<br/><sub>Parasite</sub></td><td valign="top" align="center"><img src="img/ta-units/cordecom.png" width="48" alt="Decoy Commander" title="CORDECOM" /><br/><code>CORDECOM</code> ⬇️<br/><sub>Decoy Commander</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cornecro.png" width="48" alt="Resurrection Kbot" title="CORNECRO" /><br/><code>CORNECRO</code> ⬇️<br/><sub>Resurrection Kbot</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>14</b> buildable units across <b>4</b> pages; <b>9</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORASY` — Adv. Shipyard

_Produces Ships_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corasy.png" width="80" alt="Adv. Shipyard" title="CORASY" /><br/><sub><code>CORASY</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center"><img src="img/ta-units/corcarry.png" width="48" alt="Hive" title="CORCARRY" /><br/><code>CORCARRY</code><br/><sub>Hive</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corshark.png" width="48" alt="Shark" title="CORSHARK" /><br/><code>CORSHARK</code><br/><sub>Shark</sub></td><td valign="top" align="center"><img src="img/ta-units/cormship.png" width="48" alt="Missile Frigate" title="CORMSHIP" /><br/><code>CORMSHIP</code><br/><sub>Missile Frigate</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corcrus.png" width="48" alt="Executioner" title="CORCRUS" /><br/><code>CORCRUS</code><br/><sub>Executioner</sub></td><td valign="top" align="center"><img src="img/ta-units/corbats.png" width="48" alt="Warlord" title="CORBATS" /><br/><code>CORBATS</code><br/><sub>Warlord</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corsjam.png" width="48" alt="Phantom" title="CORSJAM" /><br/><code>CORSJAM</code> ⬇️<br/><sub>Phantom</sub></td><td valign="top" align="center"><img src="img/ta-units/corarch.png" width="48" alt="Shredder" title="CORARCH" /><br/><code>CORARCH</code> ⬇️<br/><sub>Shredder</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/corssub.png" width="48" alt="Leviathan" title="CORSSUB" /><br/><code>CORSSUB</code> ⬇️<br/><sub>Leviathan</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>9</b> buildable units across <b>2</b> pages; <b>3</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>


#### `CORAVP` — Adv. Vehicle Plant

_Produces Vehicles_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/coravp.png" width="80" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><sub><code>CORAVP</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td valign="top" align="center"><img src="img/ta-units/corseal.png" width="48" alt="Crock" title="CORSEAL" /><br/><code>CORSEAL</code><br/><sub>Crock</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/correap.png" width="48" alt="Reaper" title="CORREAP" /><br/><code>CORREAP</code><br/><sub>Reaper</sub></td><td valign="top" align="center"><img src="img/ta-units/coreter.png" width="48" alt="Deleter" title="CORETER" /><br/><code>CORETER</code><br/><sub>Deleter</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormart.png" width="48" alt="Mobile Artillery" title="CORMART" /><br/><code>CORMART</code><br/><sub>Mobile Artillery</sub></td><td valign="top" align="center"><img src="img/ta-units/corgol.png" width="48" alt="Goliath" title="CORGOL" /><br/><code>CORGOL</code><br/><sub>Goliath</sub></td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 2</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corvrad.png" width="48" alt="Informer" title="CORVRAD" /><br/><code>CORVRAD</code><br/><sub>Informer</sub></td><td valign="top" align="center"><img src="img/ta-units/corvroc.png" width="48" alt="Diplomat" title="CORVROC" /><br/><code>CORVROC</code><br/><sub>Diplomat</sub></td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<table>
  <thead><tr><th colspan="2" align="left">Page 3</th></tr></thead>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center"><img src="img/ta-units/corsent.png" width="48" alt="Copperhead" title="CORSENT" /><br/><code>CORSENT</code> ⬇️<br/><sub>Copperhead</sub></td></tr>
  <tr><td valign="top" align="center"><img src="img/ta-units/cormabm.png" width="48" alt="Hedgehog" title="CORMABM" /><br/><code>CORMABM</code> ⬇️<br/><sub>Hedgehog</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>10</b> buildable units across <b>3</b> pages; <b>2</b> ⬇️ added by <code>download/*.tdf</code>.</sub>
</td>
</tr>
</table>



### Core — Krogoth gantry

#### `CORGANT` — Krogoth Gantry

_Builds Krogoth_

<table>
<tr>
<td valign="top" width="96"><img src="img/ta-units/corgant.png" width="80" alt="Krogoth Gantry" title="CORGANT" /><br/><sub><code>CORGANT</code></sub></td>
<td>

<table>
  <thead><tr><th colspan="2" align="left">Page 1</th></tr></thead>
  <tr><td valign="top" align="center"><img src="img/ta-units/corkrog.png" width="48" alt="Krogoth" title="CORKROG" /><br/><code>CORKROG</code><br/><sub>Krogoth</sub></td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
  <tr><td valign="top" align="center" style="color:#aaa">·</td><td valign="top" align="center" style="color:#aaa">·</td></tr>
</table>


<sub><b>1</b> buildable unit across <b>1</b> page.</sub>
</td>
</tr>
</table>


---


## Reverse index: who can build each unit

Sorted alphabetically. For each buildable unit, the constructors
that can produce it — each builder shown with its own portrait,
code, and display name. Useful when you're staring at a tech
requirement and trying to remember which factory you need to
queue first.


### Arm buildables — 130 units

<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armaap.png" width="80" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><b><code>ARMAAP</code></b><br/><sub>Adv. Aircraft Plant</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Produces Aircraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armaas.png" width="80" alt="Archer" title="ARMAAS" /><br/><b><code>ARMAAS</code></b><br/><sub>Archer</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Anti-Air Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armaca.png" width="80" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><b><code>ARMACA</code></b><br/><sub>Adv. Construction Aircraft</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 2</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaap.png" width="48" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><code>ARMAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armack.png" width="80" alt="Adv. Construction Kbot" title="ARMACK" /><br/><b><code>ARMACK</code></b><br/><sub>Adv. Construction Kbot</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 2</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armacsub.png" width="80" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><b><code>ARMACSUB</code></b><br/><sub>Advanced Construction Sub</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 2</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armacv.png" width="80" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><b><code>ARMACV</code></b><br/><sub>Adv. Construction Vehicle</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 2</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armah.png" width="80" alt="Swatter" title="ARMAH" /><br/><b><code>ARMAH</code></b><br/><sub>Swatter</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Anti-Air Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armalab.png" width="80" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><b><code>ARMALAB</code></b><br/><sub>Adv. Kbot Lab</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>2</b> constructors · <em>Produces Kbots</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armamb.png" width="80" alt="Ambusher" title="ARMAMB" /><br/><b><code>ARMAMB</code></b><br/><sub>Ambusher</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Pop-up Heavy Cannon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armamd.png" width="80" alt="Protector" title="ARMAMD" /><br/><b><code>ARMAMD</code></b><br/><sub>Protector</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Anti Missile Defense System</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armamph.png" width="80" alt="Pelican" title="ARMAMPH" /><br/><b><code>ARMAMPH</code></b><br/><sub>Pelican</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Amphibious Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armanac.png" width="80" alt="Anaconda" title="ARMANAC" /><br/><b><code>ARMANAC</code></b><br/><sub>Anaconda</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Hovertank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armanni.png" width="80" alt="Annihilator" title="ARMANNI" /><br/><b><code>ARMANNI</code></b><br/><sub>Annihilator</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Energy weapon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armap.png" width="80" alt="Aircraft Plant" title="ARMAP" /><br/><b><code>ARMAP</code></b><br/><sub>Aircraft Plant</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>7</b> constructors · <em>Produces Aircraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armarad.png" width="80" alt="Advanced Radar Tower" title="ARMARAD" /><br/><b><code>ARMARAD</code></b><br/><sub>Advanced Radar Tower</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Long Range Radar Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armaser.png" width="80" alt="Eraser" title="ARMASER" /><br/><b><code>ARMASER</code></b><br/><sub>Eraser</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Radar Jammer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armason.png" width="80" alt="Advanced Sonar Station" title="ARMASON" /><br/><b><code>ARMASON</code></b><br/><sub>Advanced Sonar Station</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Extended Sonar</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armacsub.png" width="48" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><code>ARMACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armasp.png" width="80" alt="Air Repair Pad" title="ARMASP" /><br/><b><code>ARMASP</code></b><br/><sub>Air Repair Pad</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Automatically repairs aircraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armasy.png" width="80" alt="Adv. Shipyard" title="ARMASY" /><br/><b><code>ARMASY</code></b><br/><sub>Adv. Shipyard</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Produces Ships</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armatl.png" width="80" alt="Advanced Torpedo Launcher" title="ARMATL" /><br/><b><code>ARMATL</code></b><br/><sub>Advanced Torpedo Launcher</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Advanced Torpedo Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armacsub.png" width="48" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><code>ARMACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armatlas.png" width="80" alt="Atlas" title="ARMATLAS" /><br/><b><code>ARMATLAS</code></b><br/><sub>Atlas</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Air Transport</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armavp.png" width="80" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><b><code>ARMAVP</code></b><br/><sub>Adv. Vehicle Plant</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>2</b> constructors · <em>Produces Vehicles</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armawac.png" width="80" alt="Eagle" title="ARMAWAC" /><br/><b><code>ARMAWAC</code></b><br/><sub>Eagle</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Radar Plane</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaap.png" width="48" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><code>ARMAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armbats.png" width="80" alt="Millenium" title="ARMBATS" /><br/><b><code>ARMBATS</code></b><br/><sub>Millenium</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Battleship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armbrawl.png" width="80" alt="Brawler" title="ARMBRAWL" /><br/><b><code>ARMBRAWL</code></b><br/><sub>Brawler</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Gunship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaap.png" width="48" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><code>ARMAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armbrtha.png" width="80" alt="Big Bertha" title="ARMBRTHA" /><br/><b><code>ARMBRTHA</code></b><br/><sub>Big Bertha</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Long Range Plasma Cannon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armbull.png" width="80" alt="Bulldog" title="ARMBULL" /><br/><b><code>ARMBULL</code></b><br/><sub>Bulldog</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Heavy Assault Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armca.png" width="80" alt="Construction Aircraft" title="ARMCA" /><br/><b><code>ARMCA</code></b><br/><sub>Construction Aircraft</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>2</b> constructors · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armplat.png" width="48" alt="Seaplane Platform" title="ARMPLAT" /><br/><code>ARMPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armcarry.png" width="80" alt="Colossus" title="ARMCARRY" /><br/><b><code>ARMCARRY</code></b><br/><sub>Colossus</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Light Carrier</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armch.png" width="80" alt="Construction Hovercraft" title="ARMCH" /><br/><b><code>ARMCH</code></b><br/><sub>Construction Hovercraft</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armck.png" width="80" alt="Construction KBot" title="ARMCK" /><br/><b><code>ARMCK</code></b><br/><sub>Construction KBot</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armckfus.png" width="80" alt="Cloakable Fusion Reactor" title="ARMCKFUS" /><br/><b><code>ARMCKFUS</code></b><br/><sub>Cloakable Fusion Reactor</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armcroc.png" width="80" alt="Triton" title="ARMCROC" /><br/><b><code>ARMCROC</code></b><br/><sub>Triton</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Amphibious Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armcrus.png" width="80" alt="Conqueror" title="ARMCRUS" /><br/><b><code>ARMCRUS</code></b><br/><sub>Conqueror</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Cruiser</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armcs.png" width="80" alt="Construction Ship" title="ARMCS" /><br/><b><code>ARMCS</code></b><br/><sub>Construction Ship</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armcv.png" width="80" alt="Construction Vehicle" title="ARMCV" /><br/><b><code>ARMCV</code></b><br/><sub>Construction Vehicle</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armdecom.png" width="80" alt="Decoy Commander" title="ARMDECOM" /><br/><b><code>ARMDECOM</code></b><br/><sub>Decoy Commander</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Decoy Commander</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armdrag.png" width="80" alt="Dragon&#39;s Teeth" title="ARMDRAG" /><br/><b><code>ARMDRAG</code></b><br/><sub>Dragon&#39;s Teeth</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>5</b> constructors · <em>Perimeter Defense</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armemp.png" width="80" alt="Stunner" title="ARMEMP" /><br/><b><code>ARMEMP</code></b><br/><sub>Stunner</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>EMP Missile Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armestor.png" width="80" alt="Energy Storage" title="ARMESTOR" /><br/><b><code>ARMESTOR</code></b><br/><sub>Energy Storage</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>6</b> constructors · <em>Increases Energy Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfark.png" width="80" alt="FARK" title="ARMFARK" /><br/><b><code>ARMFARK</code></b><br/><sub>FARK</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Fast Assist-Repair Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfast.png" width="80" alt="Zipper" title="ARMFAST" /><br/><b><code>ARMFAST</code></b><br/><sub>Zipper</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Fast Attack Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfav.png" width="80" alt="Jeffy" title="ARMFAV" /><br/><b><code>ARMFAV</code></b><br/><sub>Jeffy</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Fast Attack Vehicle</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfdrag.png" width="80" alt="Floating Dragon&#39;s Teeth" title="ARMFDRAG" /><br/><b><code>ARMFDRAG</code></b><br/><sub>Floating Dragon&#39;s Teeth</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Floating Dragon's Teeth</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfhlt.png" width="80" alt="Stingray" title="ARMFHLT" /><br/><b><code>ARMFHLT</code></b><br/><sub>Stingray</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Floating Heavy Laser Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfido.png" width="80" alt="Fido" title="ARMFIDO" /><br/><b><code>ARMFIDO</code></b><br/><sub>Fido</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Assault Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfig.png" width="80" alt="Freedom Fighter" title="ARMFIG" /><br/><b><code>ARMFIG</code></b><br/><sub>Freedom Fighter</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Fighter</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armflak.png" width="80" alt="Flakker" title="ARMFLAK" /><br/><b><code>ARMFLAK</code></b><br/><sub>Flakker</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Anti-Air Flak Gun</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armflash.png" width="80" alt="Flash" title="ARMFLASH" /><br/><b><code>ARMFLASH</code></b><br/><sub>Flash</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Fast Assault Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armflea.png" width="80" alt="Flea" title="ARMFLEA" /><br/><b><code>ARMFLEA</code></b><br/><sub>Flea</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Fast Light Scout Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfmkr.png" width="80" alt="Floating Metal Maker" title="ARMFMKR" /><br/><b><code>ARMFMKR</code></b><br/><sub>Floating Metal Maker</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>4</b> constructors · <em>Floating Metal Maker</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfort.png" width="80" alt="Fortification Wall" title="ARMFORT" /><br/><b><code>ARMFORT</code></b><br/><sub>Fortification Wall</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Perimeter Defense</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfrt.png" width="80" alt="Defender - NS" title="ARMFRT" /><br/><b><code>ARMFRT</code></b><br/><sub>Defender - NS</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Missile Tower - Naval Series</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armfus.png" width="80" alt="Fusion Reactor" title="ARMFUS" /><br/><b><code>ARMFUS</code></b><br/><sub>Fusion Reactor</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armgeo.png" width="80" alt="Geothermal Powerplant" title="ARMGEO" /><br/><b><code>ARMGEO</code></b><br/><sub>Geothermal Powerplant</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>5</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armguard.png" width="80" alt="Guardian" title="ARMGUARD" /><br/><b><code>ARMGUARD</code></b><br/><sub>Guardian</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>5</b> constructors · <em>Plasma Battery</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armham.png" width="80" alt="Hammer" title="ARMHAM" /><br/><b><code>ARMHAM</code></b><br/><sub>Hammer</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Artillery Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armhawk.png" width="80" alt="Hawk" title="ARMHAWK" /><br/><b><code>ARMHAWK</code></b><br/><sub>Hawk</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>2</b> constructors · <em>Stealth Fighter</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaap.png" width="48" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><code>ARMAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armplat.png" width="48" alt="Seaplane Platform" title="ARMPLAT" /><br/><code>ARMPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armhlt.png" width="80" alt="Sentinel" title="ARMHLT" /><br/><b><code>ARMHLT</code></b><br/><sub>Sentinel</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>5</b> constructors · <em>Heavy Laser Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armhp.png" width="80" alt="Hovercraft Platform" title="ARMHP" /><br/><b><code>ARMHP</code></b><br/><sub>Hovercraft Platform</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>5</b> constructors · <em>Builds Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armjam.png" width="80" alt="Jammer" title="ARMJAM" /><br/><b><code>ARMJAM</code></b><br/><sub>Jammer</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Radar Jammer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armjeth.png" width="80" alt="Jethro" title="ARMJETH" /><br/><b><code>ARMJETH</code></b><br/><sub>Jethro</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Anti-Air Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armlab.png" width="80" alt="Kbot Lab" title="ARMLAB" /><br/><b><code>ARMLAB</code></b><br/><sub>Kbot Lab</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>7</b> constructors · <em>Produces Kbots</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armlance.png" width="80" alt="Lancet" title="ARMLANCE" /><br/><b><code>ARMLANCE</code></b><br/><sub>Lancet</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>2</b> constructors · <em>Torpedo Bomber</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaap.png" width="48" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><code>ARMAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armplat.png" width="48" alt="Seaplane Platform" title="ARMPLAT" /><br/><code>ARMPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armlatnk.png" width="80" alt="Panther" title="ARMLATNK" /><br/><b><code>ARMLATNK</code></b><br/><sub>Panther</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Lightning Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armllt.png" width="80" alt="L.L.T." title="ARMLLT" /><br/><b><code>ARMLLT</code></b><br/><sub>L.L.T.</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>7</b> constructors · <em>Light Laser Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmakr.png" width="80" alt="Metal Maker" title="ARMMAKR" /><br/><b><code>ARMMAKR</code></b><br/><sub>Metal Maker</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>6</b> constructors · <em>Converts Energy into Metal</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmanni.png" width="80" alt="Penetrator" title="ARMMANNI" /><br/><b><code>ARMMANNI</code></b><br/><sub>Penetrator</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Energy Weapon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmark.png" width="80" alt="Marky" title="ARMMARK" /><br/><b><code>ARMMARK</code></b><br/><sub>Marky</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Radar Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmart.png" width="80" alt="Luger" title="ARMMART" /><br/><b><code>ARMMART</code></b><br/><sub>Luger</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Artillery</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmav.png" width="80" alt="Maverick" title="ARMMAV" /><br/><b><code>ARMMAV</code></b><br/><sub>Maverick</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Gun-slinging Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmerl.png" width="80" alt="Merl" title="ARMMERL" /><br/><b><code>ARMMERL</code></b><br/><sub>Merl</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Rocket Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmex.png" width="80" alt="Metal Extractor" title="ARMMEX" /><br/><b><code>ARMMEX</code></b><br/><sub>Metal Extractor</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>6</b> constructors · <em>Extracts Metal</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmh.png" width="80" alt="Wombat" title="ARMMH" /><br/><b><code>ARMMH</code></b><br/><sub>Wombat</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Hovercraft Rocket Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmine1.png" width="80" alt="Tiny" title="ARMMINE1" /><br/><b><code>ARMMINE1</code></b><br/><sub>Tiny</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Low Damage, Med. Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armmlv.png" width="48" alt="Podger" title="ARMMLV" /><br/><code>ARMMLV</code><br/><sub>Podger</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmine2.png" width="80" alt="Area Mine" title="ARMMINE2" /><br/><b><code>ARMMINE2</code></b><br/><sub>Area Mine</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Low Damage, Large Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armmlv.png" width="48" alt="Podger" title="ARMMLV" /><br/><code>ARMMLV</code><br/><sub>Podger</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmine3.png" width="80" alt="Focused Mine" title="ARMMINE3" /><br/><b><code>ARMMINE3</code></b><br/><sub>Focused Mine</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Med. Damage, Small Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armmlv.png" width="48" alt="Podger" title="ARMMLV" /><br/><code>ARMMLV</code><br/><sub>Podger</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmine4.png" width="80" alt="HE Area Mine" title="ARMMINE4" /><br/><b><code>ARMMINE4</code></b><br/><sub>HE Area Mine</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Med. Damage, Large Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armmlv.png" width="48" alt="Podger" title="ARMMLV" /><br/><code>ARMMLV</code><br/><sub>Podger</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmine5.png" width="80" alt="Precision Mine" title="ARMMINE5" /><br/><b><code>ARMMINE5</code></b><br/><sub>Precision Mine</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>High Damage, Small Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armmlv.png" width="48" alt="Podger" title="ARMMLV" /><br/><code>ARMMLV</code><br/><sub>Podger</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmine6.png" width="80" alt="Nuclear Mine" title="ARMMINE6" /><br/><b><code>ARMMINE6</code></b><br/><sub>Nuclear Mine</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Nuclear Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armmlv.png" width="48" alt="Podger" title="ARMMLV" /><br/><code>ARMMLV</code><br/><sub>Podger</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmlv.png" width="80" alt="Podger" title="ARMMLV" /><br/><b><code>ARMMLV</code></b><br/><sub>Podger</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mine Layer Vehicle</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmmkr.png" width="80" alt="Moho Metal Maker" title="ARMMMKR" /><br/><b><code>ARMMMKR</code></b><br/><sub>Moho Metal Maker</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Converts Energy into Metal</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmoho.png" width="80" alt="Moho Mine" title="ARMMOHO" /><br/><b><code>ARMMOHO</code></b><br/><sub>Moho Mine</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Advanced Metal Extractor</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmship.png" width="80" alt="Ranger" title="ARMMSHIP" /><br/><b><code>ARMMSHIP</code></b><br/><sub>Ranger</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Missile Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armmstor.png" width="80" alt="Metal Storage" title="ARMMSTOR" /><br/><b><code>ARMMSTOR</code></b><br/><sub>Metal Storage</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>6</b> constructors · <em>Increases Metal Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armpeep.png" width="80" alt="Peeper" title="ARMPEEP" /><br/><b><code>ARMPEEP</code></b><br/><sub>Peeper</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Air Scout</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armplat.png" width="80" alt="Seaplane Platform" title="ARMPLAT" /><br/><b><code>ARMPLAT</code></b><br/><sub>Seaplane Platform</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Builds Seaplanes</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armacsub.png" width="48" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><code>ARMACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armpnix.png" width="80" alt="Phoenix" title="ARMPNIX" /><br/><b><code>ARMPNIX</code></b><br/><sub>Phoenix</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Bomber</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaap.png" width="48" alt="Adv. Aircraft Plant" title="ARMAAP" /><br/><code>ARMAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armpt.png" width="80" alt="Skeeter" title="ARMPT" /><br/><b><code>ARMPT</code></b><br/><sub>Skeeter</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Scout Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armpw.png" width="80" alt="Peewee" title="ARMPW" /><br/><b><code>ARMPW</code></b><br/><sub>Peewee</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Infantry Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armrad.png" width="80" alt="Radar Tower" title="ARMRAD" /><br/><b><code>ARMRAD</code></b><br/><sub>Radar Tower</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>6</b> constructors · <em>Radar Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armrl.png" width="80" alt="Defender" title="ARMRL" /><br/><b><code>ARMRL</code></b><br/><sub>Defender</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>5</b> constructors · <em>Missile Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armrock.png" width="80" alt="Rocko" title="ARMROCK" /><br/><b><code>ARMROCK</code></b><br/><sub>Rocko</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Rocket Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armroy.png" width="80" alt="Crusader" title="ARMROY" /><br/><b><code>ARMROY</code></b><br/><sub>Crusader</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Destroyer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsam.png" width="80" alt="Samson" title="ARMSAM" /><br/><b><code>ARMSAM</code></b><br/><sub>Samson</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Missile Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armscab.png" width="80" alt="Scarab" title="ARMSCAB" /><br/><b><code>ARMSCAB</code></b><br/><sub>Scarab</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Missile Defense</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armscram.png" width="80" alt="Fibber" title="ARMSCRAM" /><br/><b><code>ARMSCRAM</code></b><br/><sub>Fibber</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Sonar Jamming Sub</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armseap.png" width="80" alt="Albatross" title="ARMSEAP" /><br/><b><code>ARMSEAP</code></b><br/><sub>Albatross</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Torpedo Seaplane</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armplat.png" width="48" alt="Seaplane Platform" title="ARMPLAT" /><br/><code>ARMPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armseer.png" width="80" alt="Seer" title="ARMSEER" /><br/><b><code>ARMSEER</code></b><br/><sub>Seer</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Radar</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsehak.png" width="80" alt="Seahawk" title="ARMSEHAK" /><br/><b><code>ARMSEHAK</code></b><br/><sub>Seahawk</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Airborne Sonar</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armplat.png" width="48" alt="Seaplane Platform" title="ARMPLAT" /><br/><code>ARMPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsfig.png" width="80" alt="Tornado" title="ARMSFIG" /><br/><b><code>ARMSFIG</code></b><br/><sub>Tornado</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Seaplane Fighter</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armplat.png" width="48" alt="Seaplane Platform" title="ARMPLAT" /><br/><code>ARMPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsh.png" width="80" alt="Skimmer" title="ARMSH" /><br/><b><code>ARMSH</code></b><br/><sub>Skimmer</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Scout Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsilo.png" width="80" alt="Retaliator" title="ARMSILO" /><br/><b><code>ARMSILO</code></b><br/><sub>Retaliator</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Nuclear Missile Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsjam.png" width="80" alt="Escort" title="ARMSJAM" /><br/><b><code>ARMSJAM</code></b><br/><sub>Escort</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Radar Jammer Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsnipe.png" width="80" alt="Shooter" title="ARMSNIPE" /><br/><b><code>ARMSNIPE</code></b><br/><sub>Shooter</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Sniper Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsolar.png" width="80" alt="Solar Collector" title="ARMSOLAR" /><br/><b><code>ARMSOLAR</code></b><br/><sub>Solar Collector</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>6</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsonar.png" width="80" alt="Sonar Station" title="ARMSONAR" /><br/><b><code>ARMSONAR</code></b><br/><sub>Sonar Station</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>4</b> constructors · <em>Locates Water Units</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armspid.png" width="80" alt="Spider" title="ARMSPID" /><br/><b><code>ARMSPID</code></b><br/><sub>Spider</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Spider Assault Vehicle</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armspy.png" width="80" alt="Infiltrator" title="ARMSPY" /><br/><b><code>ARMSPY</code></b><br/><sub>Infiltrator</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>SPY Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armstump.png" width="80" alt="Stumpy" title="ARMSTUMP" /><br/><b><code>ARMSTUMP</code></b><br/><sub>Stumpy</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Medium Assault Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armvp.png" width="48" alt="Vehicle Plant" title="ARMVP" /><br/><code>ARMVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsub.png" width="80" alt="Lurker" title="ARMSUB" /><br/><b><code>ARMSUB</code></b><br/><sub>Lurker</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Submarine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsubk.png" width="80" alt="Piranha" title="ARMSUBK" /><br/><b><code>ARMSUBK</code></b><br/><sub>Piranha</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Submarine Killer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armasy.png" width="48" alt="Adv. Shipyard" title="ARMASY" /><br/><code>ARMASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armsy.png" width="80" alt="Shipyard" title="ARMSY" /><br/><b><code>ARMSY</code></b><br/><sub>Shipyard</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>8</b> constructors · <em>Produces Ships</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armacsub.png" width="48" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><code>ARMACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armtarg.png" width="80" alt="Targeting Facility" title="ARMTARG" /><br/><b><code>ARMTARG</code></b><br/><sub>Targeting Facility</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Automatic Radar Targeting</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armthovr.png" width="80" alt="Bear" title="ARMTHOVR" /><br/><b><code>ARMTHOVR</code></b><br/><sub>Bear</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Transport Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armhp.png" width="48" alt="Hovercraft Platform" title="ARMHP" /><br/><code>ARMHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armthund.png" width="80" alt="Thunder" title="ARMTHUND" /><br/><b><code>ARMTHUND</code></b><br/><sub>Thunder</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Bomber</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armap.png" width="48" alt="Aircraft Plant" title="ARMAP" /><br/><code>ARMAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armtide.png" width="80" alt="Tidal Generator" title="ARMTIDE" /><br/><b><code>ARMTIDE</code></b><br/><sub>Tidal Generator</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>4</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armtl.png" width="80" alt="Torpedo Launcher" title="ARMTL" /><br/><b><code>ARMTL</code></b><br/><sub>Torpedo Launcher</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>4</b> constructors · <em>Torpedo Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armtship.png" width="80" alt="Hulk" title="ARMTSHIP" /><br/><b><code>ARMTSHIP</code></b><br/><sub>Hulk</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Transport Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armsy.png" width="48" alt="Shipyard" title="ARMSY" /><br/><code>ARMSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armuwes.png" width="80" alt="Underwater Energy Storage" title="ARMUWES" /><br/><b><code>ARMUWES</code></b><br/><sub>Underwater Energy Storage</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>4</b> constructors · <em>Increases Energy Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armuwfus.png" width="80" alt="Underwater Fusion Plant" title="ARMUWFUS" /><br/><b><code>ARMUWFUS</code></b><br/><sub>Underwater Fusion Plant</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armacsub.png" width="48" alt="Advanced Construction Sub" title="ARMACSUB" /><br/><code>ARMACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armuwmex.png" width="80" alt="Underwater Metal Extractor" title="ARMUWMEX" /><br/><b><code>ARMUWMEX</code></b><br/><sub>Underwater Metal Extractor</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>4</b> constructors · <em>Extracts Metal</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armuwms.png" width="80" alt="Underwater Metal Storage" title="ARMUWMS" /><br/><b><code>ARMUWMS</code></b><br/><sub>Underwater Metal Storage</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>4</b> constructors · <em>Increases Metal Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcs.png" width="48" alt="Construction Ship" title="ARMCS" /><br/><code>ARMCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armvader.png" width="80" alt="Invader" title="ARMVADER" /><br/><b><code>ARMVADER</code></b><br/><sub>Invader</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Crawling Bomb</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armvp.png" width="80" alt="Vehicle Plant" title="ARMVP" /><br/><b><code>ARMVP</code></b><br/><sub>Vehicle Plant</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>7</b> constructors · <em>Produces Vehicles</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armvulc.png" width="80" alt="Vulcan" title="ARMVULC" /><br/><b><code>ARMVULC</code></b><br/><sub>Vulcan</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>3</b> constructors · <em>Rapid Fire Plasma Cannon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armaca.png" width="48" alt="Adv. Construction Aircraft" title="ARMACA" /><br/><code>ARMACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armack.png" width="48" alt="Adv. Construction Kbot" title="ARMACK" /><br/><code>ARMACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armacv.png" width="48" alt="Adv. Construction Vehicle" title="ARMACV" /><br/><code>ARMACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armwar.png" width="80" alt="Warrior" title="ARMWAR" /><br/><b><code>ARMWAR</code></b><br/><sub>Warrior</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Medium Infantry Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armlab.png" width="48" alt="Kbot Lab" title="ARMLAB" /><br/><code>ARMLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armwin.png" width="80" alt="Wind Generator" title="ARMWIN" /><br/><b><code>ARMWIN</code></b><br/><sub>Wind Generator</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>6</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armca.png" width="48" alt="Construction Aircraft" title="ARMCA" /><br/><code>ARMCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armch.png" width="48" alt="Construction Hovercraft" title="ARMCH" /><br/><code>ARMCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armck.png" width="48" alt="Construction KBot" title="ARMCK" /><br/><code>ARMCK</code><br/><sub>Construction KBot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcom.png" width="48" alt="Commander" title="ARMCOM" /><br/><code>ARMCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcsa.png" width="48" alt="Construction Seaplane" title="ARMCSA" /><br/><code>ARMCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/armcv.png" width="48" alt="Construction Vehicle" title="ARMCV" /><br/><code>ARMCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armyork.png" width="80" alt="Phalanx" title="ARMYORK" /><br/><b><code>ARMYORK</code></b><br/><sub>Phalanx</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Mobile Flak Vehicle</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armavp.png" width="48" alt="Adv. Vehicle Plant" title="ARMAVP" /><br/><code>ARMAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/armzeus.png" width="80" alt="Zeus" title="ARMZEUS" /><br/><b><code>ARMZEUS</code></b><br/><sub>Zeus</sub>
</td>
<td valign="top">
<b>ARM</b> · built by <b>1</b> constructor · <em>Assault Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/armalab.png" width="48" alt="Adv. Kbot Lab" title="ARMALAB" /><br/><code>ARMALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>



### Core buildables — 131 units

<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coraap.png" width="80" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><b><code>CORAAP</code></b><br/><sub>Adv. Aircraft Plant</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Produces Aircraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coraca.png" width="80" alt="Adv. Construction Aircraft" title="CORACA" /><br/><b><code>CORACA</code></b><br/><sub>Adv. Construction Aircraft</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Tech Level 2</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraap.png" width="48" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><code>CORAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corack.png" width="80" alt="Adv. Construction Kbot" title="CORACK" /><br/><b><code>CORACK</code></b><br/><sub>Adv. Construction Kbot</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Tech Level 2</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coracv.png" width="80" alt="Adv. Construction Vehicle" title="CORACV" /><br/><b><code>CORACV</code></b><br/><sub>Adv. Construction Vehicle</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Tech Level 2</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corah.png" width="80" alt="Slinger" title="CORAH" /><br/><b><code>CORAH</code></b><br/><sub>Slinger</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Anti-Air Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corak.png" width="80" alt="A.K." title="CORAK" /><br/><b><code>CORAK</code></b><br/><sub>A.K.</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Infantry Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coralab.png" width="80" alt="Adv. Kbot Lab" title="CORALAB" /><br/><b><code>CORALAB</code></b><br/><sub>Adv. Kbot Lab</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>2</b> constructors · <em>Produces Kbots</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coramph.png" width="80" alt="Gimp" title="CORAMPH" /><br/><b><code>CORAMPH</code></b><br/><sub>Gimp</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Amphibious Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corap.png" width="80" alt="Aircraft Plant" title="CORAP" /><br/><b><code>CORAP</code></b><br/><sub>Aircraft Plant</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>7</b> constructors · <em>Produces Aircraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corape.png" width="80" alt="Rapier" title="CORAPE" /><br/><b><code>CORAPE</code></b><br/><sub>Rapier</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Gunship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraap.png" width="48" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><code>CORAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corarad.png" width="80" alt="Advanced Radar Tower" title="CORARAD" /><br/><b><code>CORARAD</code></b><br/><sub>Advanced Radar Tower</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Long Range Radar</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corarch.png" width="80" alt="Shredder" title="CORARCH" /><br/><b><code>CORARCH</code></b><br/><sub>Shredder</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Anti-Air Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corason.png" width="80" alt="Advanced Sonar Station" title="CORASON" /><br/><b><code>CORASON</code></b><br/><sub>Advanced Sonar Station</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Locates Water Units</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coracsub.png" width="48" alt="Advanced Construction Sub" title="CORACSUB" /><br/><code>CORACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corasp.png" width="80" alt="Air Repair Pad" title="CORASP" /><br/><b><code>CORASP</code></b><br/><sub>Air Repair Pad</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Automatically repairs aircraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corasy.png" width="80" alt="Adv. Shipyard" title="CORASY" /><br/><b><code>CORASY</code></b><br/><sub>Adv. Shipyard</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Produces Ships</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coratl.png" width="80" alt="Advanced Torpedo Launcher" title="CORATL" /><br/><b><code>CORATL</code></b><br/><sub>Advanced Torpedo Launcher</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Advanced Torpedo Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coracsub.png" width="48" alt="Advanced Construction Sub" title="CORACSUB" /><br/><code>CORACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coravp.png" width="80" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><b><code>CORAVP</code></b><br/><sub>Adv. Vehicle Plant</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>2</b> constructors · <em>Produces Vehicles</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corawac.png" width="80" alt="Vulture" title="CORAWAC" /><br/><b><code>CORAWAC</code></b><br/><sub>Vulture</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Radar Plane</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraap.png" width="48" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><code>CORAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corbats.png" width="80" alt="Warlord" title="CORBATS" /><br/><b><code>CORBATS</code></b><br/><sub>Warlord</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Battleship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corbuzz.png" width="80" alt="Buzzsaw" title="CORBUZZ" /><br/><b><code>CORBUZZ</code></b><br/><sub>Buzzsaw</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Rapid Fire Plasma Cannon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corca.png" width="80" alt="Construction Aircraft" title="CORCA" /><br/><b><code>CORCA</code></b><br/><sub>Construction Aircraft</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>2</b> constructors · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corplat.png" width="48" alt="Seaplane Platform" title="CORPLAT" /><br/><code>CORPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corcan.png" width="80" alt="The Can" title="CORCAN" /><br/><b><code>CORCAN</code></b><br/><sub>The Can</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Armored Assault Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corcarry.png" width="80" alt="Hive" title="CORCARRY" /><br/><b><code>CORCARRY</code></b><br/><sub>Hive</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Light Carrier</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corch.png" width="80" alt="Construction Hovercraft" title="CORCH" /><br/><b><code>CORCH</code></b><br/><sub>Construction Hovercraft</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corck.png" width="80" alt="Construction Kbot" title="CORCK" /><br/><b><code>CORCK</code></b><br/><sub>Construction Kbot</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corckfus.png" width="80" alt="Cloakable Fusion Reactor" title="CORCKFUS" /><br/><b><code>CORCKFUS</code></b><br/><sub>Cloakable Fusion Reactor</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corcrash.png" width="80" alt="Crasher" title="CORCRASH" /><br/><b><code>CORCRASH</code></b><br/><sub>Crasher</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Missile Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corcrus.png" width="80" alt="Executioner" title="CORCRUS" /><br/><b><code>CORCRUS</code></b><br/><sub>Executioner</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Cruiser</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corcs.png" width="80" alt="Construction Ship" title="CORCS" /><br/><b><code>CORCS</code></b><br/><sub>Construction Ship</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>2</b> constructors · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corcv.png" width="80" alt="Construction Vehicle" title="CORCV" /><br/><b><code>CORCV</code></b><br/><sub>Construction Vehicle</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Tech Level 1</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cordecom.png" width="80" alt="Decoy Commander" title="CORDECOM" /><br/><b><code>CORDECOM</code></b><br/><sub>Decoy Commander</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Decoy Commander</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cordoom.png" width="80" alt="Doomsday Machine" title="CORDOOM" /><br/><b><code>CORDOOM</code></b><br/><sub>Doomsday Machine</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Energy Weapon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cordrag.png" width="80" alt="Dragon&#39;s Teeth" title="CORDRAG" /><br/><b><code>CORDRAG</code></b><br/><sub>Dragon&#39;s Teeth</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>5</b> constructors · <em>Perimeter Defense</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corestor.png" width="80" alt="Energy Storage" title="CORESTOR" /><br/><b><code>CORESTOR</code></b><br/><sub>Energy Storage</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Increases Energy Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coreter.png" width="80" alt="Deleter" title="CORETER" /><br/><b><code>CORETER</code></b><br/><sub>Deleter</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Radar Jammer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfast.png" width="80" alt="Freaker" title="CORFAST" /><br/><b><code>CORFAST</code></b><br/><sub>Freaker</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Fast Attack Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfav.png" width="80" alt="Weasel" title="CORFAV" /><br/><b><code>CORFAV</code></b><br/><sub>Weasel</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Scout</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfdrag.png" width="80" alt="Floating Dragon&#39;s Teeth" title="CORFDRAG" /><br/><b><code>CORFDRAG</code></b><br/><sub>Floating Dragon&#39;s Teeth</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Floating Dragon's Teeth</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfhlt.png" width="80" alt="Thunderbolt" title="CORFHLT" /><br/><b><code>CORFHLT</code></b><br/><sub>Thunderbolt</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Floating Heavy Laser Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfink.png" width="80" alt="Fink" title="CORFINK" /><br/><b><code>CORFINK</code></b><br/><sub>Fink</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Air Scout</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corflak.png" width="80" alt="Cobra" title="CORFLAK" /><br/><b><code>CORFLAK</code></b><br/><sub>Cobra</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Anti-Air Flak Gun</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfmd.png" width="80" alt="Fortitude Missile Defense" title="CORFMD" /><br/><b><code>CORFMD</code></b><br/><sub>Fortitude Missile Defense</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Anti Missile Defense System</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfmkr.png" width="80" alt="Floating Metal Maker" title="CORFMKR" /><br/><b><code>CORFMKR</code></b><br/><sub>Floating Metal Maker</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Floating Metal Maker</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfort.png" width="80" alt="Fortification Wall" title="CORFORT" /><br/><b><code>CORFORT</code></b><br/><sub>Fortification Wall</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Perimeter Defense</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfrt.png" width="80" alt="Stinger" title="CORFRT" /><br/><b><code>CORFRT</code></b><br/><sub>Stinger</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Missile Tower - Naval Series</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corfus.png" width="80" alt="Fusion Power Plant" title="CORFUS" /><br/><b><code>CORFUS</code></b><br/><sub>Fusion Power Plant</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corgant.png" width="80" alt="Krogoth Gantry" title="CORGANT" /><br/><b><code>CORGANT</code></b><br/><sub>Krogoth Gantry</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Builds Krogoth</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corgator.png" width="80" alt="Instigator" title="CORGATOR" /><br/><b><code>CORGATOR</code></b><br/><sub>Instigator</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Assault Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corgeo.png" width="80" alt="Geothermal Powerplant" title="CORGEO" /><br/><b><code>CORGEO</code></b><br/><sub>Geothermal Powerplant</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>5</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corgol.png" width="80" alt="Goliath" title="CORGOL" /><br/><b><code>CORGOL</code></b><br/><sub>Goliath</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Very Heavy Assault Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corhlt.png" width="80" alt="Gaat Gun" title="CORHLT" /><br/><b><code>CORHLT</code></b><br/><sub>Gaat Gun</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>5</b> constructors · <em>Heavy Laser Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corhp.png" width="80" alt="Hovercraft Platform" title="CORHP" /><br/><b><code>CORHP</code></b><br/><sub>Hovercraft Platform</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>5</b> constructors · <em>Builds Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corhrk.png" width="80" alt="Dominator" title="CORHRK" /><br/><b><code>CORHRK</code></b><br/><sub>Dominator</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Heavy Rocket Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corhunt.png" width="80" alt="Hunter" title="CORHUNT" /><br/><b><code>CORHUNT</code></b><br/><sub>Hunter</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Airborne Sonar</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corplat.png" width="48" alt="Seaplane Platform" title="CORPLAT" /><br/><code>CORPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corhurc.png" width="80" alt="Hurricane" title="CORHURC" /><br/><b><code>CORHURC</code></b><br/><sub>Hurricane</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Strategic Bomber</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraap.png" width="48" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><code>CORAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corint.png" width="80" alt="Intimidator" title="CORINT" /><br/><b><code>CORINT</code></b><br/><sub>Intimidator</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Long Range Plasma Cannon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corkrog.png" width="80" alt="Krogoth" title="CORKROG" /><br/><b><code>CORKROG</code></b><br/><sub>Krogoth</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Experimental Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corgant.png" width="48" alt="Krogoth Gantry" title="CORGANT" /><br/><code>CORGANT</code><br/><sub>Krogoth Gantry</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corlab.png" width="80" alt="Kbot Lab" title="CORLAB" /><br/><b><code>CORLAB</code></b><br/><sub>Kbot Lab</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>7</b> constructors · <em>Produces Kbots</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corlevlr.png" width="80" alt="Leveler" title="CORLEVLR" /><br/><b><code>CORLEVLR</code></b><br/><sub>Leveler</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Riot Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corllt.png" width="80" alt="Light Laser Tower" title="CORLLT" /><br/><b><code>CORLLT</code></b><br/><sub>Light Laser Tower</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Light Laser Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormabm.png" width="80" alt="Hedgehog" title="CORMABM" /><br/><b><code>CORMABM</code></b><br/><sub>Hedgehog</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Missile Defense</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormakr.png" width="80" alt="Metal Maker" title="CORMAKR" /><br/><b><code>CORMAKR</code></b><br/><sub>Metal Maker</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Metal Maker</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormart.png" width="80" alt="Mobile Artillery" title="CORMART" /><br/><b><code>CORMART</code></b><br/><sub>Mobile Artillery</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Artillery</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormex.png" width="80" alt="Metal Extractor" title="CORMEX" /><br/><b><code>CORMEX</code></b><br/><sub>Metal Extractor</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Extracts Metal</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormh.png" width="80" alt="Nixer" title="CORMH" /><br/><b><code>CORMH</code></b><br/><sub>Nixer</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Hovercraft Rocket Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormine1.png" width="80" alt="M-104" title="CORMINE1" /><br/><b><code>CORMINE1</code></b><br/><sub>M-104</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Low Damage, Med. Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/cormlv.png" width="48" alt="Spoiler" title="CORMLV" /><br/><code>CORMLV</code><br/><sub>Spoiler</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormine2.png" width="80" alt="M-209" title="CORMINE2" /><br/><b><code>CORMINE2</code></b><br/><sub>M-209</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Low Damage, Large Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/cormlv.png" width="48" alt="Spoiler" title="CORMLV" /><br/><code>CORMLV</code><br/><sub>Spoiler</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormine3.png" width="80" alt="M-303" title="CORMINE3" /><br/><b><code>CORMINE3</code></b><br/><sub>M-303</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Med. Damage, Med. Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/cormlv.png" width="48" alt="Spoiler" title="CORMLV" /><br/><code>CORMLV</code><br/><sub>Spoiler</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormine4.png" width="80" alt="M-420" title="CORMINE4" /><br/><b><code>CORMINE4</code></b><br/><sub>M-420</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>High Damage, Med. Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/cormlv.png" width="48" alt="Spoiler" title="CORMLV" /><br/><code>CORMLV</code><br/><sub>Spoiler</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormine5.png" width="80" alt="M-515" title="CORMINE5" /><br/><b><code>CORMINE5</code></b><br/><sub>M-515</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>High Damage, Large Range Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/cormlv.png" width="48" alt="Spoiler" title="CORMLV" /><br/><code>CORMLV</code><br/><sub>Spoiler</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormine6.png" width="80" alt="M-610" title="CORMINE6" /><br/><b><code>CORMINE6</code></b><br/><sub>M-610</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Nuclear Mine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/cormlv.png" width="48" alt="Spoiler" title="CORMLV" /><br/><code>CORMLV</code><br/><sub>Spoiler</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormist.png" width="80" alt="Slasher" title="CORMIST" /><br/><b><code>CORMIST</code></b><br/><sub>Slasher</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Missile Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormlv.png" width="80" alt="Spoiler" title="CORMLV" /><br/><b><code>CORMLV</code></b><br/><sub>Spoiler</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mine Layer Vehicle</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormmkr.png" width="80" alt="Moho Metal Maker" title="CORMMKR" /><br/><b><code>CORMMKR</code></b><br/><sub>Moho Metal Maker</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Produces Metal</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormoho.png" width="80" alt="Moho Mine" title="CORMOHO" /><br/><b><code>CORMOHO</code></b><br/><sub>Moho Mine</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Advanced Metal Extractor</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormort.png" width="80" alt="Morty" title="CORMORT" /><br/><b><code>CORMORT</code></b><br/><sub>Morty</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Mortar Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormship.png" width="80" alt="Missile Frigate" title="CORMSHIP" /><br/><b><code>CORMSHIP</code></b><br/><sub>Missile Frigate</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Missile Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cormstor.png" width="80" alt="Metal Storage" title="CORMSTOR" /><br/><b><code>CORMSTOR</code></b><br/><sub>Metal Storage</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Increases Metal Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cornecro.png" width="80" alt="Resurrection Kbot" title="CORNECRO" /><br/><b><code>CORNECRO</code></b><br/><sub>Resurrection Kbot</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Resurrection Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corplas.png" width="80" alt="Immolator; //c" title="CORPLAS" /><br/><b><code>CORPLAS</code></b><br/><sub>Immolator; //c</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Plasma Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corplat.png" width="80" alt="Seaplane Platform" title="CORPLAT" /><br/><b><code>CORPLAT</code></b><br/><sub>Seaplane Platform</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Builds Seaplanes</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coracsub.png" width="48" alt="Advanced Construction Sub" title="CORACSUB" /><br/><code>CORACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corpt.png" width="80" alt="Searcher" title="CORPT" /><br/><b><code>CORPT</code></b><br/><sub>Searcher</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Scout Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corpun.png" width="80" alt="Punisher" title="CORPUN" /><br/><b><code>CORPUN</code></b><br/><sub>Punisher</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>5</b> constructors · <em>Plasma Battery</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corpyro.png" width="80" alt="Pyro" title="CORPYRO" /><br/><b><code>CORPYRO</code></b><br/><sub>Pyro</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Assault Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corrad.png" width="80" alt="Radar Tower" title="CORRAD" /><br/><b><code>CORRAD</code></b><br/><sub>Radar Tower</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Radar Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corraid.png" width="80" alt="Raider" title="CORRAID" /><br/><b><code>CORRAID</code></b><br/><sub>Raider</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Medium Assault Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corvp.png" width="48" alt="Vehicle Plant" title="CORVP" /><br/><code>CORVP</code><br/><sub>Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/correap.png" width="80" alt="Reaper" title="CORREAP" /><br/><b><code>CORREAP</code></b><br/><sub>Reaper</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Heavy Assault Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corrl.png" width="80" alt="Pulverizer" title="CORRL" /><br/><b><code>CORRL</code></b><br/><sub>Pulverizer</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>5</b> constructors · <em>Missile Tower</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corroach.png" width="80" alt="Roach" title="CORROACH" /><br/><b><code>CORROACH</code></b><br/><sub>Roach</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Crawling Bomb</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corroy.png" width="80" alt="Enforcer" title="CORROY" /><br/><b><code>CORROY</code></b><br/><sub>Enforcer</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Destroyer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corseal.png" width="80" alt="Crock" title="CORSEAL" /><br/><b><code>CORSEAL</code></b><br/><sub>Crock</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Amphibious Tank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corseap.png" width="80" alt="Typhoon" title="CORSEAP" /><br/><b><code>CORSEAP</code></b><br/><sub>Typhoon</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Torpedo Seaplane</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corplat.png" width="48" alt="Seaplane Platform" title="CORPLAT" /><br/><code>CORPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsent.png" width="80" alt="Copperhead" title="CORSENT" /><br/><b><code>CORSENT</code></b><br/><sub>Copperhead</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Flak Vehicle</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsfig.png" width="80" alt="Voodoo" title="CORSFIG" /><br/><b><code>CORSFIG</code></b><br/><sub>Voodoo</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Seaplane Fighter</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corplat.png" width="48" alt="Seaplane Platform" title="CORPLAT" /><br/><code>CORPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsh.png" width="80" alt="Scrubber" title="CORSH" /><br/><b><code>CORSH</code></b><br/><sub>Scrubber</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Scout Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corshad.png" width="80" alt="Shadow" title="CORSHAD" /><br/><b><code>CORSHAD</code></b><br/><sub>Shadow</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Bomber</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corshark.png" width="80" alt="Shark" title="CORSHARK" /><br/><b><code>CORSHARK</code></b><br/><sub>Shark</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Submarine Killer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsilo.png" width="80" alt="Silencer" title="CORSILO" /><br/><b><code>CORSILO</code></b><br/><sub>Silencer</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Nuclear Missile Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsjam.png" width="80" alt="Phantom" title="CORSJAM" /><br/><b><code>CORSJAM</code></b><br/><sub>Phantom</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Radar Jammer Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsnap.png" width="80" alt="Snapper" title="CORSNAP" /><br/><b><code>CORSNAP</code></b><br/><sub>Snapper</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Hovertank</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsolar.png" width="80" alt="Solar Collector" title="CORSOLAR" /><br/><b><code>CORSOLAR</code></b><br/><sub>Solar Collector</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsonar.png" width="80" alt="Sonar Station" title="CORSONAR" /><br/><b><code>CORSONAR</code></b><br/><sub>Sonar Station</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Sonar Station</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corspec.png" width="80" alt="Spectre" title="CORSPEC" /><br/><b><code>CORSPEC</code></b><br/><sub>Spectre</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Radar Jammer</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corspy.png" width="80" alt="Parasite" title="CORSPY" /><br/><b><code>CORSPY</code></b><br/><sub>Parasite</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>SPY Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corssub.png" width="80" alt="Leviathan" title="CORSSUB" /><br/><b><code>CORSSUB</code></b><br/><sub>Leviathan</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Battle Sub</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corasy.png" width="48" alt="Adv. Shipyard" title="CORASY" /><br/><code>CORASY</code><br/><sub>Adv. Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corstorm.png" width="80" alt="Storm" title="CORSTORM" /><br/><b><code>CORSTORM</code></b><br/><sub>Storm</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Rocket Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsub.png" width="80" alt="Snake" title="CORSUB" /><br/><b><code>CORSUB</code></b><br/><sub>Snake</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Submarine</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsumo.png" width="80" alt="Sumo" title="CORSUMO" /><br/><b><code>CORSUMO</code></b><br/><sub>Sumo</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Adv. Armored Assault Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corsy.png" width="80" alt="Shipyard" title="CORSY" /><br/><b><code>CORSY</code></b><br/><sub>Shipyard</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>7</b> constructors · <em>Produces Ships</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coracsub.png" width="48" alt="Advanced Construction Sub" title="CORACSUB" /><br/><code>CORACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cortarg.png" width="80" alt="Targeting Facility" title="CORTARG" /><br/><b><code>CORTARG</code></b><br/><sub>Targeting Facility</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Automatic Radar Targeting</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corthovr.png" width="80" alt="Turtle" title="CORTHOVR" /><br/><b><code>CORTHOVR</code></b><br/><sub>Turtle</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Transport Hovercraft</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corhp.png" width="48" alt="Hovercraft Platform" title="CORHP" /><br/><code>CORHP</code><br/><sub>Hovercraft Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corthud.png" width="80" alt="Thud" title="CORTHUD" /><br/><b><code>CORTHUD</code></b><br/><sub>Thud</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Artillery Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corlab.png" width="48" alt="Kbot Lab" title="CORLAB" /><br/><code>CORLAB</code><br/><sub>Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cortide.png" width="80" alt="Tidal Generator" title="CORTIDE" /><br/><b><code>CORTIDE</code></b><br/><sub>Tidal Generator</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cortitan.png" width="80" alt="Titan" title="CORTITAN" /><br/><b><code>CORTITAN</code></b><br/><sub>Titan</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>2</b> constructors · <em>Torpedo Bomber</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraap.png" width="48" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><code>CORAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corplat.png" width="48" alt="Seaplane Platform" title="CORPLAT" /><br/><code>CORPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cortl.png" width="80" alt="Torpedo Launcher" title="CORTL" /><br/><b><code>CORTL</code></b><br/><sub>Torpedo Launcher</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Torpedo Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cortoast.png" width="80" alt="Toaster" title="CORTOAST" /><br/><b><code>CORTOAST</code></b><br/><sub>Toaster</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Pop-up Heavy Cannon</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cortron.png" width="80" alt="Neutron" title="CORTRON" /><br/><b><code>CORTRON</code></b><br/><sub>Neutron</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>3</b> constructors · <em>Neutron Missile Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraca.png" width="48" alt="Adv. Construction Aircraft" title="CORACA" /><br/><code>CORACA</code><br/><sub>Adv. Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corack.png" width="48" alt="Adv. Construction Kbot" title="CORACK" /><br/><code>CORACK</code><br/><sub>Adv. Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/cortship.png" width="80" alt="Envoy" title="CORTSHIP" /><br/><b><code>CORTSHIP</code></b><br/><sub>Envoy</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Transport Ship</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corsy.png" width="48" alt="Shipyard" title="CORSY" /><br/><code>CORSY</code><br/><sub>Shipyard</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coruwes.png" width="80" alt="Underwater Energy Storage" title="CORUWES" /><br/><b><code>CORUWES</code></b><br/><sub>Underwater Energy Storage</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Increases Energy Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coruwfus.png" width="80" alt="Underwater Fusion Plant" title="CORUWFUS" /><br/><b><code>CORUWFUS</code></b><br/><sub>Underwater Fusion Plant</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coracsub.png" width="48" alt="Advanced Construction Sub" title="CORACSUB" /><br/><code>CORACSUB</code><br/><sub>Advanced Construction Sub</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coruwmex.png" width="80" alt="Underwater Metal Extractor" title="CORUWMEX" /><br/><b><code>CORUWMEX</code></b><br/><sub>Underwater Metal Extractor</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Extracts Metal</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/coruwms.png" width="80" alt="Underwater Metal Storage" title="CORUWMS" /><br/><b><code>CORUWMS</code></b><br/><sub>Underwater Metal Storage</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>4</b> constructors · <em>Increases Metal Storage</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcs.png" width="48" alt="Construction Ship" title="CORCS" /><br/><code>CORCS</code><br/><sub>Construction Ship</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corvalk.png" width="80" alt="Valkyrie" title="CORVALK" /><br/><b><code>CORVALK</code></b><br/><sub>Valkyrie</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Air Transport</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corvamp.png" width="80" alt="Vamp" title="CORVAMP" /><br/><b><code>CORVAMP</code></b><br/><sub>Vamp</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>2</b> constructors · <em>Stealth Fighter</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coraap.png" width="48" alt="Adv. Aircraft Plant" title="CORAAP" /><br/><code>CORAAP</code><br/><sub>Adv. Aircraft Plant</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corplat.png" width="48" alt="Seaplane Platform" title="CORPLAT" /><br/><code>CORPLAT</code><br/><sub>Seaplane Platform</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corveng.png" width="80" alt="Avenger" title="CORVENG" /><br/><b><code>CORVENG</code></b><br/><sub>Avenger</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Fighter</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corap.png" width="48" alt="Aircraft Plant" title="CORAP" /><br/><code>CORAP</code><br/><sub>Aircraft Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corvipe.png" width="80" alt="Viper" title="CORVIPE" /><br/><b><code>CORVIPE</code></b><br/><sub>Viper</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>5</b> constructors · <em>Pop-Up Heavy Laser</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corvoyr.png" width="80" alt="Voyeur" title="CORVOYR" /><br/><b><code>CORVOYR</code></b><br/><sub>Voyeur</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Radar Kbot</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coralab.png" width="48" alt="Adv. Kbot Lab" title="CORALAB" /><br/><code>CORALAB</code><br/><sub>Adv. Kbot Lab</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corvp.png" width="80" alt="Vehicle Plant" title="CORVP" /><br/><b><code>CORVP</code></b><br/><sub>Vehicle Plant</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>7</b> constructors · <em>Produces Vehicles</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coracv.png" width="48" alt="Adv. Construction Vehicle" title="CORACV" /><br/><code>CORACV</code><br/><sub>Adv. Construction Vehicle</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td></tr>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corvrad.png" width="80" alt="Informer" title="CORVRAD" /><br/><b><code>CORVRAD</code></b><br/><sub>Informer</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Radar</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corvroc.png" width="80" alt="Diplomat" title="CORVROC" /><br/><b><code>CORVROC</code></b><br/><sub>Diplomat</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>1</b> constructor · <em>Mobile Rocket Launcher</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/coravp.png" width="48" alt="Adv. Vehicle Plant" title="CORAVP" /><br/><code>CORAVP</code><br/><sub>Adv. Vehicle Plant</sub></td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
</table>
</td></tr>
</table>


<table>
<tr><td valign="top" width="120" rowspan="2" align="center">
<img src="img/ta-units/corwin.png" width="80" alt="Wind Generator" title="CORWIN" /><br/><b><code>CORWIN</code></b><br/><sub>Wind Generator</sub>
</td>
<td valign="top">
<b>CORE</b> · built by <b>6</b> constructors · <em>Produces Energy</em>
</td></tr>
<tr><td valign="top">
<table>
<tr><td valign="top" align="center" width="56"><img src="img/ta-units/corca.png" width="48" alt="Construction Aircraft" title="CORCA" /><br/><code>CORCA</code><br/><sub>Construction Aircraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corch.png" width="48" alt="Construction Hovercraft" title="CORCH" /><br/><code>CORCH</code><br/><sub>Construction Hovercraft</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corck.png" width="48" alt="Construction Kbot" title="CORCK" /><br/><code>CORCK</code><br/><sub>Construction Kbot</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcom.png" width="48" alt="Commander" title="CORCOM" /><br/><code>CORCOM</code><br/><sub>Commander</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcsa.png" width="48" alt="Construction Seaplane" title="CORCSA" /><br/><code>CORCSA</code><br/><sub>Construction Seaplane</sub></td><td valign="top" align="center" width="56"><img src="img/ta-units/corcv.png" width="48" alt="Construction Vehicle" title="CORCV" /><br/><code>CORCV</code><br/><sub>Construction Vehicle</sub></td></tr>
</table>
</td></tr>
</table>




### Units not registered with any builder

17 units defined in `units/*.fbi` but not
reachable through any constructor's build menu — these are
mission-only spawns, decoy variants, features, mines deployed
by mine-layers, or wreckage. Their full stats remain in
[ta-units.md](ta-units.md).

`ARMBEAC`, `ARMCOM`, `ARMCSA`, `ARMDEV1`, `ARMGATE`, `ARMSCORP`, `ARMSS`, `CORACSUB`, `CORBEAC`, `CORBUILD`, `CORCOM`, `CORCSA`, `CORDEV1`, `CORGATE`, `CORSCORP`, `CORSS`, `CORTRUCK`.

