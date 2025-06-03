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