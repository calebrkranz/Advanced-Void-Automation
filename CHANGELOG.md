# Changelog

## 0.2.83 Beta

This cumulative changelog covers every pack version from 0.2.42 through 0.2.83, following 0.2.41.

### Void Nether and Wither Chamber

- Added a bounded spawn check for dark player-built platforms over the Nether void. Eligible platforms can spawn Wither Skeletons, Blazes, Piglins, Zombified Piglins and Magma Cubes without a fortress. The check respects difficulty, mob spawning, player distance and a nearby monster cap.
- Added the Wither Chamber, Witherproof Casing, Witherproof Glass and Chamber Ports. Validated shells accept off-center controllers and glass anywhere in the shell. Watt Pipes can feed the shell and Ports connect item automation.
- The contained Wither cycle assembles Soul Sand and skulls, shows the Wither's phases and uses harmless explosion particles and sound. A completed cycle yields one Nether Star. The guide explains how to feed and extract items.

### Upgraded chests

- Added craftable Iron, Gold, Diamond and Netherite Chests with 45, 54, 63 and 72 slots respectively. Matching double chests have 90, 108, 126 and 144 slots.
- Refined single and double placement, lid animation, black interiors, metal textures and chest-style inventory spacing. Added Transfer Node routing into and out of upgraded chests.
- Removed AVA Copper Chest from the craftable lineup. Its legacy ID is retained for existing worlds.

### Machine HUD overhaul

- Restyled machine screens with machine-specific art, clearer slot groups, more visible button states and consistent inventory spacing. MV Storage and MV Link retain their established layouts.
- Standardized red Watt Reserve gauges and added a recent-power-draw indicator so a working machine can still show activity when its reserve is empty. Refined fuel, heat and fluid gauges, including Burn Time, Liquid XP and Pink Essence.
- Added work indicators across the processors, Void Ore Miner and Star machines. Refined the Pulverizer's fill animation and added planting and harvesting feedback.

### Star Forge

- Added the Star Infuser, Star Generator, Star Fusion Replicator, Star Ingots and rechargeable equipment. Charging takes 10 seconds. Full charge lasts up to one Minecraft day of active use, and full charged armor gains Jump Boost I.
- Ore replication takes 15 seconds per job and supports Diamond and other eligible ores, gems and ore products.

### Guide

- Added illustrated chest and Wither recipes with pictured outputs, Nether platform setup, Star Forge timings and a guide to the new gauges.

## Version history since 0.2.41

### Void Nether and Wither Chamber

- **0.2.42** — Added mob spawning on eligible platforms in the void Nether.
- **0.2.43** — Expanded Nether platform support and added automated Wither Skeleton Skull drops through the Mob Grinder.
- **0.2.44** — Added the Wither Chamber and automated Nether Stars.
- **0.2.45** — Added Witherproof Glass and Chamber Ports. Routed power through the shell and items through the ports.
- **0.2.46** — Allowed off-center controllers and improved seal diagnostics with block coordinates.
- **0.2.47** — Added visible, harmless explosions during the chamber cycle.
- **0.2.48** — Switched the chamber to vanilla TNT-style explosion particles and sound.
- **0.2.49** — Used the vanilla Wither model for the contained entity and made chamber glass clearer.
- **0.2.50** — Made the contained Wither turn while hovering.
- **0.2.51** — Animated the assembly of the Wither with Soul Sand and skulls, and refined its movement.

### Star Forge

- **0.2.52** — Added Star Infuser, Star Generator, Star Fusion Replicator, Star Ingots and rechargeable armor, weapons and tools.
- **0.2.53** — Increased Star equipment strength and damage. Tuned armor effects and the Star Sword and Battleaxe.
- **0.2.54** — Updated Star Forge art, revised the ingot, and made charged equipment visually distinct.
- **0.2.55** — Integrated Star tools with their intended roles and Vein Miner.
- **0.2.56** — Added automation for feeding the Star machines and extracting finished output. Updated the guide with pictured recipe outputs and a Void Ore Miner build.
- **0.2.57** — Reduced charging to 10 seconds and extended charge to one Minecraft day of active use. Added Jump Boost I to the full charged armor set. Set replication to 15 seconds per item and expanded eligible inputs, including diamonds.

### Void Nether follow-up

- **0.2.58** — Added support for Netherrack platforms.
- **0.2.59** — Removed the material restriction so any eligible spawnable floor can work.
- **0.2.60** — Added a periodic, bounded spawn check for void platforms with solid floors, dark headroom and nearby players. Respects Peaceful, mob spawning settings and a local mob cap.

### Upgraded storage chests and Pulverizer

- **0.2.61** — Added upgraded metal chests and doubled capacity when matched pairs join.
- **0.2.62** — Repaired opening interactions and replaced chest art with classic chest-style textures.
- **0.2.63** — Refined single and double chest models and inventory interaction. Removed the AVA Copper Chest from the craftable lineup, while keeping its legacy ID.
- **0.2.64** — Fixed upgraded chest block geometry validation.
- **0.2.65** — Refined metal textures, improved inventory spacing and restored break effects.
- **0.2.66** — Switched upgraded chests to the shared inventory controls to improve item movement.
- **0.2.67** — Updated facing, added Transfer Node input and output, and gave chests black interiors.
- **0.2.68** — Locked chest models to their placed facing.
- **0.2.69** — Aligned cardinal rotations and the double-chest footprint.
- **0.2.70** — Moved chest body and closed-lid orientation onto normal block facing.
- **0.2.71** — Reworked double-chest rendering and added a dedicated Pulverizer screen.
- **0.2.72** — Restored the missing geometry asset referenced by upgraded chest blocks.
- **0.2.73** — Adjusted joining so matching chests keep their intended facing. Added the Pulverizer crushing animation.
- **0.2.74** — Fixed the double-chest front and guarded lid updates when an entity has been removed. Simplified the Pulverizer animation to a white progress fill.

### Machine HUD overhaul

- **0.2.75** — Built an industrial Pulverizer faceplate with dedicated feed, output and work areas.
- **0.2.76** — Restyled the Harvester and Planter and added red Watt Reserve meters.
- **0.2.77** — Added original machine artwork, a textured reserve gauge, and work indicators for the farm machines.
- **0.2.78** — Reworked machine titleplates, grouped readouts, and aligned inventory and upgrade outlines.
- **0.2.79** — Extended the shared machine style and shortened repeated information. Kept artwork in the machine panel and kept the established MV Storage and Link layouts.
- **0.2.80** — Extended illustrated machine panels and live Watt Reserve gauges across powered HUDs.
- **0.2.81** — Refined machine console art and separate gauges for fuel, heat, and stored fluids such as Liquid XP and Pink Essence.
- **0.2.82** — Aligned portrait docks, spaced status and inventory sections, and refined button states.
- **0.2.83** — Standardized Watt Reserve display and added a green recent-draw indicator. Added live progress to Dehydrator, Glacial Chiller, Pressure Reactor, Precision Assembler, Material Infuser, Factory Core, Essence Tinkering Table, Star Infuser, Star Fusion Replicator and Void Ore Miner. Improved Harvester progress and header spacing.

## 0.2.41 Beta

- The illustrated guide shows a pictured output and quantity beside each crafting grid.
- The Automated Sprinkler has a new 16×16 steel, cyan, and brass texture. The guide uses the new art.
- The beginner walkthrough covers water, lava, renewable Cobblestone, power, the smeltery, and MV Storage.

[Read the 0.2.41 guide](Advanced-Void-Automation-Complete-Guide-0.2.41.pdf)
