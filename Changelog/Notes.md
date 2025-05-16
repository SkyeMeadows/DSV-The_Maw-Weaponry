# Calculations
ROF - Equivalent to Rounds Per Minute (RPM)
A value of 60 ROF means 1 shot per seconds or 60 shots per minute. 3600 is beam weapons as that is 60 shots per second which is the fastest the engine can go
To fire more shots than 3600 per minute, but not be a beam, Use TrajectilesPerBarrel as higher than 1, as this will create multiple projectiles/shots per firing event (ROF)\

Weapon Block Volume (InventorySize) - Dictated in Scripts/CorePart/[Named]_Weapon.cs, in kL
A value of 1f equates to 1000.0L of Volume in-game. Irritating to find, simple to change.
P.S. Any changes to blocks already placed will need to be updated by replacing said blocks.


# Bugfixes Needed


# Weapons to potentially modify further
Riptide Flak Turret - Potentially add projectile EOL effect so that it does explosion damage


# Other Notes
Bad to go under 1.0 second base crafting time for performance

# Poll:
8 options, Multiple choices allowed 1 will be accepted to be worked on

Nyx/Sabre SG Missile
B2-M Shrike Bomb Bay
M8G-LS4 Longsword Missile Battery
M98-V Crusader Focus Beam 
PL16(-C) Gravastar Laser Turret
XM-500 Medusa Phase Cannon
VL6 Modulus Variable-Laser
Other (specify in [link thread])


# Things to change/do
General:
- Need to evaluate all projectile-based weapons and make health adjustments, as some are currently untargetable.
 
Ammunition Effects:
 -Examine Volume for all LG Turret Ammo. Adjust Accordingly.


# Weapons to look at for the first time
RL6 Hydra Rocket Battery
R1-S Interceptor Rocker Pod
M8G-LS4 Longsword Missile Battery *
XM-500 Medusa Phase Cannon *
VL6 Modulus Variable-Laser *
PL16(-C) Gravastar Laser Turret *
Nucleon Laser Shotgun
M-1000 Avalanche Siege Mortar
Riptide Flak Turret
AC85 Echo Autocannon
ML-T8 Gladiator Tactical Launcher
M98-T Crusader Focus Beam Turret *
SR-75 Sentinel Smartgun
EB-10 Nova Phase Blaster
MG65-T Vulcan Gatling Cannon
Argus Orb PD Laser
B2-M Shrike Bomb Bay
PL-16-S Gravastar Pulse Laser
Nucleon Laser Shotgun (SG)
PL4-S Zarya Pulse Laser
M98-V Crusasder Focus Beam *
EB-5A Nova Phase Blaster
Sabre Missile *
Nyx Missile *

# Notes on specific Weapons
### Notes on Coilgun Balance 2-3-2025

AryxLightCoilgunAmmoWC - to break shield face
* Most Lore-accurate potential would be to increase hit-scan radius from 1 block to 2 or 3 blocks

Reduced Shield Multiplier - Should break Corvette Max Shields, but not Frigate (in average cases)
Increased Reload time from 25s to 60s - Balance
Adjusted power cost to ~1.5GW while charging. Using this weapon includes a risk. If you are a tank, your shields won't charge as fast.
Increased linear damage ~7x - Allows for targets of opportunity if you can aim well enough


### 405 Coilgun Wrap-up 2-5-2025

Aryx_AWE_Blueprints.sbc - Significant Material Cost Increase
Aryx_AWE_AmmoMagazines.sbc - Mass and Volume increase x10
AryxCoilgunHunter_Weapon.cs - InventorySize (Ammo Volume) increase x10

### Coilgun Hunter (405) 4-5-25

Reduced Mass and Volume back to original. 
Decreased Gun Inventory back to original.
Reduced Ammunition Cost back to original.
Left Ammunition damage properties, power draw, and reload alone.

# Notes on Ammunition Mass Changes:

Large Grid Large Turret Ammunition changed to follow the following formula(pseudocode):
(BattlecruiserMaxMass / 10) / (10MinSustFire * FireRate * MaxTurretCount)   #FireRate accounts for all affecting values (Heat, multiplue mags, etc.)
Large Grid Medium and Small Turrets follow the same formula * .5, and * .25, respectively.

## Changes:
### Light Weapons
M120 Whirlwind Strike Cannon        250 > 50    <SubtypeId>AWE120mmCannonMag
MG50 ATLAS Point Defence Cannon     8 > 80      <SubtypeId>ATLASAmmoMagazine
AC54 Chord Autocannon               4 > 90      <SubtypeId>54mmAmmoMagazine

### Medium Weapons
M240 Cyclone Strike Cannon          500 > 185   <SubtypeId>AWE240mmCannonMag
F4-GL Thrasher Heavy Flak Cannon    30 > 360    <SubtypeId>AWE135mmFlakMagazine
BR-RT7 Punisher Burst Cannon        100 > 1050  <SubtypeId>70mmBurstMag
AC85 Echo Autocannon                12 > 450    <SubtypeId>AWE85mmAmmoMagazine
KR115 Athena Picket Railgun Turret  400 > 1250  <SubtypeId>AryxSmallRailgunMagDef
MG-65 Vulcan Gatling Gun            8 > 80      <SubtypeId>ATLASAmmoMagazine

### Large Weapons
M480 Hurricane Strike Cannon        750 > 1000  <SubtypeId>AWE480mmCannonMag
KR250 Apollo Railgun Turret         800 > 9000  <SubtypeId>AryxRailgunMagDef
M600 Tempest Strike Cannon          1000 > 2200 <SubtypeId>AWE600mmCannonMag

### TLDR:
Large Turret Ammo's mass now reflects 10 minutes of continuous fire, assuming all turret points are spent on that turret, and that 10% of a given Battlecruiser's mass is reserved for Ammo.
Medium and Small Turrets have 1/2 and 1/4 that mass, respectively.
All Ammo Values double-checked in-game.

Note: The actual Magazine that goes into the gun is just that, the magazine. It does not affect the projectile(s) fired as that is defined seperately.

# --- Munition Categories ---
Energy
Small Caliber
Cannon
Hybrid (Railgun)
Rocket/Missile

- Have at least one weapon from each category (except maybe Rocket/Missile) that is anti-SG.

## --- Defining Anti-SG Turrets ---
Anti-Munition
- TEB101 Ancile

Anti-SG
- F4-GL Thrasher
- KR115 Athena
- M120 Whirlwind
- MG50 ATLAS
- AC54 Chord
- MG25 Rampart
- Aurora Combat Laser
- Oculus Orb

Not Anti-SG
- M240 Cyclone
- M480 Hurricane
- M600 Typhoon
- BR-RT7 Punisher
- AC85 Echo
- AL35 Spartan
- T200A1 Pulsar
- KR250 Apollo
- T400A2 Quasar
- NC7-5F Trident
- ZS-1200 Ariadne
- T600A3 Magnetar

## --- Anti-SG By Category ---
Energy:        Aurora
Small Caliber: Thrasher, ATLAS
Cannon:        Whirlwind
Hybrid:        Athena
Missile:       Flechette
