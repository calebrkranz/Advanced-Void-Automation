# Void Ore Miner

[Illustrated Void Ore Miner build in the PDF](Advanced-Void-Automation-Complete-Guide-0.2.41.pdf)

Build this late-game machine over the edge of your island. It produces unfinished metals; seeds, essence and other sieve-progression drops remain exclusive to existing systems.



## Structure

All nine blocks are on the same horizontal layer. Place seven Mining Frames, one controller in the middle of any side, and one Laser Head in the center.

```text
F F F
F L F
F C F

F = Void Mining Frame
L = Void Laser Head
C = Void Ore Miner controller
```

Leave the complete vertical shaft below L empty down to the bottom of the Overworld. Fluids and passable blocks also obstruct the laser. Do not place the platform directly on your island floor. Connect Watt pipes to C. Connect a transfer node or an MV Transfer link to export its output to storage. The native MV link must have its normal MV power and routing requirements satisfied.

## Recipes

Recipes are shapeless at a crafting table and are also registered with the Universal Crafter/MV crafting system.

| Item | Ingredients | Output |
|---|---|---|
| Mining Frames | 2 Steel Ingots + 4 Seared Bricks + 1 Reinforced Frame | 4 |
| Laser Head | 2 Crystalline Alloy + 2 Diamonds + 1 Conductive Core + 4 Glass | 1 |
| Controller | 4 Reinforced Frames + 2 Advanced Circuits + 1 Conductive Core + 1 Diamond + 1 Laser Head | 1 |
| Iron Focus Lens | 4 Glass + 4 Iron Ingots + 1 Light Gray Dye | 1 |
| Copper Focus Lens | 4 Glass + 4 Copper Ingots + 1 Orange Dye | 1 |
| Gold Focus Lens | 4 Glass + 4 Gold Ingots + 1 Yellow Dye | 1 |
| Alloy Focus Lens | 4 Glass + 4 Steel Ingots + 1 Purple Dye | 1 |

The laser head consumed in the controller recipe is separate from the center head placed in the structure. Craft two heads in total. Two batches of frames give eight frames, of which seven are placed.

## Operation and HUD

Use the controller normally to open its dedicated HUD. The left slot holds one optional focusing-lens type; stacked lenses do not multiply production and lenses are not consumed. Output appears in the 27 slots on the right. Pause/Resume controls production; Rescan Structure checks construction and shaft immediately; Collect Output transfers output into your available inventory space.

Each batch produces four pieces of one raw/crushed metal after two powered seconds at 400 W per working second: 800 W per batch (200 W per piece). There are no upgrade slots in this initial version. No power, missing structure, blocked shaft, invalid lens or full output stops production and the beam. Progress is retained and resumes when the condition is fixed. Power is drawn only when a mining second advances. A single visual entity creates a moving cyan-violet, beacon-style beam pointing downward. It produces no items, damages no blocks and does not keep chunks loaded.

## Unfocused output chances per completed cycle

| Output | Chance |
|---|---:|
| Raw Iron | 35% |
| Raw Copper | 25% |
| Raw Gold | 12% |
| Crushed Tin | 7% |
| Crushed Silver | 6% |
| Crushed Lead | 5% |
| Crushed Nickel | 5% |
| Crushed Aluminum | 4% |
| Crushed Platinum | 1% |

Exactly four pieces of the selected metal per completed cycle. Focus lenses multiply the matching output weights by four before normalization. Iron/Copper/Gold lenses favor their matching raw metal. Alloy Focus Lens favors all six custom crushed metals. Focusing does not guarantee an output or increase the total number of results. Process the ores using the pack's existing recipes and machines; the miner does not output finished ingots.

## Performance and validation

Only C ticks; F and L have no ticking component. Structure and downward-ray checks are cached for five seconds, invalidated by normal network/layout changes, and can be forced with Rescan. The beam animates on the client, uses no per-tick particle stream, and expires within three seconds unless renewed. Existing HUD files are preserved, with only a new title selector and new UI definition added.

Automated checks cover power use, structure/shaft validation, lens preservation, full output, pause/resume, no-power recovery, final output-write rollback, and the existing MV/node/crafter regressions. The actual in-game appearance and interaction have not been live-tested in this release.

## Art

Block faces are 16x16 PNGs derived from a built-in image-generation atlas; generated source and prompt are retained in work/art-229. The beam and lens sprites are 16x16. The design uses charcoal iron framing, purple conduits and cyan lighting.

## Placing extraction nodes

Hold a Transfer Node, sneak, then right-click the controller face where it should attach. The node intake points toward the controller automatically. Normal right-click opens the HUD. Search for Focus Lens to find the four optional lenses; place one in the left-hand lens slot.

[Back to guide](README.md)
