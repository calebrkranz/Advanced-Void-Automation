# Advanced Void Automation

Build a skyblock factory in Minecraft Bedrock. Start with a tree, then connect sieves, farms, smelteries, and autocrafting machines to an MV Storage network.

**[Download AVA on CurseForge](https://www.curseforge.com/minecraft-bedrock/addons/advanced-void-automation)** · [Illustrated guide (PDF)](Advanced-Void-Automation-Complete-Guide-0.2.38.pdf) · [Crafting recipes](Crafting-Recipes.md)

## Install

1. Open the downloaded `.mcaddon` with Minecraft Bedrock.
2. Activate both **Advanced Void Automation BP** and **Advanced Void Automation RP** from the same release in your world settings.
3. Enable **Beta APIs** under Experiments. Back up your world before updating the packs.

## Player guide

These pages cover AVA **0.2.38**.

- [First Island](First-Island.md) and [Sieve Drops](Sieve-Drops.md)
- [Power and Pipes](Power-and-Pipes.md) and [MV Storage and Autocrafting](MV-Storage-and-Autocrafting.md)
- [Smeltery and Alloys](Smeltery-and-Alloys.md) and [Advanced Machines](Advanced-Machines.md)
- [Essence and Equipment](Essence-and-Equipment.md), [Void Ore Miner](Void-Ore-Miner.md), and [Flying Ships](Flying-Ships.md)
- [Nuclear and Wireless Power](Nuclear-and-Wireless-Power.md) and [Troubleshooting](Troubleshooting.md)

## Improve MV Storage

The [shared runtime](main.js) contains the MV logic along with the code for other machines. Start with the part you want to change.

| Area | Source |
| --- | --- |
| Stored counts and unique items | [Storage wrapper](main.js#L52) |
| Search, pagination, and inventory display | [Native MV runtime](main.js#L2269) and [stock refresh](main.js#L2364) |
| MV Link Pull and Transfer | [Link processing](main.js#L2816), [batch transfers](main.js#L2791), and [power debit and refunds](main.js#L2764) |
| Saving item counts | [Batch persistence](main.js#L4792) |
| Universal Crafter | [MV connection lookup](main.js#L4280) and [Crafter UI](ava_crafter.json) |
| Screen layouts and routing | [MV Storage UI](ava_mv_ui.json), [MV Link UI](ava_link_mv_link_menu.json), and [shared chest screen](chest_screen.json) |

To test a change, copy a full AVA 0.2.38 installation into a disposable test world, then apply your changes to the matching Behavior or Resource Pack paths. For example, the repository’s `main.js` goes in `BP/scripts/`, and the UI JSON files go in `RP/ui/`.

Test deposits and withdrawals, a named or enchanted item, search and pagination, and both Link modes. For performance changes, run `/scriptevent ava:timing start` with the same machines running before and after.

The add-on is listed under [GNU GPL v3 on CurseForge](https://www.curseforge.com/minecraft-bedrock/addons/advanced-void-automation/license).
