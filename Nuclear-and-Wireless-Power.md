# Nuclear and Wireless Power

## Build the reactor

Build a hollow **3×3×3** shell. The controller goes in the **middle of the front wall**, one block above the bottom layer. The center of the middle layer must remain air.

- **C** = Reactor Casing
- **R** = Nuclear Reactor Controller, facing out of the front wall
- **K** = Cooling block, or another casing if that cooling position is unused
- **.** = Air

The top row of each diagram is the front of the reactor.

```
Bottom layer       Middle layer       Top layer
C C C              C R C              C C C
C K C              K . K              C K C
C C C              C K C              C C C
```

With every cooling position used, this takes **20 Reactor Casings, 5 cooling blocks and 1 controller**. At least one cooling block is required; replace unused K positions with casings. Cooling blocks work only at the five indicated face-center positions. Extra cooling blocks on corners or edges do not form a valid shell.

## Choose cooling materials

Use full vanilla material blocks, not ingots or individual diamonds.

| Cooling block | Points per block | Output with all five positions filled |
|---|---:|---:|
| Copper Block | 1 | 3,000 W/s; heat gradually builds |
| Iron Block | 2 | 5,000 W/s |
| Gold Block | 3 | 7,000 W/s |
| Diamond Block | 6 | 13,000 W/s |
| Netherite Block | 10 | 20,000 W/s |

Materials can be mixed. Total output is **1,000 + 400 × cooling points**, capped at **20,000 W/s**. Cooling removes **4 × points** of heat each second; producing power adds 25. At least **7 cooling points** keeps continuous operation stable. Five copper blocks are below the continuous cooling threshold.

The reactor shuts down before heat reaches 1,000. It automatically resumes when heat falls to 300 or below, provided the shell is valid and fuel is available. Pausing and standby still allow cooling. Overheating destroys installed cooling blocks. The casing and controller remain. Replace the lost cooling blocks and let heat fall to 300 or below.

## Consumable cooling and automatic replacement

Each installed cooler now has a saved life percentage. It wears only when the reactor generates energy. Generated energy is divided evenly across the installed coolers for wear accounting. Pause, standby, missing fuel, heat shutdown and an incomplete shell do not spend coolant life. This does not change a fuel rod's total energy.

| Material | Life capacity per block | Approximate continuous life with five matching coolers |
|---|---:|---:|
| Copper | 250,000 W | 6.9 generating minutes; heat shutdowns extend wall-clock time |
| Iron | 750,000 W | 12.5 minutes |
| Gold | 1,500,000 W | 17.9 minutes |
| Diamond | 5,000,000 W | 32.1 minutes |
| Netherite | 20,000,000 W | 83.3 minutes |

These are game-tick timings at 20 ticks/second with continuous power demand. Mixed coolers have different lifetimes. Replacements and pauses can extend the elapsed time.

At 0% a cooler becomes air, without dropping its block. The shell is then incomplete and generation pauses. The HUD shows **0%** for an exhausted position, **--** for unused casing positions, and the current percentage for installed coolers. **L/R** mean left/right when looking at the controller's front; Back, Top and Bottom identify the other positions. **Low** is the lowest cooler life.

Place one Activator immediately outside each cooling block, pointing inward at that block. Set **Enabled: ON**, **Click: Place/Use**, **Aim: Level**, **Sneak: OFF**, and **Redstone: Ignore**. Set **Face** to the target direction; load the desired cooling blocks in its input slots. Use only the intended replacement material in each Activator.

- Left/right/back Activators point horizontally toward the corresponding cooler.
- The top Activator points **Down**.
- The bottom Activator points **Up**. Build the reactor one block above the floor to leave room underneath.
- Activators wait while a cooler is present, then place one block into the empty position. The reactor checks the shell once per second and automatically resumes; it does not need to be broken or manually restarted. A heat trip still waits until heat is at most 300.
- Feed Activator inputs using an MV Pull Link or a Transfer Node if you want unattended replacement. Do not send those blocks into the reactor's fuel slots.
- Coolant life is saved across world reloads. Existing reactors start their first tracked coolers at full life on this update.

[Illustrated nuclear reactor build in the PDF](Advanced-Void-Automation-Complete-Guide-0.2.41.pdf)

[Illustrated coolant replacement using Activators in the PDF](Advanced-Void-Automation-Complete-Guide-0.2.41.pdf)

## Fuel and automation

- Craft a Uranium Chunk using **4 End Stone + 4 Glowstone Dust + 1 Enriched Essence**: End Stone in the corners, Glowstone on the edges, Essence in the center.
- Craft a Nuclear Fuel Rod using **4 Uranium Chunks around 1 Steel Ingot** in a cross.
- Each rod supplies exactly **1,200,000 W**, regardless of the cooling material. Better cooling increases output rate, not total energy per rod.
- A fully used rod becomes one Spent Fuel Rod. Craft it back into one Steel Ingot. Uranium is consumed.
- Put fuel in the upper row of the reactor HUD. Spent fuel appears in the lower row. Transfer Nodes and MV Links can insert rods and extract spent rods.
- The reactor stores up to **1,000,000 W**. A full energy buffer stops fuel use. Full spent-fuel output also pauses production safely.
- Connect Watt Pipes or a wireless transmitter to the controller **or any Reactor Casing in the assembled shell**. Cooling blocks are not power ports.

The controller is an expensive crafting-table recipe using Netherite Ingots, Reinforced Frames, a Factory Core, Advanced Circuits and a Precision Assembler. Reactor Casings craft four at a time from Steel Blocks, Reinforced Frames and Obsidian. All six new recipes are registered in the crafting table, MV crafting and the Universal Crafter.

## Persistent wireless power controls

Use a relay normally to open the pack's custom chest HUD. Find, pairing, pagination, mode changes and disconnecting update this screen in place. Each relay receives a random readable name on placement, such as Solar Beacon 4821. Names are saved and remain searchable. Existing custom names and connections are preserved.

1. Place the source relay against a fueled generator, battery bank, **reactor controller or Reactor Casing**, or connect it to one using Watt Pipes.
2. Open it, read its automatically assigned name in the top bar. Set it to **Use as transmitter** if it was previously a receiver.
3. Place a second relay against the machine you want to power, or connect that relay to the machine with Watt Pipes.
4. In the second relay, type the source's name in the search bar, press **Find**, and click its result. This relay becomes a receiver. No battery is required between the receiver and machine.
5. Repeat for additional receivers. They share the source's available energy. Existing custom names remain searchable.

The screen reports role, selected source and available power. Both ends must be loaded and in the same dimension. An empty/unavailable source supplies no power. Receiver blocks do not duplicate or separately store energy. The name directory is accessed on setup actions; status refreshes only for open relay screens. The registry holds up to 256 named relays, and the persistent list shows eight results per page.

For a nuclear reactor, all 20 casing positions act as logical power ports once the structure is assembled. They forward the controller's existing stored energy; they do not create extra buffers or bridge unrelated item networks. A broken port or invalid reactor stops supply. Use actual casing blocks for cable/relay contact, not a diamond cooling block.

[Back to guide](README.md)
