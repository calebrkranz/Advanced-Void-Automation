# Power and Pipes

A Combustion Generator generates 80 W per working second. Its 10,000 W buffer continues supplying connected machines during standby and while remaining charge lasts after fuel runs out. It resumes burning once there is room for another 80 W. If a powered machine stops while the generator is charged, check its own status and Watt Pipe connections.

## Generators, Watt Pipes and battery backup

Red Watt Pipes form the electrical network. Purple Transfer Pipes carry items/fluids. Choose a generator supported by your supplies: Combustion, Solar/Advanced Solar, lava conversion or the late Pink Slime route. Read the live HUD for power and fuel conditions.

An empty source cannot power machines using stale pipe energy. Solar depends on its active lighting/day conditions. Check source fuel, red pipe connections and workload when a machine reports no power.

Place touching Battery blocks to combine their storage. Connect the bank to sources through Watt Pipes. Multiple sources can contribute spare charging power; full banks stop charging. Charge remains through reloads.

Batteries remain standby while primary generation is active, then discharge when primary sources go down. They do not supplement an undersized but still-active primary source. Remove source fuel for a safe outage test.

The connected bank displays a centered horizontal gauge on one front face, red when low and green when high, plus numeric status. A broken battery drops empty; plan storage changes before dismantling a charged bank.

## Fluid Pumps, tanks and lava handling

Place a Fluid Pump at the supported fluid source, run purple Transfer Pipes and connect a compatible tank. Collected ordinary water over a Moisture Collector is a supported source. Capacity, fluid compatibility and locks still matter.

Adjacent compatible tanks combine displayed storage and fill bottom-up. Their shared inner divisions disappear. Add more blocks to expand the group. Use buckets for manual supported fluid insertion/extraction.

The Kiln is an early lava route. Supply its supported solid input and connected output storage, then wait for processing. A blocked/full output tank can prevent further production.

Seared Tanks supply the smeltery fuel arrangement. Do not mix different fluids into an occupied group. Molten metals can ignite entities like lava; build safe walkways rather than stepping into the molten volume.

## Transfer Nodes, filters, priorities and bulk storage

Place a Transfer Node against the source inventory and route purple Transfer Pipes to a destination. Keep intake direction unambiguous. Sneak-use rotates the intake. Start with one source chest and one destination when troubleshooting.

Use a Polymer Circuit Board on a node to enable smart routing. Open its HUD and place actual example items into persistent filter slots. Remove them manually when you want to change the filter.

ALLOW listed items transfers only matching items; BLOCK listed items excludes them. An empty filter permits all items. The button label names the active mode. Destination priority tries High, then Normal, then Overflow, skipping full or incompatible inventories.

A Black Hole Unit can accept and supply items through the transfer network. Its capacity does not remove the need for a correct source/destination route. A Vacuum Hopper collects loose drops; conveyors and Express Conveyors move physical items. Filter overflow after reserving production inputs.

Face the Mob Grinder’s blades toward the mobs. The HUD names the direction and range it checks. Base cost is 80 W per mob. Transfer Nodes can extract item drops, and separate tank groups can collect Liquid XP and Pink Essence. Full fluid buffers preserve their stored contents and skip new overflow. Full item output still stops processing.

![Battery bank and Watt Pipe build](assets/battery.png)

*Illustrated build reference.*

[Back to guide](README.md)
