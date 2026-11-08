# Flying Ships

Adapted from the MHAFY ship system in Emerald Deals. Build a ship out of supported vanilla hull blocks, then turn it into a flying ship at its Helm. No Watt network or Education flight is required for ships.

## Small starter ship

1. Build a 3 × 3 Oak Plank deck. Put a Ship Helm on its center.
2. Put one Ship Balloon on the deck beside the Helm. One Balloon supports up to 32 total ship blocks, including balloons. Add more as the ship grows.
3. Optionally add a Passenger Seat and a **single** Chest or Barrel on the deck.
4. Keep the ship separated from your island. If it touches a pier, place **Ship Dock** blocks at the contact points so the scan stops there. A continuous wood floor can otherwise become part of the scan.
5. Use the Helm, let the first scan finish, then choose **Captain (Launch)**.

Example top-down layout (each symbol is one deck position):

```
P P P
B H C
P S P
```

There is a 3 × 3 plank floor beneath these positions. B = Balloon, H = Helm, C = optional single Chest, S = optional Passenger Seat, P = clear deck space.

## Controls

- Move using your normal movement controls. The hull turns toward your view. Look up/down while moving forward to climb/descend. Release movement to hover.
- Jump opens the Helm menu while piloting. Camera settings offer player view or an optional chase view.
- Sneak/dismount or choose **Dock Ship** to place the ship back into real blocks. Leave enough empty space; obstructed docking keeps the saved ship and cargo. If no pilot remains, idle recovery attempts a clear docking position.
- After changing the hull, use **Ship Settings → Rescan Ship** before launching. One Helm per connected ship.
- Craft Ship Helm I, II or III for 1×, 1.5× or 1.75× horizontal speed. Each higher tier uses the previous Helm as an ingredient.

## Passengers and cargo

Passenger Seats work on the docked ship and travel with it. Up to 16 seats are supported. Single Chests and vanilla Barrels retain exact item stacks, including names and lore. Cargo containers are unavailable during flight and become accessible again after docking. Split double chests before launch.

**AVA machines, MV Storage, links, pipes, tanks, reactors and their inventories stay anchored to the island.** An attached AVA block rejects launch rather than moving its position-based saved data. Use Ship Dock blocks to separate the ship from these builds. ED workers, warp cores and blueprint/Falcon tools are not included in this port.

## Rope ladders and cannons

Use a Rope Ladder to deploy/retract it. Retract it before launch or docking. Climbing uses movement/jump; sneak holds position. Deployed ladder supports are system blocks, not separate craftable equipment.

Ship Cannons use one **Cannonball** from the firing player's inventory per shot. Use to fire; sneak-use aims. Cannon impacts can damage blocks, matching the Emerald Deals ship system.

## Limits and performance

Up to 4,096 connected blocks, a maximum 48-block span per axis and a 65,536-cell bounding volume. Up to 160 hull fragments and 256 special visual blocks. Large ships cost more to render: start small. Scanning and assembly are staged; idle ship code performs no repeated global entity scans or player ray tracing. Only loaded ships simulate.

[Back to guide](README.md)
