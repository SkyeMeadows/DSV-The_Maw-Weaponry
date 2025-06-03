# Calculations
ROF - Equivalent to Rounds Per Minute (RPM)
A value of 60 ROF means 1 shot per second or 60 shots per minute. 3600 is beam weapons as that is 60 shots per second which is the fastest the engine can go
To fire more shots than 3600 per minute, but not be a beam, Use TrajectilesPerBarrel as higher than 1, as this will create multiple projectiles/shots per firing event (ROF)\

Weapon Block Volume (InventorySize) - Dictated in Scripts/CorePart/[Named]_Weapon.cs, in kL
A value of 1f equates to 1000.0L of Volume in-game. Irritating to find, simple to change.
P.S. Any changes to blocks already placed will need to be updated by replacing said blocks.


# Bugfixes Needed


# Weapons to potentially modify further
M600 Tempest Turret - Certainly needs damage buff to be a capital weapon
M480 Hurricane Turret - Probably needs damage buff to be a Heavy weapon
Sunderer Heavy Lance - Needs a damage buff against shields to be an anti-shield version of the ares

# Other Notes
Bad to go under 1.0 second base crafting time for performance

# Things to change/do
General:
- Need to evaluate all projectile-based weapons and make health adjustments, as some are currently untargetable.
 
Ammunition Effects:
 -Examine Volume for all LG Turret Ammo. Adjust Accordingly.

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
