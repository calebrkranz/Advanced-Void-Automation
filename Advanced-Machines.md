# Advanced Machines

Put **16 crops or saplings** and **1 charcoal** in a Pressure Reactor. Add **1,000 mB of water** using a water bucket or a connected water tank. Supply **400 W per working second** through Watt Pipes. At base speed it takes **8 seconds** and yields **4 Polymer**. Wheat, carrots, potatoes, beetroot, sugar cane, melon slices, pumpkins, cactus and supported saplings can be mixed.

[Pressure Reactor production cell in the PDF](Advanced-Void-Automation-Complete-Guide-0.2.41.pdf)

## Planters, harvesters, sprinklers and Activators

Provide a Planter with seeds/saplings, suitable soil, free space and power. Place the powered Harvester so its area covers mature crops/trees. Export its internal output with a transfer node. Tree harvesting has built-in crook behavior.

The Automated Sprinkler uses water and Watt power to speed nearby crop growth. Supply water by bucket or from a connected compatible water source. Use the Harvester to collect mature crops.

See the crop-build illustration and the new sprinkler texture in the [0.2.41 illustrated guide](Advanced-Void-Automation-Complete-Guide-0.2.41.pdf).

Configure an Activator deliberately: face, aim, use/break click, sneaking, redstone and order. Tool durability is spent on the first usable tool one at a time, not randomly spread across tools.

Ore crops have four harvest tiers. Inferium crops have five and always grow Inferium, with larger per-harvest yields. Check power and output capacity before adding speed boards.

## Advanced assembly, infusion and the Factory Core

Precision Assembler makes the listed Reinforced Frames, Advanced Circuits, Conductive Cores, Growth Essence and modifiers. Supply ingredients and Watts; the first complete matching recipe is processed.

Material Infuser needs solid ingredients plus water and power for Crystalline Alloy or Enriched Essence. Its fluid supply and returned containers are part of your production line.

Factory Core uses late components and substantial power for its listed high-throughput recipes. Build crop/Charcoal production, Polymer, circuits, assembly components and infusion materials in stages before scaling the core.

Keep buffers between stages. Use High-priority input destinations before bulk overflow. A blocked output or missing machine-made component can stop a large factory even when most materials are abundant.

## Production recipes

Base values from the pack. Keep machine output space free.

| Machine | Output | Input per batch | Water | Time | Power per working second |
|---|---|---|---:|---:|---:|
| Pressure Reactor | 4 × Polymer | 16 × Crops or saplings, 1 × Charcoal | 1000 mB | 8 s | 400 W |
| Precision Assembler | 1 × Reinforced Frame | 4 × Steel Ingot, 2 × Polymer, 1 × Bronze Ingot | 0 mB | 8 s | 250 W |
| Precision Assembler | 2 × Advanced Circuit | 2 × Circuit Board, 2 × Electrum Ingot, 1 × Quartz, 2 × Polymer | 0 mB | 10 s | 500 W |
| Precision Assembler | 1 × Conductive Core | 2 × Platinum Ingot, 2 × Invar Ingot, 1 × Redstone Block, 1 × Advanced Circuit | 0 mB | 15 s | 1000 W |
| Precision Assembler | 4 × Growth Essence | 16 × Wheat, 4 × Bone Meal, 1 × Polymer | 0 mB | 6 s | 250 W |
| Material Infuser | 2 × Crystalline Alloy | 2 × Diamond, 4 × Steel Ingot, 2 × Nickel Ingot, 1 × Polymer | 1000 mB | 15 s | 1000 W |
| Material Infuser | 4 × Enriched Essence | 8 × Growth Essence, 4 × Amethyst Shard, 1 × Advanced Circuit | 1000 mB | 12 s | 750 W |
| Precision Assembler | 1 × Reinforcement Plate | 1 × Reinforced Frame, 2 × Crystalline Alloy | 0 mB | 10 s | 750 W |
| Precision Assembler | 1 × Efficiency Module | 2 × Advanced Circuit, 1 × Crystalline Alloy, 8 × Redstone | 0 mB | 10 s | 750 W |
| Precision Assembler | 1 × Fortune Module | 2 × Advanced Circuit, 2 × Crystalline Alloy, 16 × Lapis Lazuli, 2 × Diamond | 0 mB | 15 s | 1000 W |
| Factory Core | 1 × Factory Trophy | 8 × Crystalline Alloy, 4 × Conductive Core, 4 × Advanced Circuit, 8 × Polymer, 4 × Platinum Ingot, 4 × Pink Slime, 4 × Enriched Essence, 1 × Netherite Ingot | 8000 mB | 60 s | 2000 W |

[Back to guide](README.md)
