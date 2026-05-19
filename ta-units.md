# Reference — TA Unit IDs

Every unit definition shipped in Total Annihilation v3.1c (base game +
Core Contingency + Battle Tactics + the rev 3.1 patch), extracted
directly from the flattened install's `units/*.fbi`. Counts as of
the GoG release: **278 units total** (137 ARM + 141 CORE).

Each row's portrait is the unit's `unitpics/<Objectname>.pcx`,
converted to PNG and stored under [`img/ta-units/`](img/ta-units/).
`Code` is the unit's `UnitName=` (the lookup key everything else
uses to refer to the unit). See the
[FBI field dictionary](https://github.com/coreprime/kbot/blob/main/docs/formats/tdf.md#appendix-a--fbi-field-dictionary)
in the kbot docs for what each FBI field controls. `Weapons`
columns are the literal `Weapon1/2/3=` values — cross-reference
with [TA weapons](ta-weapons.md).

> [!TIP]
> **To regenerate this page**, run `kbot document` (or `task document`)
> from a kbot checkout. Source is the flattened TA install at the path
> your kbot context points at.

## Contents

- [Arm](#arm)
  - [Commander](#arm---commander)
  - [Construction units](#arm---construction-units)
  - [Production buildings (plants, labs, shipyards)](#arm---production-buildings-plants-labs-shipyards)
  - [Resource & storage buildings](#arm---resource--storage-buildings)
  - [Defensive structures (turrets, anti-nuke, big-bertha)](#arm---defensive-structures-turrets-anti-nuke-big-bertha)
  - [Sensors & jammers (radar, sonar)](#arm---sensors--jammers-radar-sonar)
  - [Aircraft (VTOL, bombers, fighters)](#arm---aircraft-vtol-bombers-fighters)
  - [Ships (surface)](#arm---ships-surface)
  - [Submarines & underwater units](#arm---submarines--underwater-units)
  - [Kbots (bipedal walkers)](#arm---kbots-bipedal-walkers)
  - [Vehicles (tanks, hovercraft, jeeps)](#arm---vehicles-tanks-hovercraft-jeeps)
  - [Misc / other](#arm---misc--other)
- [Core](#core)
  - [Commander](#core---commander)
  - [Construction units](#core---construction-units)
  - [Production buildings (plants, labs, shipyards)](#core---production-buildings-plants-labs-shipyards)
  - [Resource & storage buildings](#core---resource--storage-buildings)
  - [Defensive structures (turrets, anti-nuke, big-bertha)](#core---defensive-structures-turrets-anti-nuke-big-bertha)
  - [Sensors & jammers (radar, sonar)](#core---sensors--jammers-radar-sonar)
  - [Aircraft (VTOL, bombers, fighters)](#core---aircraft-vtol-bombers-fighters)
  - [Ships (surface)](#core---ships-surface)
  - [Kbots (bipedal walkers)](#core---kbots-bipedal-walkers)
  - [Vehicles (tanks, hovercraft, jeeps)](#core---vehicles-tanks-hovercraft-jeeps)
  - [Misc / other](#core---misc--other)

---

## ARM

**Arm** — 137 units across 12 categories.


### ARM — Commander

2 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armcom.png" width="64" alt="Commander" title="ARMCOM" /> | `ARMCOM` | Commander | Commander | COMMANDER | 29854 / 34125 | 3000 | ARMCOMLASER, ARM_DISINTEGRATOR |
| <img src="img/ta-units/armdecom.png" width="64" alt="Decoy Commander" title="ARMDECOM" /> | `ARMDECOM` | Decoy Commander | Decoy Commander | COMMANDER | 721 / 11561 | 1420 | ARMCOMLASER |


### ARM — Construction units

12 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armaca.png" width="64" alt="Adv. Construction Aircraft" title="ARMACA" /> | `ARMACA` | Adv. Construction Aircraft | Tech Level 2 | CNSTR | 220 / 12096 | 360 | — |
| <img src="img/ta-units/armack.png" width="64" alt="Adv. Construction Kbot" title="ARMACK" /> | `ARMACK` | Adv. Construction Kbot | Tech Level 2 | CNSTR | 300 / 5784 | 1040 | — |
| <img src="img/ta-units/armacsub.png" width="64" alt="Advanced Construction Sub" title="ARMACSUB" /> | `ARMACSUB` | Advanced Construction Sub | Tech Level 2 | SHIP | 695 / 7568 | 360 | — |
| <img src="img/ta-units/armacv.png" width="64" alt="Adv. Construction Vehicle" title="ARMACV" /> | `ARMACV` | Adv. Construction Vehicle | Tech Level 2 | CNSTR | 481 / 4263 | 1205 | — |
| <img src="img/ta-units/armca.png" width="64" alt="Construction Aircraft" title="ARMCA" /> | `ARMCA` | Construction Aircraft | Tech Level 1 | VTOL | 105 / 4320 | 280 | — |
| <img src="img/ta-units/armch.png" width="64" alt="Construction Hovercraft" title="ARMCH" /> | `ARMCH` | Construction Hovercraft | Tech Level 1 | CNSTR | 396 / 4370 | 723 | — |
| <img src="img/ta-units/armck.png" width="64" alt="Construction KBot" title="ARMCK" /> | `ARMCK` | Construction KBot | Tech Level 1 | KBOT | 120 / 2410 | 700 | — |
| <img src="img/ta-units/armcs.png" width="64" alt="Construction Ship" title="ARMCS" /> | `ARMCS` | Construction Ship | Tech Level 1 | SHIP | 255 / 2130 | 1105 | — |
| <img src="img/ta-units/armcsa.png" width="64" alt="Construction Seaplane" title="ARMCSA" /> | `ARMCSA` | Construction Seaplane | Tech Level 1 | VTOL | 115 / 5368 | 170 | — |
| <img src="img/ta-units/armcv.png" width="64" alt="Construction Vehicle" title="ARMCV" /> | `ARMCV` | Construction Vehicle | Tech Level 1 | CNSTR | 185 / 2030 | 870 | — |
| <img src="img/ta-units/armfark.png" width="64" alt="FARK" title="ARMFARK" /> | `ARMFARK` | FARK | Fast Assist-Repair Kbot | KBOT | 480 / 3219 | 830 | — |
| <img src="img/ta-units/armmlv.png" width="64" alt="Podger" title="ARMMLV" /> | `ARMMLV` | Podger | Mine Layer Vehicle | CNSTR | 173 / 1031 | 1200 | — |


### ARM — Production buildings (plants, labs, shipyards)

10 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armaap.png" width="64" alt="Adv. Aircraft Plant" title="ARMAAP" /> | `ARMAAP` | Adv. Aircraft Plant | Produces Aircraft | PLANT | 2210 / 4521 | 2100 | — |
| <img src="img/ta-units/armalab.png" width="64" alt="Adv. Kbot Lab" title="ARMALAB" /> | `ARMALAB` | Adv. Kbot Lab | Produces Kbots | PLANT | 2007 / 3277 | 3005 | — |
| <img src="img/ta-units/armap.png" width="64" alt="Aircraft Plant" title="ARMAP" /> | `ARMAP` | Aircraft Plant | Produces Aircraft | PLANT | 850 / 1370 | 1850 | — |
| <img src="img/ta-units/armasy.png" width="64" alt="Adv. Shipyard" title="ARMASY" /> | `ARMASY` | Adv. Shipyard | Produces Ships | PLANT | 2524 / 2402 | 2820 | — |
| <img src="img/ta-units/armavp.png" width="64" alt="Adv. Vehicle Plant" title="ARMAVP" /> | `ARMAVP` | Adv. Vehicle Plant | Produces Vehicles | PLANT | 1984 / 3200 | 2435 | — |
| <img src="img/ta-units/armhp.png" width="64" alt="Hovercraft Platform" title="ARMHP" /> | `ARMHP` | Hovercraft Platform | Builds Hovercraft | PLANT | 2007 / 5277 | 3005 | — |
| <img src="img/ta-units/armlab.png" width="64" alt="Kbot Lab" title="ARMLAB" /> | `ARMLAB` | Kbot Lab | Produces Kbots | PLANT | 705 / 1130 | 2690 | — |
| <img src="img/ta-units/armplat.png" width="64" alt="Seaplane Platform" title="ARMPLAT" /> | `ARMPLAT` | Seaplane Platform | Builds Seaplanes | PLANT | 2223 / 5396 | 1820 | — |
| <img src="img/ta-units/armsy.png" width="64" alt="Shipyard" title="ARMSY" /> | `ARMSY` | Shipyard | Produces Ships | PLANT | 615 / 775 | 2490 | — |
| <img src="img/ta-units/armvp.png" width="64" alt="Vehicle Plant" title="ARMVP" /> | `ARMVP` | Vehicle Plant | Produces Vehicles | PLANT | 620 / 1000 | 2580 | — |


### ARM — Resource & storage buildings

19 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armckfus.png" width="64" alt="Cloakable Fusion Reactor" title="ARMCKFUS" /> | `ARMCKFUS` | Cloakable Fusion Reactor | Produces Energy | ENERGY | 5420 / 42058 | 2200 | — |
| <img src="img/ta-units/armdrag.png" width="64" alt="Dragon&#39;s Teeth" title="ARMDRAG" /> | `ARMDRAG` | Dragon's Teeth | Perimeter Defense | FORT | 10 / 250 | 3500 | — |
| <img src="img/ta-units/armestor.png" width="64" alt="Energy Storage" title="ARMESTOR" /> | `ARMESTOR` | Energy Storage | Increases Energy Storage | ENERGY | 240 / 2430 | 1000 | — |
| <img src="img/ta-units/armfmkr.png" width="64" alt="Floating Metal Maker" title="ARMFMKR" /> | `ARMFMKR` | Floating Metal Maker | Floating Metal Maker | METAL | — / 1480 | 110 | — |
| <img src="img/ta-units/armfort.png" width="64" alt="Fortification Wall" title="ARMFORT" /> | `ARMFORT` | Fortification Wall | Perimeter Defense | FORT | 27 / 675 | 2000 | — |
| <img src="img/ta-units/armfus.png" width="64" alt="Fusion Reactor" title="ARMFUS" /> | `ARMFUS` | Fusion Reactor | Produces Energy | ENERGY | 5130 / 36058 | 3100 | — |
| <img src="img/ta-units/armgeo.png" width="64" alt="Geothermal Powerplant" title="ARMGEO" /> | `ARMGEO` | Geothermal Powerplant | Produces Energy | ENERGY | 520 / 9568 | 880 | — |
| <img src="img/ta-units/armmakr.png" width="64" alt="Metal Maker" title="ARMMAKR" /> | `ARMMAKR` | Metal Maker | Converts Energy into Metal | METAL | 0 / 687 | 144 | — |
| <img src="img/ta-units/armmex.png" width="64" alt="Metal Extractor" title="ARMMEX" /> | `ARMMEX` | Metal Extractor | Extracts Metal | METAL | 50 / 521 | 170 | — |
| <img src="img/ta-units/armmmkr.png" width="64" alt="Moho Metal Maker" title="ARMMMKR" /> | `ARMMMKR` | Moho Metal Maker | Converts Energy into Metal | METAL | 58 / 9350 | 400 | — |
| <img src="img/ta-units/armmoho.png" width="64" alt="Moho Mine" title="ARMMOHO" /> | `ARMMOHO` | Moho Mine | Advanced Metal Extractor | METAL | 1508 / 8700 | 1573 | — |
| <img src="img/ta-units/armmstor.png" width="64" alt="Metal Storage" title="ARMMSTOR" /> | `ARMMSTOR` | Metal Storage | Increases Metal Storage | METAL | 305 / 535 | 1329 | — |
| <img src="img/ta-units/armsolar.png" width="64" alt="Solar Collector" title="ARMSOLAR" /> | `ARMSOLAR` | Solar Collector | Produces Energy | ENERGY | 145 / 760 | 326 | — |
| <img src="img/ta-units/armtide.png" width="64" alt="Tidal Generator" title="ARMTIDE" /> | `ARMTIDE` | Tidal Generator | Produces Energy | WATER | 82 / 768 | 256 | — |
| <img src="img/ta-units/armuwes.png" width="64" alt="Underwater Energy Storage" title="ARMUWES" /> | `ARMUWES` | Underwater Energy Storage | Increases Energy Storage | ENERGY | 284 / 2950 | 1447 | — |
| <img src="img/ta-units/armuwfus.png" width="64" alt="Underwater Fusion Plant" title="ARMUWFUS" /> | `ARMUWFUS` | Underwater Fusion Plant | Produces Energy | ENERGY | 7085 / 54287 | 1231 | — |
| <img src="img/ta-units/armuwmex.png" width="64" alt="Underwater Metal Extractor" title="ARMUWMEX" /> | `ARMUWMEX` | Underwater Metal Extractor | Extracts Metal | METAL | 130 / 2074 | 330 | — |
| <img src="img/ta-units/armuwms.png" width="64" alt="Underwater Metal Storage" title="ARMUWMS" /> | `ARMUWMS` | Underwater Metal Storage | Increases Metal Storage | METAL | 360 / 1255 | 1625 | — |
| <img src="img/ta-units/armwin.png" width="64" alt="Wind Generator" title="ARMWIN" /> | `ARMWIN` | Wind Generator | Produces Energy | ENERGY | 52 / 509 | 176 | — |


### ARM — Defensive structures (turrets, anti-nuke, big-bertha)

18 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armamb.png" width="64" alt="Ambusher" title="ARMAMB" /> | `ARMAMB` | Ambusher | Pop-up Heavy Cannon | FORT | 2002 / 16821 | 1658 | ARMAMB_GUN |
| <img src="img/ta-units/armamd.png" width="64" alt="Protector" title="ARMAMD" /> | `ARMAMD` | Protector | Anti Missile Defense System | FORT | 1437 / 88000 | 780 | AMD_ROCKET |
| <img src="img/ta-units/armanni.png" width="64" alt="Annihilator" title="ARMANNI" /> | `ARMANNI` | Annihilator | Energy weapon | FORT | 3985 / 25025 | 1410 | ARM_TOTAL_ANNIHILATOR |
| <img src="img/ta-units/armatl.png" width="64" alt="Advanced Torpedo Launcher" title="ARMATL" /> | `ARMATL` | Advanced Torpedo Launcher | Advanced Torpedo Launcher | WATER | 1762 / 4942 | 520 | ARMATL_TORPEDO |
| <img src="img/ta-units/armbrtha.png" width="64" alt="Big Bertha" title="ARMBRTHA" /> | `ARMBRTHA` | Big Bertha | Long Range Plasma Cannon | FORT | 4184 / 64680 | 1800 | ARM_BERTHACANNON |
| <img src="img/ta-units/armfdrag.png" width="64" alt="Floating Dragon&#39;s Teeth" title="ARMFDRAG" /> | `ARMFDRAG` | Floating Dragon's Teeth | Floating Dragon's Teeth | FORT | 20 / 600 | 3500 | — |
| <img src="img/ta-units/armfhlt.png" width="64" alt="Stingray" title="ARMFHLT" /> | `ARMFHLT` | Stingray | Floating Heavy Laser Tower | WATER | 524 / 5796 | 1325 | ARMFHLT_LASER |
| <img src="img/ta-units/armflak.png" width="64" alt="Flakker" title="ARMFLAK" /> | `ARMFLAK` | Flakker | Anti-Air Flak Gun | FORT | 1069 / 17425 | 1524 | ARMFLAK_GUN |
| <img src="img/ta-units/armguard.png" width="64" alt="Guardian" title="ARMGUARD" /> | `ARMGUARD` | Guardian | Plasma Battery | FORT | 1946 / 7687 | 2477 | ARMFIXED_GUN |
| <img src="img/ta-units/armhlt.png" width="64" alt="Sentinel" title="ARMHLT" /> | `ARMHLT` | Sentinel | Heavy Laser Tower | FORT | 584 / 5398 | 1230 | ARM_LASERH1 |
| <img src="img/ta-units/armllt.png" width="64" alt="L.L.T." title="ARMLLT" /> | `ARMLLT` | L.L.T. | Light Laser Tower | FORT | 262 / 2546 | 750 | ARM_LIGHTLASER |
| <img src="img/ta-units/armmanni.png" width="64" alt="Penetrator" title="ARMMANNI" /> | `ARMMANNI` | Penetrator | Mobile Energy Weapon | TANK | 2604 / 17477 | 650 | ARMMANNI_WEAPON |
| <img src="img/ta-units/armmart.png" width="64" alt="Luger" title="ARMMART" /> | `ARMMART` | Luger | Mobile Artillery | TANK | 264 / 2140 | 525 | ARM_ARTILLERY |
| <img src="img/ta-units/armmerl.png" width="64" alt="Merl" title="ARMMERL" /> | `ARMMERL` | Merl | Mobile Rocket Launcher | TANK | 462 / 2746 | 540 | ARMTRUCK_ROCKET |
| <img src="img/ta-units/armrl.png" width="64" alt="Defender" title="ARMRL" /> | `ARMRL` | Defender | Missile Tower | FORT | 79 / 843 | 295 | ARMRL_MISSILE |
| <img src="img/ta-units/armsilo.png" width="64" alt="Retaliator" title="ARMSILO" /> | `ARMSILO` | Retaliator | Nuclear Missile Launcher | SPECIAL | 1010 / 52134 | 2300 | NUCLEAR_MISSILE |
| <img src="img/ta-units/armtl.png" width="64" alt="Torpedo Launcher" title="ARMTL" /> | `ARMTL` | Torpedo Launcher | Torpedo Launcher | WATER | 804 / 2658 | 1450 | COAX_TORPEDO |
| <img src="img/ta-units/armvulc.png" width="64" alt="Vulcan" title="ARMVULC" /> | `ARMVULC` | Vulcan | Rapid Fire Plasma Cannon | FORT | 45198 / 479111 | 1400 | ARMVULC_WEAPON |


### ARM — Sensors & jammers (radar, sonar)

6 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armarad.png" width="64" alt="Advanced Radar Tower" title="ARMARAD" /> | `ARMARAD` | Advanced Radar Tower | Long Range Radar Tower | SPECIAL | 125 / 1830 | 120 | — |
| <img src="img/ta-units/armason.png" width="64" alt="Advanced Sonar Station" title="ARMASON" /> | `ARMASON` | Advanced Sonar Station | Extended Sonar | WATER | 163 / 2469 | 320 | — |
| <img src="img/ta-units/armjam.png" width="64" alt="Jammer" title="ARMJAM" /> | `ARMJAM` | Jammer | Mobile Radar Jammer | TANK | 97 / 1621 | 460 | — |
| <img src="img/ta-units/armrad.png" width="64" alt="Radar Tower" title="ARMRAD" /> | `ARMRAD` | Radar Tower | Radar Tower | SPECIAL | 49 / 750 | 51 | — |
| <img src="img/ta-units/armsjam.png" width="64" alt="Escort" title="ARMSJAM" /> | `ARMSJAM` | Escort | Radar Jammer Ship | SHIP | 131 / 1928 | 510 | — |
| <img src="img/ta-units/armsonar.png" width="64" alt="Sonar Station" title="ARMSONAR" /> | `ARMSONAR` | Sonar Station | Locates Water Units | WATER | 20 / 403 | 50 | — |


### ARM — Aircraft (VTOL, bombers, fighters)

12 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armatlas.png" width="64" alt="Atlas" title="ARMATLAS" /> | `ARMATLAS` | Atlas | Air Transport | VTOL | 107 / 2479 | 150 | — |
| <img src="img/ta-units/armawac.png" width="64" alt="Eagle" title="ARMAWAC" /> | `ARMAWAC` | Eagle | Radar Plane | VTOL | 165 / 8062 | 110 | — |
| <img src="img/ta-units/armbrawl.png" width="64" alt="Brawler" title="ARMBRAWL" /> | `ARMBRAWL` | Brawler | Gunship | VTOL | 314 / 6249 | 920 | VTOL_EMG |
| <img src="img/ta-units/armfig.png" width="64" alt="Freedom Fighter" title="ARMFIG" /> | `ARMFIG` | Freedom Fighter | Fighter | VTOL | 99 / 3234 | 196 | ARMVTOL_MISSILE |
| <img src="img/ta-units/armhawk.png" width="64" alt="Hawk" title="ARMHAWK" /> | `ARMHAWK` | Hawk | Stealth Fighter | VTOL | 254 / 6893 | 510 | ARMVTOL_ADVMISSILE, ARMVTOL_ADVMISSILE2 |
| <img src="img/ta-units/armlance.png" width="64" alt="Lancet" title="ARMLANCE" /> | `ARMLANCE` | Lancet | Torpedo Bomber | VTOL | 378 / 6438 | 370 | ARMAIR_TORPEDO |
| <img src="img/ta-units/armpeep.png" width="64" alt="Peeper" title="ARMPEEP" /> | `ARMPEEP` | Peeper | Air Scout | VTOL | 40.28 / 1475 | 80 | — |
| <img src="img/ta-units/armpnix.png" width="64" alt="Phoenix" title="ARMPNIX" /> | `ARMPNIX` | Phoenix | Bomber | VTOL | 209 / 7624 | 470 | ARMADVBOMB, ARMAIR2AIRLASER |
| <img src="img/ta-units/armseap.png" width="64" alt="Albatross" title="ARMSEAP" /> | `ARMSEAP` | Albatross | Torpedo Seaplane | VTOL | 557 / 9619 | 216 | ARMSEAP_WEAPON1, ARMSEAP_WEAPON2, ARMSEAP_WEAPON3 |
| <img src="img/ta-units/armsehak.png" width="64" alt="Seahawk" title="ARMSEHAK" /> | `ARMSEHAK` | Seahawk | Airborne Sonar | VTOL | 139 / 7624 | 470 | — |
| <img src="img/ta-units/armsfig.png" width="64" alt="Tornado" title="ARMSFIG" /> | `ARMSFIG` | Tornado | Seaplane Fighter | VTOL | 187 / 6307 | 150 | ARMSFIG_WEAPON, ARMSFIG_WEAPON2 |
| <img src="img/ta-units/armthund.png" width="64" alt="Thunder" title="ARMTHUND" /> | `ARMTHUND` | Thunder | Bomber | VTOL | 130 / 5496 | 320 | ARMBOMB |


### ARM — Ships (surface)

9 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armaas.png" width="64" alt="Archer" title="ARMAAS" /> | `ARMAAS` | Archer | Anti-Air Ship | SHIP | 1358 / 17058 | 2360 | ARMAAS_WEAPON1, ARMAAS_WEAPON2, ARMAAS_WEAPON3 |
| <img src="img/ta-units/armbats.png" width="64" alt="Millenium" title="ARMBATS" /> | `ARMBATS` | Millenium | Battleship | SHIP | 4404 / 20731 | 5720 | ARM_BATS, ARM_BATS |
| <img src="img/ta-units/armcarry.png" width="64" alt="Colossus" title="ARMCARRY" /> | `ARMCARRY` | Colossus | Light Carrier | SHIP | 1372 / 11257 | 3390 | — |
| <img src="img/ta-units/armcrus.png" width="64" alt="Conqueror" title="ARMCRUS" /> | `ARMCRUS` | Conqueror | Cruiser | SHIP | 1719 / 8608 | 4050 | ARM_CRUS, ARMDEPTHCHARGE |
| <img src="img/ta-units/armmship.png" width="64" alt="Ranger" title="ARMMSHIP" /> | `ARMMSHIP` | Ranger | Missile Ship | SHIP | 2348 / 7804 | 1200 | ARMMSHIP_ROCKET, ARMSHIP_MISSILE |
| <img src="img/ta-units/armpt.png" width="64" alt="Skeeter" title="ARMPT" /> | `ARMPT` | Skeeter | Scout Ship | SHIP | 100 / 985 | 560 | ARMPT_LASER, ARMKBOT_MISSILE |
| <img src="img/ta-units/armroy.png" width="64" alt="Crusader" title="ARMROY" /> | `ARMROY` | Crusader | Destroyer | SHIP | 898 / 4537 | 2870 | ARM_ROY, ARMDEPTHCHARGE |
| <img src="img/ta-units/armss.png" width="64" alt="Sea Serpent" title="ARMSS" /> | `ARMSS` | Sea Serpent | Indigenous Lifeform | SPECIAL | 0 / 4385 | 420 | FLAMETHROWER |
| <img src="img/ta-units/armtship.png" width="64" alt="Hulk" title="ARMTSHIP" /> | `ARMTSHIP` | Hulk | Transport Ship | SHIP | 919 / 4639 | 2000 | — |


### ARM — Submarines & underwater units

3 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armscram.png" width="64" alt="Fibber" title="ARMSCRAM" /> | `ARMSCRAM` | Fibber | Sonar Jamming Sub | WATER | 295 / 2897 | 450 | — |
| <img src="img/ta-units/armsub.png" width="64" alt="Lurker" title="ARMSUB" /> | `ARMSUB` | Lurker | Submarine | WATER | 1151 / 3724 | 610 | ARM_TORPEDO |
| <img src="img/ta-units/armsubk.png" width="64" alt="Piranha" title="ARMSUBK" /> | `ARMSUBK` | Piranha | Submarine Killer | WATER | 1448 / 5481 | 290 | ARMSMART_TORPEDO |


### ARM — Kbots (bipedal walkers)

16 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armamph.png" width="64" alt="Pelican" title="ARMAMPH" /> | `ARMAMPH` | Pelican | Amphibious Kbot | KBOT | 255 / 2468 | 800 | ARMAMPH_WEAPON1, ARMAMPH_WEAPON2 |
| <img src="img/ta-units/armaser.png" width="64" alt="Eraser" title="ARMASER" /> | `ARMASER` | Eraser | Radar Jammer | KBOT | 73 / 1326 | 305 | — |
| <img src="img/ta-units/armfast.png" width="64" alt="Zipper" title="ARMFAST" /> | `ARMFAST` | Zipper | Fast Attack Kbot | KBOT | 151 / 2221 | 550 | ARM_FAST |
| <img src="img/ta-units/armfido.png" width="64" alt="Fido" title="ARMFIDO" /> | `ARMFIDO` | Fido | Assault Kbot | KBOT | 398 / 3556 | 1000 | GAUSS |
| <img src="img/ta-units/armflea.png" width="64" alt="Flea" title="ARMFLEA" /> | `ARMFLEA` | Flea | Fast Light Scout Kbot | KBOT | 44 / 712 | 75 | ARMFLEA_WEAPON |
| <img src="img/ta-units/armham.png" width="64" alt="Hammer" title="ARMHAM" /> | `ARMHAM` | Hammer | Artillery Kbot | KBOT | 151 / 1187 | 800 | ARM_HAM |
| <img src="img/ta-units/armjeth.png" width="64" alt="Jethro" title="ARMJETH" /> | `ARMJETH` | Jethro | Anti-Air Kbot | KBOT | 128 / 1219 | 470 | ARMKBOT_MISSILE |
| <img src="img/ta-units/armmark.png" width="64" alt="Marky" title="ARMMARK" /> | `ARMMARK` | Marky | Mobile Radar Kbot | KBOT | 95 / 1152 | 320 | — |
| <img src="img/ta-units/armmav.png" width="64" alt="Maverick" title="ARMMAV" /> | `ARMMAV` | Maverick | Gun-slinging Kbot | KBOT | 492 / 10914 | 870 | ARMMAV_WEAPON |
| <img src="img/ta-units/armpw.png" width="64" alt="Peewee" title="ARMPW" /> | `ARMPW` | Peewee | Infantry Kbot | KBOT | 53 / 697 | 250 | EMG |
| <img src="img/ta-units/armrock.png" width="64" alt="Rocko" title="ARMROCK" /> | `ARMROCK` | Rocko | Rocket Kbot | KBOT | 117 / 964 | 610 | KBOT_ROCKET |
| <img src="img/ta-units/armsnipe.png" width="64" alt="Shooter" title="ARMSNIPE" /> | `ARMSNIPE` | Shooter | Sniper Kbot | KBOT | 935 / 14727 | 320 | ARMSNIPE_WEAPON |
| <img src="img/ta-units/armspy.png" width="64" alt="Infiltrator" title="ARMSPY" /> | `ARMSPY` | Infiltrator | SPY Kbot | KBOT | 128 / 9219 | 270 | — |
| <img src="img/ta-units/armvader.png" width="64" alt="Invader" title="ARMVADER" /> | `ARMVADER` | Invader | Crawling Bomb | KBOT | 61 / 5473 | 185 | — |
| <img src="img/ta-units/armwar.png" width="64" alt="Warrior" title="ARMWAR" /> | `ARMWAR` | Warrior | Medium Infantry Kbot | KBOT | 196 / 2236 | 850 | ARMWAR_LCANNON, ARMWAR_EMG |
| <img src="img/ta-units/armzeus.png" width="64" alt="Zeus" title="ARMZEUS" /> | `ARMZEUS` | Zeus | Assault Kbot | KBOT | 267 / 2228 | 875 | LIGHTNING |


### ARM — Vehicles (tanks, hovercraft, jeeps)

16 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armah.png" width="64" alt="Swatter" title="ARMAH" /> | `ARMAH` | Swatter | Anti-Air Hovercraft | TANK | 120 / 1444 | 375 | ARMAH_WEAPON |
| <img src="img/ta-units/armanac.png" width="64" alt="Anaconda" title="ARMANAC" /> | `ARMANAC` | Anaconda | Hovertank | TANK | 272 / 2856 | 880 | ARMANAC_WEAPON |
| <img src="img/ta-units/armbull.png" width="64" alt="Bulldog" title="ARMBULL" /> | `ARMBULL` | Bulldog | Heavy Assault Tank | TANK | 467 / 2994 | 2102 | ARM_BULL |
| <img src="img/ta-units/armcroc.png" width="64" alt="Triton" title="ARMCROC" /> | `ARMCROC` | Triton | Amphibious Tank | TANK | 298 / 2300 | 1230 | ARM_MEDIUMCANNON |
| <img src="img/ta-units/armfav.png" width="64" alt="Jeffy" title="ARMFAV" /> | `ARMFAV` | Jeffy | Fast Attack Vehicle | TANK | 37 / 564 | 79 | ARM_LASER |
| <img src="img/ta-units/armflash.png" width="64" alt="Flash" title="ARMFLASH" /> | `ARMFLASH` | Flash | Fast Assault Tank | TANK | 106 / 870 | 625 | EMG |
| <img src="img/ta-units/armlatnk.png" width="64" alt="Panther" title="ARMLATNK" /> | `ARMLATNK` | Panther | Lightning Tank | TANK | 354 / 3830 | 1100 | ARMLATNK_WEAPON, ARMKBOT_MISSILE |
| <img src="img/ta-units/armmh.png" width="64" alt="Wombat" title="ARMMH" /> | `ARMMH` | Wombat | Hovercraft Rocket Launcher | TANK | 325 / 3131 | 450 | ARMMH_WEAPON |
| <img src="img/ta-units/armsam.png" width="64" alt="Samson" title="ARMSAM" /> | `ARMSAM` | Samson | Mobile Missile Launcher | TANK | 119 / 1027 | 650 | ARMTRUCK_MISSILE |
| <img src="img/ta-units/armscab.png" width="64" alt="Scarab" title="ARMSCAB" /> | `ARMSCAB` | Scarab | Mobile Missile Defense | TANK | 1437 / 88000 | 780 | ARMSCAB_WEAPON |
| <img src="img/ta-units/armseer.png" width="64" alt="Seer" title="ARMSEER" /> | `ARMSEER` | Seer | Mobile Radar | TANK | 85 / 941 | 480 | — |
| <img src="img/ta-units/armsh.png" width="64" alt="Skimmer" title="ARMSH" /> | `ARMSH` | Skimmer | Scout Hovercraft | TANK | 76 / 1169 | 200 | ARMSH_WEAPON |
| <img src="img/ta-units/armspid.png" width="64" alt="Spider" title="ARMSPID" /> | `ARMSPID` | Spider | Spider Assault Vehicle | TANK | 230 / 2200 | 450 | ARM_PARALYZER |
| <img src="img/ta-units/armstump.png" width="64" alt="Stumpy" title="ARMSTUMP" /> | `ARMSTUMP` | Stumpy | Medium Assault Tank | TANK | 165 / 1246 | 992 | ARM_LIGHTCANNON |
| <img src="img/ta-units/armthovr.png" width="64" alt="Bear" title="ARMTHOVR" /> | `ARMTHOVR` | Bear | Transport Hovercraft | TANK | 665 / 7938 | 1150 | — |
| <img src="img/ta-units/armyork.png" width="64" alt="Phalanx" title="ARMYORK" /> | `ARMYORK` | Phalanx | Mobile Flak Vehicle | TANK | 830 / 10500 | 621 | ARMYORK_GUN |


### ARM — Misc / other

14 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/armasp.png" width="64" alt="Air Repair Pad" title="ARMASP" /> | `ARMASP` | Air Repair Pad | Automatically repairs aircraft | SPECIAL | 425 / 8510 | 680 | — |
| <img src="img/ta-units/armbeac.png" width="64" alt="Alien Beacon" title="ARMBEAC" /> | `ARMBEAC` | Alien Beacon | Alien Beacon | SPECIAL | 5214 / 423100 | 11000 | — |
| <img src="img/ta-units/armdev1.png" width="64" alt="Implosion Device" title="ARMDEV1" /> | `ARMDEV1` | Implosion Device | Implosion Device | SPECIAL | 8545 / 132500 | 4110 | — |
| <img src="img/ta-units/armemp.png" width="64" alt="Stunner" title="ARMEMP" /> | `ARMEMP` | Stunner | EMP Missile Launcher | SPECIAL | 1802 / 52134 | 2300 | ARMEMP_WEAPON |
| <img src="img/ta-units/armfrt.png" width="64" alt="Defender - NS" title="ARMFRT" /> | `ARMFRT` | Defender - NS | Missile Tower - Naval Series | WATER | 71 / 987 | 252 | ARMRL_MISSILE |
| <img src="img/ta-units/armgate.png" width="64" alt="Galactic Gate" title="ARMGATE" /> | `ARMGATE` | Galactic Gate | Space Teleporter | SPECIAL | 213965 / 1865294 | 2876 | — |
| <img src="img/ta-units/armmine1.png" width="64" alt="Tiny" title="ARMMINE1" /> | `ARMMINE1` | Tiny | Low Damage, Med. Range Mine | SPECIAL | 32 / 1017 | 100 | — |
| <img src="img/ta-units/armmine2.png" width="64" alt="Area Mine" title="ARMMINE2" /> | `ARMMINE2` | Area Mine | Low Damage, Large Range Mine | SPECIAL | 61 / 1909 | 100 | — |
| <img src="img/ta-units/armmine3.png" width="64" alt="Focused Mine" title="ARMMINE3" /> | `ARMMINE3` | Focused Mine | Med. Damage, Small Range Mine | SPECIAL | 86 / 2688 | 100 | — |
| <img src="img/ta-units/armmine4.png" width="64" alt="HE Area Mine" title="ARMMINE4" /> | `ARMMINE4` | HE Area Mine | Med. Damage, Large Range Mine | SPECIAL | 137 / 4294 | 100 | — |
| <img src="img/ta-units/armmine5.png" width="64" alt="Precision Mine" title="ARMMINE5" /> | `ARMMINE5` | Precision Mine | High Damage, Small Range Mine | SPECIAL | 132 / 4135 | 2000 | — |
| <img src="img/ta-units/armmine6.png" width="64" alt="Nuclear Mine" title="ARMMINE6" /> | `ARMMINE6` | Nuclear Mine | Nuclear Mine | SPECIAL | 498 / 22272 | 100 | — |
| — | `ARMSCORP` | Scorpion | Indigenous Lifeform | SPECIAL | 0 / 15660 | 1000 | ARMSCORP_WEAPON |
| <img src="img/ta-units/armtarg.png" width="64" alt="Targeting Facility" title="ARMTARG" /> | `ARMTARG` | Targeting Facility | Automatic Radar Targeting | SPECIAL | 15130 / 136058 | 1900 | — |

---

## CORE

**Core** — 141 units across 11 categories.


### CORE — Commander

2 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/corcom.png" width="64" alt="Commander" title="CORCOM" /> | `CORCOM` | Commander | Commander | COMMANDER | 23512 / 35838 | 3000 | CORCOMLASER, CORE_DISINTEGRATOR |
| <img src="img/ta-units/cordecom.png" width="64" alt="Decoy Commander" title="CORDECOM" /> | `CORDECOM` | Decoy Commander | Decoy Commander | COMMANDER | 705 / 12085 | 1580 | CORCOMLASER |


### CORE — Construction units

11 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/coraca.png" width="64" alt="Adv. Construction Aircraft" title="CORACA" /> | `CORACA` | Adv. Construction Aircraft | Tech Level 2 | CNSTR | 231 / 12824 | 370 | — |
| <img src="img/ta-units/corack.png" width="64" alt="Adv. Construction Kbot" title="CORACK" /> | `CORACK` | Adv. Construction Kbot | Tech Level 2 | CNSTR | 325 / 6096 | 1070 | — |
| <img src="img/ta-units/coracsub.png" width="64" alt="Advanced Construction Sub" title="CORACSUB" /> | `CORACSUB` | Advanced Construction Sub | Tech Level 2 | SHIP | 690 / 7911 | 370 | — |
| <img src="img/ta-units/coracv.png" width="64" alt="Adv. Construction Vehicle" title="CORACV" /> | `CORACV` | Adv. Construction Vehicle | Tech Level 2 | CNSTR | 455 / 4504 | 1220 | — |
| <img src="img/ta-units/corca.png" width="64" alt="Construction Aircraft" title="CORCA" /> | `CORCA` | Construction Aircraft | Tech Level 1 | CNSTR | 110 / 4580 | 290 | — |
| <img src="img/ta-units/corch.png" width="64" alt="Construction Hovercraft" title="CORCH" /> | `CORCH` | Construction Hovercraft | Tech Level 1 | CNSTR | 390 / 4455 | 740 | — |
| <img src="img/ta-units/corck.png" width="64" alt="Construction Kbot" title="CORCK" /> | `CORCK` | Construction Kbot | Tech Level 1 | CNSTR | 130 / 2540 | 710 | — |
| <img src="img/ta-units/corcs.png" width="64" alt="Construction Ship" title="CORCS" /> | `CORCS` | Construction Ship | Tech Level 1 | CNSTR | 260 / 2375 | 1150 | — |
| <img src="img/ta-units/corcsa.png" width="64" alt="Construction Seaplane" title="CORCSA" /> | `CORCSA` | Construction Seaplane | Tech Level 1 | VTOL | 125 / 5824 | 180 | — |
| <img src="img/ta-units/corcv.png" width="64" alt="Construction Vehicle" title="CORCV" /> | `CORCV` | Construction Vehicle | Tech Level 1 | TANK | 175 / 2145 | 825 | — |
| <img src="img/ta-units/cormlv.png" width="64" alt="Spoiler" title="CORMLV" /> | `CORMLV` | Spoiler | Mine Layer Vehicle | CNSTR | 187 / 1117 | 1400 | — |


### CORE — Production buildings (plants, labs, shipyards)

11 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/coraap.png" width="64" alt="Adv. Aircraft Plant" title="CORAAP" /> | `CORAAP` | Adv. Aircraft Plant | Produces Aircraft | PLANT | 2191 / 4422 | 2200 | — |
| <img src="img/ta-units/coralab.png" width="64" alt="Adv. Kbot Lab" title="CORALAB" /> | `CORALAB` | Adv. Kbot Lab | Produces Kbots | PLANT | 1972 / 3625 | 3170 | — |
| <img src="img/ta-units/corap.png" width="64" alt="Aircraft Plant" title="CORAP" /> | `CORAP` | Aircraft Plant | Produces Aircraft | PLANT | 830 / 1340 | 1925 | — |
| <img src="img/ta-units/corasy.png" width="64" alt="Adv. Shipyard" title="CORASY" /> | `CORASY` | Adv. Shipyard | Produces Ships | PLANT | 2460 / 2325 | 2760 | — |
| <img src="img/ta-units/coravp.png" width="64" alt="Adv. Vehicle Plant" title="CORAVP" /> | `CORAVP` | Adv. Vehicle Plant | Produces Vehicles | PLANT | 1947 / 3520 | 2580 | — |
| <img src="img/ta-units/corgant.png" width="64" alt="Krogoth Gantry" title="CORGANT" /> | `CORGANT` | Krogoth Gantry | Builds Krogoth | PLANT | 6587 / 9574 | 3050 | — |
| <img src="img/ta-units/corhp.png" width="64" alt="Hovercraft Platform" title="CORHP" /> | `CORHP` | Hovercraft Platform | Builds Hovercraft | PLANT | 1793 / 5421 | 3356 | — |
| <img src="img/ta-units/corlab.png" width="64" alt="Kbot Lab" title="CORLAB" /> | `CORLAB` | Kbot Lab | Produces Kbots | PLANT | 680 / 1250 | 2600 | — |
| <img src="img/ta-units/corplat.png" width="64" alt="Seaplane Platform" title="CORPLAT" /> | `CORPLAT` | Seaplane Platform | Builds Seaplanes | PLANT | 2305 / 5367 | 2000 | — |
| <img src="img/ta-units/corsy.png" width="64" alt="Shipyard" title="CORSY" /> | `CORSY` | Shipyard | Produces Ships | PLANT | 600 / 750 | 2490 | — |
| <img src="img/ta-units/corvp.png" width="64" alt="Vehicle Plant" title="CORVP" /> | `CORVP` | Vehicle Plant | Produces Vehicles | PLANT | 600 / 1100 | 2550 | — |


### CORE — Resource & storage buildings

20 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| — | `CORBUILD` | Hydration Plant | Creates Water | SPECIAL | 220 / 2550 | 1806 | — |
| <img src="img/ta-units/corckfus.png" width="64" alt="Cloakable Fusion Reactor" title="CORCKFUS" /> | `CORCKFUS` | Cloakable Fusion Reactor | Produces Energy | ENERGY | 5321 / 46225 | 2450 | — |
| <img src="img/ta-units/cordrag.png" width="64" alt="Dragon&#39;s Teeth" title="CORDRAG" /> | `CORDRAG` | Dragon's Teeth | Perimeter Defense | FORT | 11 / 300 | 3600 | — |
| <img src="img/ta-units/corestor.png" width="64" alt="Energy Storage" title="CORESTOR" /> | `CORESTOR` | Energy Storage | Increases Energy Storage | ENERGY | 250 / 2490 | 1070 | — |
| <img src="img/ta-units/corfmkr.png" width="64" alt="Floating Metal Maker" title="CORFMKR" /> | `CORFMKR` | Floating Metal Maker | Floating Metal Maker | METAL | — / 1530 | 120 | — |
| <img src="img/ta-units/corfort.png" width="64" alt="Fortification Wall" title="CORFORT" /> | `CORFORT` | Fortification Wall | Perimeter Defense | FORT | 23 / 612 | 1750 | — |
| <img src="img/ta-units/corfus.png" width="64" alt="Fusion Power Plant" title="CORFUS" /> | `CORFUS` | Fusion Power Plant | Produces Energy | ENERGY | 5004 / 37865 | 3000 | — |
| <img src="img/ta-units/corgeo.png" width="64" alt="Geothermal Powerplant" title="CORGEO" /> | `CORGEO` | Geothermal Powerplant | Produces Energy | ENERGY | 505 / 9375 | 930 | — |
| <img src="img/ta-units/cormakr.png" width="64" alt="Metal Maker" title="CORMAKR" /> | `CORMAKR` | Metal Maker | Metal Maker | METAL | 0 / 700 | 150 | — |
| <img src="img/ta-units/cormex.png" width="64" alt="Metal Extractor" title="CORMEX" /> | `CORMEX` | Metal Extractor | Extracts Metal | METAL | 51 / 514 | 175 | — |
| <img src="img/ta-units/cormmkr.png" width="64" alt="Moho Metal Maker" title="CORMMKR" /> | `CORMMKR` | Moho Metal Maker | Produces Metal | METAL | 51 / 10928 | 500 | — |
| <img src="img/ta-units/cormoho.png" width="64" alt="Moho Mine" title="CORMOHO" /> | `CORMOHO` | Moho Mine | Advanced Metal Extractor | METAL | 1450 / 9121 | 1465 | — |
| <img src="img/ta-units/cormstor.png" width="64" alt="Metal Storage" title="CORMSTOR" /> | `CORMSTOR` | Metal Storage | Increases Metal Storage | METAL | 320 / 550 | 1306 | — |
| <img src="img/ta-units/corsolar.png" width="64" alt="Solar Collector" title="CORSOLAR" /> | `CORSOLAR` | Solar Collector | Produces Energy | ENERGY | 141 / 790 | 320 | — |
| <img src="img/ta-units/cortide.png" width="64" alt="Tidal Generator" title="CORTIDE" /> | `CORTIDE` | Tidal Generator | Produces Energy | WATER | 81 / 752 | 253 | — |
| <img src="img/ta-units/coruwes.png" width="64" alt="Underwater Energy Storage" title="CORUWES" /> | `CORUWES` | Underwater Energy Storage | Increases Energy Storage | ENERGY | 280 / 2540 | 1521 | — |
| <img src="img/ta-units/coruwfus.png" width="64" alt="Underwater Fusion Plant" title="CORUWFUS" /> | `CORUWFUS` | Underwater Fusion Plant | Produces Energy | ENERGY | 7210 / 57349 | 1425 | — |
| <img src="img/ta-units/coruwmex.png" width="64" alt="Underwater Metal Extractor" title="CORUWMEX" /> | `CORUWMEX` | Underwater Metal Extractor | Extracts Metal | METAL | 125 / 2219 | 355 | — |
| <img src="img/ta-units/coruwms.png" width="64" alt="Underwater Metal Storage" title="CORUWMS" /> | `CORUWMS` | Underwater Metal Storage | Increases Metal Storage | METAL | 350 / 1523 | 1750 | — |
| <img src="img/ta-units/corwin.png" width="64" alt="Wind Generator" title="CORWIN" /> | `CORWIN` | Wind Generator | Produces Energy | ENERGY | 55 / 523 | 179 | — |


### CORE — Defensive structures (turrets, anti-nuke, big-bertha)

18 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/coratl.png" width="64" alt="Advanced Torpedo Launcher" title="CORATL" /> | `CORATL` | Advanced Torpedo Launcher | Advanced Torpedo Launcher | WATER | 1758 / 5389 | 562 | CORATL_TORPEDO |
| <img src="img/ta-units/corbuzz.png" width="64" alt="Buzzsaw" title="CORBUZZ" /> | `CORBUZZ` | Buzzsaw | Rapid Fire Plasma Cannon | FORT | 35264 / 462648 | 1700 | CORBUZZ_WEAPON |
| <img src="img/ta-units/cordoom.png" width="64" alt="Doomsday Machine" title="CORDOOM" /> | `CORDOOM` | Doomsday Machine | Energy Weapon | FORT | 2140 / 14245 | 3140 | CORE_DOOMSDAY, CORE_LIGHTLASER, CORE_LASERH1 |
| <img src="img/ta-units/corfdrag.png" width="64" alt="Floating Dragon&#39;s Teeth" title="CORFDRAG" /> | `CORFDRAG` | Floating Dragon's Teeth | Floating Dragon's Teeth | FORT | 18 / 630 | 3800 | — |
| <img src="img/ta-units/corfhlt.png" width="64" alt="Thunderbolt" title="CORFHLT" /> | `CORFHLT` | Thunderbolt | Floating Heavy Laser Tower | WATER | 558 / 5812 | 1385 | CORFHLT_LASER |
| <img src="img/ta-units/corflak.png" width="64" alt="Cobra" title="CORFLAK" /> | `CORFLAK` | Cobra | Anti-Air Flak Gun | FORT | 1092 / 18995 | 1655 | CORFLAK_GUN |
| <img src="img/ta-units/corfmd.png" width="64" alt="Fortitude Missile Defense" title="CORFMD" /> | `CORFMD` | Fortitude Missile Defense | Anti Missile Defense System | SPECIAL | 1508 / 92321 | 780 | FMD_ROCKET |
| <img src="img/ta-units/corhlt.png" width="64" alt="Gaat Gun" title="CORHLT" /> | `CORHLT` | Gaat Gun | Heavy Laser Tower | FORT | 589 / 5443 | 1200 | CORE_LASERH1 |
| <img src="img/ta-units/corint.png" width="64" alt="Intimidator" title="CORINT" /> | `CORINT` | Intimidator | Long Range Plasma Cannon | FORT | 4328 / 62520 | 1900 | CORE_INTIMIDATOR |
| <img src="img/ta-units/corllt.png" width="64" alt="Light Laser Tower" title="CORLLT" /> | `CORLLT` | Light Laser Tower | Light Laser Tower | FORT | 268 / 2608 | 710 | CORE_LIGHTLASER |
| <img src="img/ta-units/cormart.png" width="64" alt="Mobile Artillery" title="CORMART" /> | `CORMART` | Mobile Artillery | Mobile Artillery | TANK | 251 / 1535 | 600 | CORE_ARTILLERY |
| <img src="img/ta-units/corplas.png" width="64" alt="Immolator; //c" title="CORPLAS" /> | `CORPLAS` | Immolator; //c | Plasma Tower | FORT | 321;  //C  llt=268 / 1790;  //C llt=2608 | 842;  //C  llt=710 | CORPLAS_WEAPON |
| <img src="img/ta-units/corpun.png" width="64" alt="Punisher" title="CORPUN" /> | `CORPUN` | Punisher | Plasma Battery | FORT | 1887 / 7585 | 2540 | CORFIXED_GUN |
| <img src="img/ta-units/corrl.png" width="64" alt="Pulverizer" title="CORRL" /> | `CORRL` | Pulverizer | Missile Tower | FORT | 76 / 805 | 300 | CORRL_MISSILE |
| <img src="img/ta-units/corsilo.png" width="64" alt="Silencer" title="CORSILO" /> | `CORSILO` | Silencer | Nuclear Missile Launcher | SPECIAL | 975 / 48768 | 2560 | CRBLMSSL |
| <img src="img/ta-units/cortl.png" width="64" alt="Torpedo Launcher" title="CORTL" /> | `CORTL` | Torpedo Launcher | Torpedo Launcher | WATER | 831 / 3058 | 1520 | COAX_TORPEDO |
| <img src="img/ta-units/cortoast.png" width="64" alt="Toaster" title="CORTOAST" /> | `CORTOAST` | Toaster | Pop-up Heavy Cannon | FORT | 2146 / 12687 | 1877 | CORTOAST_GUN |
| <img src="img/ta-units/corvipe.png" width="64" alt="Viper" title="CORVIPE" /> | `CORVIPE` | Viper | Pop-Up Heavy Laser | FORT | 642 / 6687 | 988 | CORVIPE_LASER |


### CORE — Sensors & jammers (radar, sonar)

6 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/corarad.png" width="64" alt="Advanced Radar Tower" title="CORARAD" /> | `CORARAD` | Advanced Radar Tower | Long Range Radar | SPECIAL | 122 / 1920 | 130 | — |
| <img src="img/ta-units/corason.png" width="64" alt="Advanced Sonar Station" title="CORASON" /> | `CORASON` | Advanced Sonar Station | Locates Water Units | WATER | 152 / 2257 | 240 | — |
| <img src="img/ta-units/corrad.png" width="64" alt="Radar Tower" title="CORRAD" /> | `CORRAD` | Radar Tower | Radar Tower | SPECIAL | 50 / 800 | 51 | — |
| <img src="img/ta-units/corsjam.png" width="64" alt="Phantom" title="CORSJAM" /> | `CORSJAM` | Phantom | Radar Jammer Ship | SHIP | 135 / 2254 | 570 | — |
| <img src="img/ta-units/corsonar.png" width="64" alt="Sonar Station" title="CORSONAR" /> | `CORSONAR` | Sonar Station | Sonar Station | WATER | 20 / 399 | 52 | — |
| <img src="img/ta-units/corvrad.png" width="64" alt="Informer" title="CORVRAD" /> | `CORVRAD` | Informer | Mobile Radar | TANK | 86 / 1209 | 510 | — |


### CORE — Aircraft (VTOL, bombers, fighters)

12 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/corape.png" width="64" alt="Rapier" title="CORAPE" /> | `CORAPE` | Rapier | Gunship | VTOL | 294 / 5778 | 940 | VTOL_ROCKET, VTOL_ROCKET2 |
| <img src="img/ta-units/corawac.png" width="64" alt="Vulture" title="CORAWAC" /> | `CORAWAC` | Vulture | Radar Plane | VTOL | 169 / 7824 | 170 | — |
| <img src="img/ta-units/corfink.png" width="64" alt="Fink" title="CORFINK" /> | `CORFINK` | Fink | Air Scout | VTOL | 36 / 1369 | 90 | — |
| <img src="img/ta-units/corhunt.png" width="64" alt="Hunter" title="CORHUNT" /> | `CORHUNT` | Hunter | Airborne Sonar | VTOL | 142 / 7421 | 495 | — |
| <img src="img/ta-units/corhurc.png" width="64" alt="Hurricane" title="CORHURC" /> | `CORHURC` | Hurricane | Strategic Bomber | VTOL | 220 / 8050 | 480 | CORADVBOMB, CORAIR2AIRLASER |
| <img src="img/ta-units/corseap.png" width="64" alt="Typhoon" title="CORSEAP" /> | `CORSEAP` | Typhoon | Torpedo Seaplane | VTOL | 545 / 9785 | 210 | CORSEAP_WEAPON1, CORSEAP_WEAPON2, CORSEAP_WEAPON3 |
| <img src="img/ta-units/corsfig.png" width="64" alt="Voodoo" title="CORSFIG" /> | `CORSFIG` | Voodoo | Seaplane Fighter | VTOL | 182 / 6524 | 159 | CORSFIG_WEAPON, CORSFIG_WEAPON2 |
| <img src="img/ta-units/corshad.png" width="64" alt="Shadow" title="CORSHAD" /> | `CORSHAD` | Shadow | Bomber | VTOL | 131 / 5691 | 315 | CORBOMB |
| <img src="img/ta-units/cortitan.png" width="64" alt="Titan" title="CORTITAN" /> | `CORTITAN` | Titan | Torpedo Bomber | VTOL | 364 / 6588 | 375 | CORAIR_TORPEDO |
| <img src="img/ta-units/corvalk.png" width="64" alt="Valkyrie" title="CORVALK" /> | `CORVALK` | Valkyrie | Air Transport | VTOL | 115 / 2695 | 160 | — |
| <img src="img/ta-units/corvamp.png" width="64" alt="Vamp" title="CORVAMP" /> | `CORVAMP` | Vamp | Stealth Fighter | VTOL | 257 / 6973 | 490 | CORVTOL_ADVMISSILE, CORVTOL_ADVMISSILE2 |
| <img src="img/ta-units/corveng.png" width="64" alt="Avenger" title="CORVENG" /> | `CORVENG` | Avenger | Fighter | VTOL | 101 / 3181 | 202 | CORVTOL_MISSILE |


### CORE — Ships (surface)

13 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/corarch.png" width="64" alt="Shredder" title="CORARCH" /> | `CORARCH` | Shredder | Anti-Air Ship | SHIP | 1314 / 17921 | 2450 | CORARCH_WEAPON1, CORARCH_WEAPON2, CORARCH_WEAPON3 |
| <img src="img/ta-units/corbats.png" width="64" alt="Warlord" title="CORBATS" /> | `CORBATS` | Warlord | Battleship | SHIP | 4181 / 19741 | 6140 | CORE_BATSLASER, COR_BATS |
| <img src="img/ta-units/corcarry.png" width="64" alt="Hive" title="CORCARRY" /> | `CORCARRY` | Hive | Light Carrier | SHIP | 1379 / 11715 | 3500 | — |
| <img src="img/ta-units/corcrus.png" width="64" alt="Executioner" title="CORCRUS" /> | `CORCRUS` | Executioner | Cruiser | SHIP | 1724 / 8551 | 4170 | COR_CRUS, COREDEPTHCHARGE |
| <img src="img/ta-units/cormship.png" width="64" alt="Missile Frigate" title="CORMSHIP" /> | `CORMSHIP` | Missile Frigate | Missile Ship | SHIP | 2283 / 7628 | 1250 | CORMSHIP_ROCKET, CORSHIP_MISSILE |
| <img src="img/ta-units/corpt.png" width="64" alt="Searcher" title="CORPT" /> | `CORPT` | Searcher | Scout Ship | SHIP | 95 / 917 | 570 | COREPT_LASER, CORKBOT_MISSILE |
| <img src="img/ta-units/corroy.png" width="64" alt="Enforcer" title="CORROY" /> | `CORROY` | Enforcer | Destroyer | SHIP | 887 / 4505 | 3150 | CORE_ROY, COREDEPTHCHARGE |
| <img src="img/ta-units/corshark.png" width="64" alt="Shark" title="CORSHARK" /> | `CORSHARK` | Shark | Submarine Killer | SHIP | 1356 / 5245 | 276 | CORSMART_TORPEDO |
| — | `CORSS` | Sea Serpent | Indigenous Lifeform | SPECIAL | 0 / 4385 | 420 | FLAMETHROWER |
| <img src="img/ta-units/corssub.png" width="64" alt="Leviathan" title="CORSSUB" /> | `CORSSUB` | Leviathan | Battle Sub | SHIP | 3850 / 19940 | 3052 | CORSSUB_WEAPON |
| <img src="img/ta-units/corsub.png" width="64" alt="Snake" title="CORSUB" /> | `CORSUB` | Snake | Submarine | SHIP | 1199 / 3902 | 590 | CORE_TORPEDO |
| <img src="img/ta-units/corthovr.png" width="64" alt="Turtle" title="CORTHOVR" /> | `CORTHOVR` | Turtle | Transport Hovercraft | TANK | 650 / 7541 | 1080 | — |
| <img src="img/ta-units/cortship.png" width="64" alt="Envoy" title="CORTSHIP" /> | `CORTSHIP` | Envoy | Transport Ship | SHIP | 887 / 4786 | 2120 | — |


### CORE — Kbots (bipedal walkers)

17 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/corak.png" width="64" alt="A.K." title="CORAK" /> | `CORAK` | A.K. | Infantry Kbot | KBOT | 56 / 696 | 265 | CORE_LASER |
| <img src="img/ta-units/coramph.png" width="64" alt="Gimp" title="CORAMPH" /> | `CORAMPH` | Gimp | Amphibious Kbot | KBOT | 324 / 2935 | 1150 | CORAMPH_WEAPON1, CORAMPH_WEAPON2 |
| <img src="img/ta-units/corcan.png" width="64" alt="The Can" title="CORCAN" /> | `CORCAN` | The Can | Armored Assault Kbot | KBOT | 420 / 3500 | 2800 | CORE_CANLASER |
| <img src="img/ta-units/corcrash.png" width="64" alt="Crasher" title="CORCRASH" /> | `CORCRASH` | Crasher | Missile Kbot | KBOT | 129 / 1224 | 480 | CORKBOT_MISSILE |
| <img src="img/ta-units/corfast.png" width="64" alt="Freaker" title="CORFAST" /> | `CORFAST` | Freaker | Fast Attack Kbot | KBOT | 175 / 2658 | 630 | CORFAST_WEAPON |
| <img src="img/ta-units/corhrk.png" width="64" alt="Dominator" title="CORHRK" /> | `CORHRK` | Dominator | Heavy Rocket Kbot | KBOT | 388 / 2107 | 620 | CORHRK_ROCKET |
| <img src="img/ta-units/corkrog.png" width="64" alt="Krogoth" title="CORKROG" /> | `CORKROG` | Krogoth | Experimental Kbot | KBOT | 29489 / 116664 | 29918 | CORKROG_FIRE, CORKROG_HEAD, CORKROG_ROCKET |
| <img src="img/ta-units/cormort.png" width="64" alt="Morty" title="CORMORT" /> | `CORMORT` | Morty | Mobile Mortar Kbot | KBOT | 321 / 2865 | 920 | CORE_MORT |
| <img src="img/ta-units/cornecro.png" width="64" alt="Resurrection Kbot" title="CORNECRO" /> | `CORNECRO` | Resurrection Kbot | Resurrection Kbot | KBOT | 376 / 10164 | 470 | — |
| <img src="img/ta-units/corpyro.png" width="64" alt="Pyro" title="CORPYRO" /> | `CORPYRO` | Pyro | Assault Kbot | KBOT | 260 / 2200 | 700 | FLAMETHROWER |
| <img src="img/ta-units/corroach.png" width="64" alt="Roach" title="CORROACH" /> | `CORROACH` | Roach | Crawling Bomb | KBOT | 65 / 5471 | 195 | — |
| <img src="img/ta-units/corspec.png" width="64" alt="Spectre" title="CORSPEC" /> | `CORSPEC` | Spectre | Radar Jammer | KBOT | 70 / 1453 | 310 | — |
| <img src="img/ta-units/corspy.png" width="64" alt="Parasite" title="CORSPY" /> | `CORSPY` | Parasite | SPY Kbot | KBOT | 156 / 13452 | 340 | — |
| <img src="img/ta-units/corstorm.png" width="64" alt="Storm" title="CORSTORM" /> | `CORSTORM` | Storm | Rocket Kbot | KBOT | 118 / 985 | 620 | CORKBOT_ROCKET |
| <img src="img/ta-units/corsumo.png" width="64" alt="Sumo" title="CORSUMO" /> | `CORSUMO` | Sumo | Adv. Armored Assault Kbot | KBOT | 844 / 5987 | 4950 | CORSUMO_WEAPON |
| <img src="img/ta-units/corthud.png" width="64" alt="Thud" title="CORTHUD" /> | `CORTHUD` | Thud | Artillery Kbot | KBOT | 147 / 1161 | 800 | CORE_THUD |
| <img src="img/ta-units/corvoyr.png" width="64" alt="Voyeur" title="CORVOYR" /> | `CORVOYR` | Voyeur | Mobile Radar Kbot | KBOT | 93 / 1283 | 350 | — |


### CORE — Vehicles (tanks, hovercraft, jeeps)

18 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/corah.png" width="64" alt="Slinger" title="CORAH" /> | `CORAH` | Slinger | Anti-Air Hovercraft | TANK | 115 / 1542 | 395 | CORAH_WEAPON |
| <img src="img/ta-units/coreter.png" width="64" alt="Deleter" title="CORETER" /> | `CORETER` | Deleter | Mobile Radar Jammer | TANK | 100 / 1757 | 520 | — |
| <img src="img/ta-units/corfav.png" width="64" alt="Weasel" title="CORFAV" /> | `CORFAV` | Weasel | Scout | TANK | 38 / 575 | 84 | CORE_LASER |
| <img src="img/ta-units/corgator.png" width="64" alt="Instigator" title="CORGATOR" /> | `CORGATOR` | Instigator | Assault Tank | TANK | 110 / 887 | 653 | GATOR_LASER |
| <img src="img/ta-units/corgol.png" width="64" alt="Goliath" title="CORGOL" /> | `CORGOL` | Goliath | Very Heavy Assault Tank | TANK | 697 / 3906 | 2845 | COR_GOL |
| <img src="img/ta-units/corlevlr.png" width="64" alt="Leveler" title="CORLEVLR" /> | `CORLEVLR` | Leveler | Riot Tank | TANK | 292 / 1887 | 375 | CORLEVLR_WEAPON |
| <img src="img/ta-units/cormabm.png" width="64" alt="Hedgehog" title="CORMABM" /> | `CORMABM` | Hedgehog | Mobile Missile Defense | TANK | 1508 / 92321 | 780 | CORMABM_WEAPON |
| <img src="img/ta-units/cormh.png" width="64" alt="Nixer" title="CORMH" /> | `CORMH` | Nixer | Hovercraft Rocket Launcher | TANK | 318 / 3352 | 460 | CORMH_WEAPON |
| <img src="img/ta-units/cormist.png" width="64" alt="Slasher" title="CORMIST" /> | `CORMIST` | Slasher | Missile Launcher | TANK | 116 / 947 | 655 | CORTRUCK_MISSILE |
| <img src="img/ta-units/corraid.png" width="64" alt="Raider" title="CORRAID" /> | `CORRAID` | Raider | Medium Assault Tank | TANK | 169 / 1241 | 1058 | CORE_LIGHTCANNON |
| <img src="img/ta-units/correap.png" width="64" alt="Reaper" title="CORREAP" /> | `CORREAP` | Reaper | Heavy Assault Tank | TANK | 473 / 3048 | 2014 | CORE_REAP |
| <img src="img/ta-units/corscorp.png" width="64" alt="Scorpion" title="CORSCORP" /> | `CORSCORP` | Scorpion | Indigenous Lifeform | SPECIAL | 0 / 15660 | 1000 | CORSCORP_WEAPON |
| <img src="img/ta-units/corseal.png" width="64" alt="Crock" title="CORSEAL" /> | `CORSEAL` | Crock | Amphibious Tank | TANK | 295 / 2310 | 1144 | CORE_MEDIUMCANNON |
| <img src="img/ta-units/corsent.png" width="64" alt="Copperhead" title="CORSENT" /> | `CORSENT` | Copperhead | Mobile Flak Vehicle | TANK | 886 / 12487 | 685 | CORSENT_GUN |
| <img src="img/ta-units/corsh.png" width="64" alt="Scrubber" title="CORSH" /> | `CORSH` | Scrubber | Scout Hovercraft | TANK | 72 / 1252 | 200 | CORSH_WEAPON |
| <img src="img/ta-units/corsnap.png" width="64" alt="Snapper" title="CORSNAP" /> | `CORSNAP` | Snapper | Hovertank | TANK | 280 / 3069 | 850 | CORSNAP_WEAPON |
| — | `CORTRUCK` | Truck | Ground Transport | TANK | 218 / 875 | 3284 | — |
| <img src="img/ta-units/corvroc.png" width="64" alt="Diplomat" title="CORVROC" /> | `CORVROC` | Diplomat | Mobile Rocket Launcher | TANK | 427 / 2470 | 602 | CORTRUCK_ROCKET |


### CORE — Misc / other

13 units.

| | Code | Name | Description | TED | Cost (M/E) | HP | Weapons |
|:-:|------|------|-------------|-----|-----------:|---:|---------|
| <img src="img/ta-units/corasp.png" width="64" alt="Air Repair Pad" title="CORASP" /> | `CORASP` | Air Repair Pad | Automatically repairs aircraft | SPECIAL | 430 / 8540 | 690 | — |
| <img src="img/ta-units/corbeac.png" width="64" alt="Alien Beacon" title="CORBEAC" /> | `CORBEAC` | Alien Beacon | Alien Beacon | SPECIAL | 5214 / 423100 | 11000 | — |
| <img src="img/ta-units/cordev1.png" width="64" alt="Implosion Device" title="CORDEV1" /> | `CORDEV1` | Implosion Device | Implosion Device | SPECIAL | 8545 / 132500 | 4110 | — |
| <img src="img/ta-units/corfrt.png" width="64" alt="Stinger" title="CORFRT" /> | `CORFRT` | Stinger | Missile Tower - Naval Series | WATER | 72 / 1054 | 290 | CORFRT_MISSILE |
| <img src="img/ta-units/corgate.png" width="64" alt="Galactic Gate" title="CORGATE" /> | `CORGATE` | Galactic Gate | Space Teleporter | SPECIAL | 197485 / 1982431 | 2469 | — |
| <img src="img/ta-units/cormine1.png" width="64" alt="M-104" title="CORMINE1" /> | `CORMINE1` | M-104 | Low Damage, Med. Range Mine | SPECIAL | 20 / 532 | 200 | — |
| <img src="img/ta-units/cormine2.png" width="64" alt="M-209" title="CORMINE2" /> | `CORMINE2` | M-209 | Low Damage, Large Range Mine | SPECIAL | 48 / 1156 | 200 | — |
| <img src="img/ta-units/cormine3.png" width="64" alt="M-303" title="CORMINE3" /> | `CORMINE3` | M-303 | Med. Damage, Med. Range Mine | SPECIAL | 73 / 1704 | 200 | — |
| <img src="img/ta-units/cormine4.png" width="64" alt="M-420" title="CORMINE4" /> | `CORMINE4` | M-420 | High Damage, Med. Range Mine | SPECIAL | 104 / 2342 | 200 | — |
| <img src="img/ta-units/cormine5.png" width="64" alt="M-515" title="CORMINE5" /> | `CORMINE5` | M-515 | High Damage, Large Range Mine | SPECIAL | 264 / 7607 | 200 | — |
| <img src="img/ta-units/cormine6.png" width="64" alt="M-610" title="CORMINE6" /> | `CORMINE6` | M-610 | Nuclear Mine | SPECIAL | 595 / 26172 | 200 | — |
| <img src="img/ta-units/cortarg.png" width="64" alt="Targeting Facility" title="CORTARG" /> | `CORTARG` | Targeting Facility | Automatic Radar Targeting | SPECIAL | 14982 / 141148 | 1800 | — |
| <img src="img/ta-units/cortron.png" width="64" alt="Neutron" title="CORTRON" /> | `CORTRON` | Neutron | Neutron Missile Launcher | SPECIAL | 1708 / 52134 | 2100 | CORTRON_WEAPON |

---

