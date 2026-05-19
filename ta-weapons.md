# Reference — TA Weapons

Every weapon section in `weapons/*.tdf` + `gamedata/weapons.tdf` from
the v3.1c install, cross-referenced with each unit's `Weapon1/2/3=`
fields. **199 unique weapon definitions**, used (collectively) by
**132 units** (and some unused / fired only by other weapons).

Each row's `Key` is the section name in the weapon's TDF; that's the
string the unit's FBI cites in `Weapon1=` / `Weapon2=` / `Weapon3=`.
`ID` is the weapon's `ID=` field (0–255 unique-ish across the install).
Archetype tokens come from the boolean weapon flags (`ballistic`,
`lineofsight`, `dropped`, `beamweapon`, `guidance`, `selfprop`,
`twophase`, `burnblow`, `waterweapon`, `noexplode`).

See the kbot docs for column semantics:

- [TDF: weapon TDFs](https://github.com/coreprime/kbot/blob/main/docs/formats/tdf.md#tdf--feature-weapon-sound-definitions)
  — what each `weapons/*.tdf` field controls.
- [Gamedata: weapons.tdf reference](https://github.com/coreprime/kbot/blob/main/docs/formats/gamedata.md#weaponstdf--weapon-tdf-reference)
  — the engine's full weapon-field catalogue.
- [TA vs TA:K formats matrix](https://github.com/coreprime/kbot/blob/main/docs/formats/compare.md)
  — how TA's separate `weapons/*.tdf` model differs from TA:K's inline
  `[WEAPONn]` model.

> [!NOTE]
> **Not every unit-cited weapon name resolves to a definition here.**
> Some weapons are hard-coded into the engine (e.g. `BULLET`,
> `STD_MISSILE`) and have no TDF; others are macro-expanded by the
> unit's own TDF at load time. Rows marked `—` in the *Used by*
> column fall in this category.

## Contents

- [Shared engine-defined weapons](#shared-engine-defined-weapons)
- [Per-unit weapon definitions](#per-unit-weapon-definitions)
- [Other weapon files](#other-weapon-files)
- [Used-by cross-reference](#used-by-cross-reference)

---

## Shared engine-defined weapons

33 weapon definitions.

| Key | Display name | ID | Archetype | Range | AOE | Damage | Used by |
|-----|--------------|---:|-----------|------:|----:|-------:|---------|
| `AMD_ROCKET` | Rocket | 30 | lineofsight, guidance, self… | 32000 | 96 | 500 | `ARMAMD` |
| `ARMADVBOMB` | Advanced Bombs | 4 | dropped | 1280 | 59 | 195 | `ARMPNIX` |
| `ARMAIR_TORPEDO` | Torpedo Launcher | 14 | lineofsight, guidance, self… | 400 | 16 | 750 | `ARMLANCE` |
| `ARMBOMB` | Bombs | 3 | dropped | 1280 | 48 | 158 | `ARMTHUND` |
| `ARMCOMLASER` | J7 Laser | 20 | lineofsight, beamweapon | 200 | 16 | 60 | `ARMCOM`, `ARMDECOM` |
| `ARMDEPTHCHARGE` | Depth Charge | 35 | lineofsight, guidance, self… | 410 | 16 | 70 | `ARMCRUS`, `ARMROY` |
| `ARMSMART_TORPEDO` | Guided Torpedo | 12 | lineofsight, guidance, self… | 375 | 16 | 200 | `ARMSUBK` |
| `ARM_DISINTEGRATOR` | Disintegrator | 22 | lineofsight, beamweapon, no… | 240 | 48 | 30000 | `ARMCOM` |
| `ARM_PARALYZER` | Paralyzer | 29 | lineofsight, beamweapon | 220 | 8 | 900;		/* 15 seconds of paralysis */ | `ARMSPID` |
| `ARM_TORPEDO` | Unguided Torpedo | 10 | lineofsight, guidance, self… | 400 | 16 | 350 | `ARMSUB` |
| `ARM_TOTAL_ANNIHILATOR` | Annihilator Weapon | 24 | lineofsight, beamweapon | 1200 | 8 | 2500 | `ARMANNI` |
| `ATOMIC_BLAST` | Atomic Blast Weapon | 27 | ballistic | 480 | 516 | 2000 | — *(unused / engine-fired)* |
| `ATOMIC_BLASTSML` | Atomic Blast Weapon | 28 | ballistic | 480 | 260 | 1000 | — *(unused / engine-fired)* |
| `COAX_TORPEDO` | Torpedo Launcher | 9 | lineofsight, guidance, self… | 400 | 16 | 400 | `ARMTL`, `CORTL` |
| `CORADVBOMB` | Advanced Bombs | 6 | dropped | 1280 | 64 | 187 | `CORHURC` |
| `CORAIR_TORPEDO` | Torpedo Launcher | 15 | lineofsight, guidance, self… | 400 | 16 | 780 | `CORTITAN` |
| `CORBOMB` | Bombs | 5 | dropped | 1280 | 56 | 150 | `CORSHAD` |
| `CORCOMLASER` | XC Laser | 21 | lineofsight, beamweapon | 200 | 16 | 70 | `CORCOM`, `CORDECOM` |
| `COREDEPTHCHARGE` | Depth Charge | 34 | lineofsight, guidance, self… | 400 | 16 | 80 | `CORCRUS`, `CORROY` |
| `CORE_DISINTEGRATOR` | Disintegrator | 23 | lineofsight, beamweapon, no… | 240 | 48 | 30000 | `CORCOM` |
| `CORE_DOOMSDAY` | Doomsday Weapon | 25 | lineofsight, beamweapon | 600 | 8 | 2500 | `CORDOOM` |
| `CORE_TORPEDO` | Unguided Torpedo | 11 | lineofsight, guidance, self… | 400 | 16 | 370 | `CORSUB` |
| `CORSMART_TORPEDO` | Guided Torpedo | 13 | lineofsight, guidance, self… | 375 | 16 | 210 | `CORSHARK` |
| `EMG` | E.M.G. | 16 | lineofsight | 180 | 8 | 8 | `ARMFLASH`, `ARMPW` |
| `FLAMETHROWER` | Flame Thrower | 1 | ballistic | 160 | 32 | 10 | `ARMSS`, `CORPYRO`, `CORSS` |
| `FMD_ROCKET` | Rocket | 32 | lineofsight, guidance, self… | 32000 | 96 | 500 | `CORFMD` |
| `LIGHTNING` | Lightning Gun | 26 | lineofsight, beamweapon | 180 | 8 | 180 | `ARMZEUS` |
| `MINDGUN` | Mind Gun | 7 | lineofsight | 500 | 16 | 100 | — *(unused / engine-fired)* |
| `NOWEAPON` | No Weapon | 0 | — | 16 | — | 0 | — *(unused / engine-fired)* |
| `SBMISSILE` | Starburst Missile | 8 | lineofsight, guidance, self… | 300 | 16 | 80 | — *(unused / engine-fired)* |
| `VTOL_EMG` | E.M.G. | 18 | lineofsight | 370 | 8 | 11 | `ARMBRAWL` |
| `VTOL_EMG2` | E.M.G. | 19 | lineofsight | 510 | 8 | 12 | — *(unused / engine-fired)* |
| `VTOL_FOOMISSILE` | Guided Missiles | — | — | — | — | — | — *(unused / engine-fired)* |

## Per-unit weapon definitions

81 weapon definitions.

| Key | Display name | ID | Archetype | Range | AOE | Damage | Used by |
|-----|--------------|---:|-----------|------:|----:|-------:|---------|
| `ARMAAS_WEAPON1` | Missiles | 77 | lineofsight, guidance, self… | 710 | 48 | 57 | `ARMAAS` |
| `ARMAAS_WEAPON2` | Missiles | 78 | lineofsight, guidance, self… | 710 | 48 | 57 | `ARMAAS` |
| `ARMAAS_WEAPON3` | Flak Cannon | 79 | ballistic, burnblow | 750 | 125 | 146 | `ARMAAS` |
| `ARMAH_WEAPON` | Missiles | 196 | lineofsight, guidance, self… | 650 | 48 | 49 | `ARMAH` |
| `ARMAMB_GUN` | Pop-up Cannon | 40 | ballistic | 910 | 100 | 310 | `ARMAMB` |
| `ARMAMPH_WEAPON1` | Energy Laser | 156 | lineofsight, beamweapon | 260 | 8 | 60 | `ARMAMPH` |
| `ARMAMPH_WEAPON2` | Missiles | 38 | lineofsight, guidance, self… | 700 | 48 | 46 | `ARMAMPH` |
| `ARMANAC_WEAPON` | Light Guass | 153 | lineofsight | 300 | 16 | 80 | `ARMANAC` |
| `ARMATL_TORPEDO` | Unguided Torpedo | 141 | lineofsight, guidance, self… | 650 | 16 | 1000 | `ARMATL` |
| `ARMEMP_WEAPON` | Atomic Blast Weapon | 139 | lineofsight, guidance, self… | 32000 | 512 | 1 | `ARMEMP` |
| `ARMFARK_WEAPON` | Plasma Cannon | 157 | ballistic | 320 | 48 | 112 | — *(unused / engine-fired)* |
| `ARMFHLT_LASER` | High Energy Laser | 48 | lineofsight, beamweapon | 480 | 8 | 200 | `ARMFHLT` |
| `ARMFLAK_GUN` | Flak Cannon | 42 | ballistic, burnblow | 700 | 120 | 130 | `ARMFLAK` |
| `ARMFLEA_WEAPON` | Light Laser | 111 | lineofsight, beamweapon | 300 | 8 | 8 | `ARMFLEA` |
| `ARMFRT_MISSILE` | Missiles | 143 | lineofsight, guidance, self… | 700 | 48 | 46 | — *(unused / engine-fired)* |
| `ARMMANNI_WEAPON` | Annihilator Weapon | 175 | lineofsight, beamweapon | 700 | 8 | 1300 | `ARMMANNI` |
| `ARMMAV_WEAPON` | Gauss Cannon | 190 | lineofsight | 340 | 8 | 320 | `ARMMAV` |
| `ARMMH_WEAPON` | Rocket | 197 | lineofsight, guidance, self… | 670 | 80 | 300 | `ARMMH` |
| `armmine1` | Level 1 Mine | 184 | ballistic | 480 | 160 | 400 | — *(unused / engine-fired)* |
| `armmine2` | Blast Mine | 185 | ballistic | 480 | 200 | 600 | — *(unused / engine-fired)* |
| `armmine3` | Focal Mine | 186 | ballistic | 480 | 130 | 1300 | — *(unused / engine-fired)* |
| `armmine4` | Wide Blast Mine | 187 | ballistic | 480 | 180 | 1500 | — *(unused / engine-fired)* |
| `armmine5` | Whap Mine | 188 | ballistic | 480 | 130 | 2000 | — *(unused / engine-fired)* |
| `armmine6` | Nuclear Mine | 189 | ballistic | 480 | 350 | 4500 | — *(unused / engine-fired)* |
| `ARMSCAB_WEAPON` | Rocket | 117 | lineofsight, guidance, self… | 27000 | 96 | 500 | `ARMSCAB` |
| `ARMSCORP_WEAPON` | Paralyzer | 145 | lineofsight, beamweapon | 320 | 8 | 400;		/* 15 seconds of paralysis */ | `ARMSCORP` |
| `ARMSCRAM_WEAPON` | Plasma Cannon | 158 | ballistic | 320 | 48 | 112 | — *(unused / engine-fired)* |
| `ARMSEAP_WEAPON1` | Torpedo Launcher | 146 | lineofsight, guidance, self… | 300 | 16 | 400 | `ARMSEAP` |
| `ARMSEAP_WEAPON2` | Torpedo Launcher | 193 | lineofsight, guidance, self… | 300 | 16 | 400 | `ARMSEAP` |
| `ARMSEAP_WEAPON3` | Guided Missiles | 95 | lineofsight, guidance, self… | 510 | 48 | 44 | `ARMSEAP` |
| `ARMSEHAK_WEAPON` | Plasma Cannon | 164 | ballistic | 320 | 48 | 112 | — *(unused / engine-fired)* |
| `ARMSFIG_WEAPON` | Guided Missiles | 75 | lineofsight, guidance, self… | 510 | 48 | 50 | `ARMSFIG` |
| `ARMSFIG_WEAPON2` | Guided Missiles | 96 | lineofsight, guidance, self… | 510 | 48 | 50 | `ARMSFIG` |
| `ARMSH_WEAPON` | Laser | 195 | lineofsight, beamweapon | 210 | 8 | 45 | `ARMSH` |
| `ARMSNIPE_WEAPON` | Annihilator Weapon | 160 | lineofsight, beamweapon | 600 | 8 | 1230 | `ARMSNIPE` |
| `ARMVULC_WEAPON` | Bertha Cannon | 2 | ballistic | 3080 | 100 | 1000 | `ARMVULC` |
| `ARMWAR_EMG` | E.M.G. | 171 | lineofsight | 180 | 8 | 12 | `ARMWAR` |
| `ARMWAR_LCANNON` | Light Cannon | 176 | ballistic | 240 | 32 | 60 | `ARMWAR` |
| `ARMyork_GUN` | Flak Cannon | 116 | ballistic, burnblow | 680 | 105 | 128 | `ARMYORK` |
| `CORAH_WEAPON` | Missiles | 199 | lineofsight, guidance, self… | 600 | 48 | 46 | `CORAH` |
| `CORAMPH_WEAPON1` | Plasma Cannon | 159 | ballistic | 230 | 48 | 80; //105 | `CORAMPH` |
| `CORAMPH_WEAPON2` | High Energy Laser | 192 | lineofsight, beamweapon | 300 | 12 | 90 | `CORAMPH` |
| `CORARCH_WEAPON1` | Missiles | 178 | lineofsight, guidance, self… | 710 | 48 | 57 | `CORARCH` |
| `CORARCH_WEAPON2` | Missiles | 179 | lineofsight, guidance, self… | 710 | 48 | 57 | `CORARCH` |
| `CORARCH_WEAPON3` | Flak Cannon | 180 | ballistic, burnblow | 750 | 125 | 146 | `CORARCH` |
| `CORATL_TORPEDO` | Unguided Torpedo | 147 | lineofsight, guidance, self… | 600 | 16 | 1000 | `CORATL` |
| `CORBUZZ_WEAPON` | Bertha Cannon | 84 | ballistic | 3800 | 120 | 1800 | `CORBUZZ` |
| `CORE_MORT` | Plasma Cannon | 46 | ballistic | 655 | 36 | 55 | `CORMORT` |
| `CORFAST_WEAPON` | Laser | 161 | lineofsight, beamweapon | 180 | 8 | 47 | `CORFAST` |
| `CORFHLT_LASER` | High Energy Laser | 49 | lineofsight, beamweapon | 410 | 8 | 195 | `CORFHLT` |
| `CORFLAK_GUN` | Flak Cannon | 43 | ballistic, burnblow | 750 | 125 | 146 | `CORFLAK` |
| `CORFRT_MISSILE` | Missiles | 148 | lineofsight, guidance, self… | 700 | 48 | 45 | `CORFRT` |
| `CORHRK_ROCKET` | Heavy Rockets | 45 | lineofsight, guidance, self… | 600 | 60 | 240 | `CORHRK` |
| `CORHUNT_WEAPON` | Plasma Cannon | 162 | ballistic | 320 | 48 | 112 | — *(unused / engine-fired)* |
| `CORKROG_FIRE` | Gauss Cannon | 150 | lineofsight | 300 | 8 | 480 | `CORKROG` |
| `CORKROG_HEAD` | Annihilator Weapon | 149 | lineofsight, beamweapon | 700 | 8 | 2500 | `CORKROG` |
| `CORKROG_ROCKET` | Heavy Rockets | 151 | lineofsight, guidance, self… | 900 | 80 | 131 | `CORKROG` |
| `CORLEVLR_WEAPON` | Light Cannon | 172 | ballistic | 260 | 84 | 180 | `CORLEVLR` |
| `CORMABM_WEAPON` | Rocket | 118 | lineofsight, guidance, self… | 22000 | 96 | 500 | `CORMABM` |
| `CORMH_WEAPON` | Rocket | 39 | lineofsight, guidance, self… | 650 | 80 | 320 | `CORMH` |
| `cormine1` | Level 1 Mine | 33 | ballistic | 480 | 175 | 200 | — *(unused / engine-fired)* |
| `cormine2` | Blast Mine | 36 | ballistic | 480 | 190 | 400 | — *(unused / engine-fired)* |
| `cormine3` | Focal Mine | 37 | ballistic | 480 | 160 | 700 | — *(unused / engine-fired)* |
| `cormine4` | Wide Blast Mine | 61 | ballistic | 480 | 140 | 1100 | — *(unused / engine-fired)* |
| `cormine5` | Whap Mine | 63 | ballistic | 480 | 250 | 2000 | — *(unused / engine-fired)* |
| `cormine6` | Nuclear Mine | 74 | ballistic | 480 | 400 | 4300 | — *(unused / engine-fired)* |
| `CORPLAS_WEAPON` | Immolator | 138 | lineofsight | 320;  //fl=180 llt=300 | 70;  //fl=8  llt=8 | 10;  //fl=12 llt=60 | `CORPLAS` |
| `CORSCORP_WEAPON` | Paralyzer | 181 | lineofsight, beamweapon | 320 | 8 | 400;		/* 15 seconds of paralysis */ | `CORSCORP` |
| `CORSEAP_WEAPON1` | Torpedo Launcher | 152 | lineofsight, guidance, self… | 300 | 16 | 400 | `CORSEAP` |
| `CORSEAP_WEAPON2` | Torpedo Launcher | 194 | lineofsight, guidance, self… | 300 | 16 | 400 | `CORSEAP` |
| `CORSEAP_WEAPON3` | Guided Missiles | 98 | lineofsight, guidance, self… | 510 | 48 | 44 | `CORSEAP` |
| `CORSENT_GUN` | Flak Cannon | 133 | ballistic, burnblow | 720 | 110 | 130 | `CORSENT` |
| `CORSFIG_WEAPON` | Guided Missiles | 76 | lineofsight, guidance, self… | 510 | 48 | 50 | `CORSFIG` |
| `CORSFIG_WEAPON2` | Guided Missiles | 97 | lineofsight, guidance, self… | 510 | 48 | 50 | `CORSFIG` |
| `CORSH_WEAPON` | Laser | 198 | lineofsight, beamweapon | 230 | 8 | 40 | `CORSH` |
| `CORSNAP_WEAPON` | Plasma Cannon | 154 | ballistic | 290 | 48 | 85 | `CORSNAP` |
| `CORSSUB_WEAPON` | Unguided Torpedo | 183 | lineofsight, guidance, self… | 500 | 5 | 812 | `CORSSUB` |
| `CORSUMO_WEAPON` | High Energy Laser | 174 | lineofsight, beamweapon | 300 | 12 | 290 | `CORSUMO` |
| `CORTOAST_GUN` | Pop-up Cannon | 44 | ballistic | 885 | 105 | 295 | `CORTOAST` |
| `CORTRON_WEAPON` | Atomic Blast Weapon | 144 | lineofsight, guidance, self… | 32000 | 362 | 1 | `CORTRON` |
| `CORVIPE_LASER` | Laser | 47 | lineofsight, beamweapon | 380 | 8 | 140 | `CORVIPE` |

## Other weapon files

85 weapon definitions.

| Key | Display name | ID | Archetype | Range | AOE | Damage | Used by |
|-----|--------------|---:|-----------|------:|----:|-------:|---------|
| `ARMAIR2AIRLASER` | Laser | 86 | lineofsight, beamweapon | 600 | 8 | 6 | `ARMPNIX` |
| `ARMFIXED_GUN` | Plasma Cannon | 70 | ballistic | 1250 | 64 | 360 | `ARMGUARD` |
| `ARMKBOT_MISSILE` | Missiles | 100 | lineofsight, guidance, self… | 604 | 48 | 31 | `ARMJETH`, `ARMLATNK`, `ARMPT` |
| `Armlatnk_weapon` | Lightning Gun | 166 | lineofsight, beamweapon | 210 | 8 | 120 | `ARMLATNK` |
| `ARMMSHIP_ROCKET` | Rocket | 128 | lineofsight, guidance, self… | 1300 | 96 | 500 | `ARMMSHIP` |
| `ARMPT_LASER` | Laser | 89 | lineofsight, beamweapon | 180 | 8 | 13 | `ARMPT` |
| `ARMRL_MISSILE` | Missiles | 106 | lineofsight, guidance, self… | 700 | 48 | 46 | `ARMFRT`, `ARMRL` |
| `ARMSHIP_MISSILE` | Missiles | 103 | lineofsight, guidance, self… | 710 | 48 | 57 | `ARMMSHIP` |
| `ARMTRUCK_MISSILE` | Missiles | 104 | lineofsight, guidance, self… | 600 | 48 | 40 | `ARMSAM` |
| `ARMTRUCK_ROCKET` | Rocket | 124 | lineofsight, guidance, self… | 800 | 96 | 500 | `ARMMERL` |
| `ARMVTOL_ADVMISSILE` | Guided Missiles | 112 | lineofsight, guidance, self… | 659 | 48 | 70 | `ARMHAWK` |
| `ARMVTOL_ADVMISSILE2` | Guided Missiles | 115 | lineofsight, guidance, self… | 659 | 48 | 70 | `ARMHAWK` |
| `ARMVTOL_MISSILE` | Guided Missiles | 108 | lineofsight, guidance, self… | 510 | 48 | 44 | `ARMFIG` |
| `ARM_ARTILLERY` | Plasma Cannon | 58 | ballistic | 620 | 48 | 130 | `ARMMART` |
| `ARM_BATS` | BattleShip Cannon | 68 | ballistic | 1250 | 64 | 260 | `ARMBATS`, `ARMBATS` |
| `ARM_BERTHACANNON` | Bertha Cannon | 72 | ballistic | 4096 | 80 | 2000 | `ARMBRTHA` |
| `ARM_BULL` | Plasma Cannon | 56 | ballistic | 320 | 48 | 147; //110 7-10-97 | `ARMBULL` |
| `ARM_CRUS` | Cruiser Cannon | 66 | ballistic | 1300 | 64 | 208 | `ARMCRUS` |
| `ARM_FAST` | Laser | 83 | lineofsight, beamweapon | 210 | 8 | 40 | `ARMFAST` |
| `ARM_HAM` | Plasma Cannon | 54 | ballistic | 320 | 48 | 85; //110 | `ARMHAM` |
| `ARM_LASER` | Laser | 82 | lineofsight, beamweapon | 180 | 8 | 30 | `ARMFAV` |
| `ARM_LASERH1` | High Energy Laser | 91 | lineofsight, beamweapon | 430 | 8 | 180 | `ARMHLT` |
| `ARM_LIGHTCANNON` | Light Cannon | 50 | ballistic | 240 | 32 | 50 | `ARMSTUMP` |
| `ARM_LIGHTLASER` | Light Laser | 80 | lineofsight, beamweapon | 300 | 8 | 60 | `ARMLLT` |
| `ARM_MEDIUMCANNON` | Plasma Cannon | 52 | ballistic | 320 | 48 | 112 | `ARMCROC` |
| `ARM_ROY` | Heavy Cannon | 64 | ballistic | 660 | 48 | 165 | `ARMROY` |
| `BIG_UNIT` | Big Kbot | 205 | ballistic | 480 | 110 | 350 | — *(unused / engine-fired)* |
| `BIG_UNITEX` | Big Kbot | 211 | ballistic | 480 | 110 | 50 | — *(unused / engine-fired)* |
| `COMMANDER_BLAST` | Atomic Blast Weapon | 213 | ballistic | 380 | 950 | 9999 | — *(unused / engine-fired)* |
| `CORAIR2AIRLASER` | Laser | 87 | lineofsight, beamweapon | 600 | 8 | 5 | `CORHURC` |
| `COREPT_LASER` | Laser | 90 | lineofsight, beamweapon | 180 | 8 | 10 | `CORPT` |
| `CORE_ARTILLERY` | Plasma Cannon | 59 | ballistic | 620 | 48 | 140 | `CORMART` |
| `CORE_BATSLASER` | High Energy Laser | 93 | lineofsight, beamweapon | 810 | 8 | 180 | `CORBATS` |
| `CORE_CANLASER` | High Energy Laser | 94 | lineofsight, beamweapon | 200 | 8 | 220 | `CORCAN` |
| `CORE_INTIMIDATOR` | Intimidator Cannon | 73 | ballistic | 5120 | 100 | 2400 | `CORINT` |
| `CORE_LASER` | Laser | 88 | lineofsight, beamweapon | 180 | 8 | 30 | `CORAK`, `CORFAV` |
| `CORE_LASERH1` | High Energy Laser | 92 | lineofsight, beamweapon | 400 | 8 | 180 | `CORDOOM`, `CORHLT` |
| `CORE_LIGHTCANNON` | Light Cannon | 51 | ballistic | 240 | 32 | 50 | `CORRAID` |
| `CORE_LIGHTLASER` | Light Laser | 81 | lineofsight, beamweapon | 300 | 8 | 60 | `CORDOOM`, `CORLLT` |
| `CORE_MEDIUMCANNON` | Plasma Cannon | 53 | ballistic | 320 | 48 | 127 | `CORSEAL` |
| `CORE_REAP` | Plasma Cannon | 57 | ballistic | 320 | 48 | 143; //110 7-10-97 | `CORREAP` |
| `CORE_ROY` | Heavy Cannon | 65 | ballistic | 660 | 48 | 180 | `CORROY` |
| `CORE_THUD` | Plasma Cannon | 55 | ballistic | 230 | 48 | 80; //105 | `CORTHUD` |
| `CORFIXED_GUN` | Plasma Cannon | 71 | ballistic | 1200 | 85 | 320 | `CORPUN` |
| `CORKBOT_MISSILE` | Missiles | 101 | lineofsight, guidance, self… | 590 | 48 | 32 | `CORCRASH`, `CORPT` |
| `CORKBOT_ROCKET` | Rockets | 121 | lineofsight, selfprop | 400 | 48 | 100 | `CORSTORM` |
| `CORMSHIP_ROCKET` | Rocket | 130 | lineofsight, guidance, self… | 1300 | 96 | 500 | `CORMSHIP` |
| `CORPYRO_BLAST` | Pyro Blast | 212 | ballistic | 480 | 128 | 60 | — *(unused / engine-fired)* |
| `CORRL_MISSILE` | Missiles | 107 | lineofsight, guidance, self… | 700 | 48 | 45 | `CORRL` |
| `CORSHIP_MISSILE` | Missiles | 102 | lineofsight, guidance, self… | 700 | 48 | 62 | `CORMSHIP` |
| `CORTRUCK_MISSILE` | Missiles | 105 | lineofsight, guidance, self… | 600 | 48 | 41 | `CORMIST` |
| `CORTRUCK_ROCKET` | Rocket | 126 | lineofsight, guidance, self… | 800 | 96 | 500 | `CORVROC` |
| `CORVTOL_ADVMISSILE` | Guided Missiles | 113 | lineofsight, guidance, self… | 650 | 48 | 68 | `CORVAMP` |
| `CORVTOL_ADVMISSILE2` | Guided Missiles | 114 | lineofsight, guidance, self… | 650 | 48 | 68 | `CORVAMP` |
| `CORVTOL_MISSILE` | Guided Missiles | 109 | lineofsight, guidance, self… | 502 | 48 | 46 | `CORVENG` |
| `COR_BATS` | BattleShip Cannon | 69 | ballistic | 1250 | 64 | 270 | `CORBATS` |
| `COR_CRUS` | Cruiser Cannon | 67 | ballistic | 1300 | 64 | 220 | `CORCRUS` |
| `COR_GOL` | Heavy Cannon | 62 | ballistic | 400 | 64 | 196 | `CORGOL` |
| `CRAWL_BLAST` | Crawling Bomb | 214 | ballistic | 480 | 556 | 2500 | — *(unused / engine-fired)* |
| `CRAWL_BLASTSML` | Wimpy Crawling Bomb | 215 | ballistic | 480 | 275 | 1200 | — *(unused / engine-fired)* |
| `CRBLMSSL` | Rocket | 123 | lineofsight, guidance, self… | 32000 | 512 | 5500 | `CORSILO` |
| `DECOY_COMMANDER_BLAST` | Atomic Blast Weapon | 155 | ballistic | 380 | 950 | 100 | — *(unused / engine-fired)* |
| `EARTHQUAKE` | Earthquake | 227 | — | — | 512 | 50 | — *(unused / engine-fired)* |
| `ESTOR_BUILDING` | Small building | 203 | ballistic | 480 | 420 | 1900 | — *(unused / engine-fired)* |
| `ESTOR_BUILDINGEX` | Small building | 209 | ballistic | 480 | 150 | 900 | — *(unused / engine-fired)* |
| `GASBAG` | Gas Bag | 99 | — | — | 140 | 500 | — *(unused / engine-fired)* |
| `GATOR_LASER` | Laser | 85 | lineofsight, beamweapon | 180 | 8 | 44 | `CORGATOR` |
| `GAUSS` | Gauss Cannon | 60 | lineofsight | 480 | 8 | 120 | `ARMFIDO` |
| `HAILSTORM` | Hail storm | 226 | — | — | 32 | 50 | — *(unused / engine-fired)* |
| `KBOT_ROCKET` | Rockets | 120 | lineofsight, selfprop | 400 | 48 | 105 | `ARMROCK` |
| `LARGE_BUILDING` | Large building | 202 | ballistic | 480 | 400 | 1800 | — *(unused / engine-fired)* |
| `LARGE_BUILDINGEX` | Large building | 208 | ballistic | 480 | 120 | 300 | — *(unused / engine-fired)* |
| `MEDIUM_BUILDING` | Medium building | 201 | ballistic | 480 | 325 | 1400 | — *(unused / engine-fired)* |
| `MEDIUM_BUILDINGEX` | Medium building | 207 | ballistic | 480 | 105 | 100 | — *(unused / engine-fired)* |
| `MEDIUM_UNIT` | Medium Unit | 110 | ballistic | 480 | 95 | 250 | — *(unused / engine-fired)* |
| `METEOR` | Meteor | 225 | — | — | 100 | 100 | — *(unused / engine-fired)* |
| `NUCLEAR_MISSILE` | Nuclear Missile | 122 | lineofsight, guidance, self… | 32000 | 512 | 5500 | `ARMSILO` |
| `SHRUBBURN` | Burning Bush | 246 | — | — | 48 | 50 | — *(unused / engine-fired)* |
| `SMALL_BUILDING` | Small building | 200 | ballistic | 480 | 205 | 900 | — *(unused / engine-fired)* |
| `SMALL_BUILDINGEX` | Small building | 206 | ballistic | 480 | 205 | 40 | — *(unused / engine-fired)* |
| `SMALL_UNIT` | Small tank | 204 | ballistic | 480 | 75 | 200 | — *(unused / engine-fired)* |
| `SMALL_UNITEX` | Small tank | 210 | ballistic | 480 | 30 | 30 | — *(unused / engine-fired)* |
| `TREEBURN` | Burning Tree | 245 | — | — | 64 | 100 | — *(unused / engine-fired)* |
| `VTOL_ROCKET` | Rockets | 135 | lineofsight, selfprop | 450 | 48 | 125 | `CORAPE` |
| `VTOL_ROCKET2` | Rockets | 136 | lineofsight, selfprop | 450 | 48 | 125 | `CORAPE` |

---

## Used-by cross-reference

Every weapon string referenced by a unit FBI's `Weapon1/2/3=`,
sorted alphabetically with the units that use it.

| Weapon key | Defined? | Used by |
|------------|:--------:|---------|
| `AMD_ROCKET` | ✅  | `ARMAMD` |
| `ARMAAS_WEAPON1` | ✅  | `ARMAAS` |
| `ARMAAS_WEAPON2` | ✅  | `ARMAAS` |
| `ARMAAS_WEAPON3` | ✅  | `ARMAAS` |
| `ARMADVBOMB` | ✅  | `ARMPNIX` |
| `ARMAH_WEAPON` | ✅  | `ARMAH` |
| `ARMAIR2AIRLASER` | ✅  | `ARMPNIX` |
| `ARMAIR_TORPEDO` | ✅  | `ARMLANCE` |
| `ARMAMB_GUN` | ✅  | `ARMAMB` |
| `ARMAMPH_WEAPON1` | ✅  | `ARMAMPH` |
| `ARMAMPH_WEAPON2` | ✅  | `ARMAMPH` |
| `ARMANAC_WEAPON` | ✅  | `ARMANAC` |
| `ARMATL_TORPEDO` | ✅  | `ARMATL` |
| `ARMBOMB` | ✅  | `ARMTHUND` |
| `ARMCOMLASER` | ✅  | `ARMCOM`, `ARMDECOM` |
| `ARMDEPTHCHARGE` | ✅  | `ARMCRUS`, `ARMROY` |
| `ARMEMP_WEAPON` | ✅  | `ARMEMP` |
| `ARMFHLT_LASER` | ✅  | `ARMFHLT` |
| `ARMFIXED_GUN` | ✅  | `ARMGUARD` |
| `ARMFLAK_GUN` | ✅  | `ARMFLAK` |
| `ARMFLEA_WEAPON` | ✅  | `ARMFLEA` |
| `ARMKBOT_MISSILE` | ✅  | `ARMJETH`, `ARMLATNK`, `ARMPT` |
| `ARMLATNK_WEAPON` | ✅  | `ARMLATNK` |
| `ARMMANNI_WEAPON` | ✅  | `ARMMANNI` |
| `ARMMAV_WEAPON` | ✅  | `ARMMAV` |
| `ARMMH_WEAPON` | ✅  | `ARMMH` |
| `ARMMSHIP_ROCKET` | ✅  | `ARMMSHIP` |
| `ARMPT_LASER` | ✅  | `ARMPT` |
| `ARMRL_MISSILE` | ✅  | `ARMFRT`, `ARMRL` |
| `ARMSCAB_WEAPON` | ✅  | `ARMSCAB` |
| `ARMSCORP_WEAPON` | ✅  | `ARMSCORP` |
| `ARMSEAP_WEAPON1` | ✅  | `ARMSEAP` |
| `ARMSEAP_WEAPON2` | ✅  | `ARMSEAP` |
| `ARMSEAP_WEAPON3` | ✅  | `ARMSEAP` |
| `ARMSFIG_WEAPON` | ✅  | `ARMSFIG` |
| `ARMSFIG_WEAPON2` | ✅  | `ARMSFIG` |
| `ARMSHIP_MISSILE` | ✅  | `ARMMSHIP` |
| `ARMSH_WEAPON` | ✅  | `ARMSH` |
| `ARMSMART_TORPEDO` | ✅  | `ARMSUBK` |
| `ARMSNIPE_WEAPON` | ✅  | `ARMSNIPE` |
| `ARMTRUCK_MISSILE` | ✅  | `ARMSAM` |
| `ARMTRUCK_ROCKET` | ✅  | `ARMMERL` |
| `ARMVTOL_ADVMISSILE` | ✅  | `ARMHAWK` |
| `ARMVTOL_ADVMISSILE2` | ✅  | `ARMHAWK` |
| `ARMVTOL_MISSILE` | ✅  | `ARMFIG` |
| `ARMVULC_WEAPON` | ✅  | `ARMVULC` |
| `ARMWAR_EMG` | ✅  | `ARMWAR` |
| `ARMWAR_LCANNON` | ✅  | `ARMWAR` |
| `ARMYORK_GUN` | ✅  | `ARMYORK` |
| `ARM_ARTILLERY` | ✅  | `ARMMART` |
| `ARM_BATS` | ✅  | `ARMBATS`, `ARMBATS` |
| `ARM_BERTHACANNON` | ✅  | `ARMBRTHA` |
| `ARM_BULL` | ✅  | `ARMBULL` |
| `ARM_CRUS` | ✅  | `ARMCRUS` |
| `ARM_DISINTEGRATOR` | ✅  | `ARMCOM` |
| `ARM_FAST` | ✅  | `ARMFAST` |
| `ARM_HAM` | ✅  | `ARMHAM` |
| `ARM_LASER` | ✅  | `ARMFAV` |
| `ARM_LASERH1` | ✅  | `ARMHLT` |
| `ARM_LIGHTCANNON` | ✅  | `ARMSTUMP` |
| `ARM_LIGHTLASER` | ✅  | `ARMLLT` |
| `ARM_MEDIUMCANNON` | ✅  | `ARMCROC` |
| `ARM_PARALYZER` | ✅  | `ARMSPID` |
| `ARM_ROY` | ✅  | `ARMROY` |
| `ARM_TORPEDO` | ✅  | `ARMSUB` |
| `ARM_TOTAL_ANNIHILATOR` | ✅  | `ARMANNI` |
| `COAX_TORPEDO` | ✅  | `ARMTL`, `CORTL` |
| `CORADVBOMB` | ✅  | `CORHURC` |
| `CORAH_WEAPON` | ✅  | `CORAH` |
| `CORAIR2AIRLASER` | ✅  | `CORHURC` |
| `CORAIR_TORPEDO` | ✅  | `CORTITAN` |
| `CORAMPH_WEAPON1` | ✅  | `CORAMPH` |
| `CORAMPH_WEAPON2` | ✅  | `CORAMPH` |
| `CORARCH_WEAPON1` | ✅  | `CORARCH` |
| `CORARCH_WEAPON2` | ✅  | `CORARCH` |
| `CORARCH_WEAPON3` | ✅  | `CORARCH` |
| `CORATL_TORPEDO` | ✅  | `CORATL` |
| `CORBOMB` | ✅  | `CORSHAD` |
| `CORBUZZ_WEAPON` | ✅  | `CORBUZZ` |
| `CORCOMLASER` | ✅  | `CORCOM`, `CORDECOM` |
| `COREDEPTHCHARGE` | ✅  | `CORCRUS`, `CORROY` |
| `COREPT_LASER` | ✅  | `CORPT` |
| `CORE_ARTILLERY` | ✅  | `CORMART` |
| `CORE_BATSLASER` | ✅  | `CORBATS` |
| `CORE_CANLASER` | ✅  | `CORCAN` |
| `CORE_DISINTEGRATOR` | ✅  | `CORCOM` |
| `CORE_DOOMSDAY` | ✅  | `CORDOOM` |
| `CORE_INTIMIDATOR` | ✅  | `CORINT` |
| `CORE_LASER` | ✅  | `CORAK`, `CORFAV` |
| `CORE_LASERH1` | ✅  | `CORDOOM`, `CORHLT` |
| `CORE_LIGHTCANNON` | ✅  | `CORRAID` |
| `CORE_LIGHTLASER` | ✅  | `CORDOOM`, `CORLLT` |
| `CORE_MEDIUMCANNON` | ✅  | `CORSEAL` |
| `CORE_MORT` | ✅  | `CORMORT` |
| `CORE_REAP` | ✅  | `CORREAP` |
| `CORE_ROY` | ✅  | `CORROY` |
| `CORE_THUD` | ✅  | `CORTHUD` |
| `CORE_TORPEDO` | ✅  | `CORSUB` |
| `CORFAST_WEAPON` | ✅  | `CORFAST` |
| `CORFHLT_LASER` | ✅  | `CORFHLT` |
| `CORFIXED_GUN` | ✅  | `CORPUN` |
| `CORFLAK_GUN` | ✅  | `CORFLAK` |
| `CORFRT_MISSILE` | ✅  | `CORFRT` |
| `CORHRK_ROCKET` | ✅  | `CORHRK` |
| `CORKBOT_MISSILE` | ✅  | `CORCRASH`, `CORPT` |
| `CORKBOT_ROCKET` | ✅  | `CORSTORM` |
| `CORKROG_FIRE` | ✅  | `CORKROG` |
| `CORKROG_HEAD` | ✅  | `CORKROG` |
| `CORKROG_ROCKET` | ✅  | `CORKROG` |
| `CORLEVLR_WEAPON` | ✅  | `CORLEVLR` |
| `CORMABM_WEAPON` | ✅  | `CORMABM` |
| `CORMH_WEAPON` | ✅  | `CORMH` |
| `CORMSHIP_ROCKET` | ✅  | `CORMSHIP` |
| `CORPLAS_WEAPON` | ✅  | `CORPLAS` |
| `CORRL_MISSILE` | ✅  | `CORRL` |
| `CORSCORP_WEAPON` | ✅  | `CORSCORP` |
| `CORSEAP_WEAPON1` | ✅  | `CORSEAP` |
| `CORSEAP_WEAPON2` | ✅  | `CORSEAP` |
| `CORSEAP_WEAPON3` | ✅  | `CORSEAP` |
| `CORSENT_GUN` | ✅  | `CORSENT` |
| `CORSFIG_WEAPON` | ✅  | `CORSFIG` |
| `CORSFIG_WEAPON2` | ✅  | `CORSFIG` |
| `CORSHIP_MISSILE` | ✅  | `CORMSHIP` |
| `CORSH_WEAPON` | ✅  | `CORSH` |
| `CORSMART_TORPEDO` | ✅  | `CORSHARK` |
| `CORSNAP_WEAPON` | ✅  | `CORSNAP` |
| `CORSSUB_WEAPON` | ✅  | `CORSSUB` |
| `CORSUMO_WEAPON` | ✅  | `CORSUMO` |
| `CORTOAST_GUN` | ✅  | `CORTOAST` |
| `CORTRON_WEAPON` | ✅  | `CORTRON` |
| `CORTRUCK_MISSILE` | ✅  | `CORMIST` |
| `CORTRUCK_ROCKET` | ✅  | `CORVROC` |
| `CORVIPE_LASER` | ✅  | `CORVIPE` |
| `CORVTOL_ADVMISSILE` | ✅  | `CORVAMP` |
| `CORVTOL_ADVMISSILE2` | ✅  | `CORVAMP` |
| `CORVTOL_MISSILE` | ✅  | `CORVENG` |
| `COR_BATS` | ✅  | `CORBATS` |
| `COR_CRUS` | ✅  | `CORCRUS` |
| `COR_GOL` | ✅  | `CORGOL` |
| `CRBLMSSL` | ✅  | `CORSILO` |
| `EMG` | ✅  | `ARMFLASH`, `ARMPW` |
| `FLAMETHROWER` | ✅  | `ARMSS`, `CORPYRO`, `CORSS` |
| `FMD_ROCKET` | ✅  | `CORFMD` |
| `GATOR_LASER` | ✅  | `CORGATOR` |
| `GAUSS` | ✅  | `ARMFIDO` |
| `KBOT_ROCKET` | ✅  | `ARMROCK` |
| `LIGHTNING` | ✅  | `ARMZEUS` |
| `NUCLEAR_MISSILE` | ✅  | `ARMSILO` |
| `VTOL_EMG` | ✅  | `ARMBRAWL` |
| `VTOL_ROCKET` | ✅  | `CORAPE` |
| `VTOL_ROCKET2` | ✅  | `CORAPE` |

