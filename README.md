# Advanced Void Automation MV contributor source

This is the MV Storage source from AVA 0.2.38 for Minecraft Bedrock. The complete shared runtime is included so contributors can trace calls into item routing, power and autocrafting.

## Where to start

- [Storage and item handling](BP/scripts/main.js#L52) covers count-backed storage and the separate handling of unique item stacks.
- [Native MV runtime](BP/scripts/main.js#L2269) and [HUD refresh](BP/scripts/main.js#L2364) cover opening storage, search, pagination and interaction.
- [MV Link Pull and Transfer](BP/scripts/main.js#L2816) uses [batch transfer](BP/scripts/main.js#L2791) and [power debit and refund](BP/scripts/main.js#L2764).
- [Batch persistence](BP/scripts/main.js#L4792) commits queued storage changes and works with the recovery journal.
- [Universal Crafter connection lookup](BP/scripts/main.js#L4280) is a starting point for recipe automation.
- [Resource Pack UI](RP/ui) holds the screen definitions. The shared chest screen routes native inventories to the custom layouts. [Behavior Pack entities](BP/entities) define the inventory hosts.

## Test a change

1. Start with a full copy of AVA 0.2.38. Overlay only the changed files at their matching paths in the Behavior and Resource Packs. This source bundle depends on the full add-on for textures, shared screens, and modules imported by the runtime.
2. Open a disposable Bedrock test world with both packs and Beta APIs enabled. Back up the test world before testing saved-storage changes.
3. Test ordinary bulk deposits and withdrawals, an enchanted or named item, a search and page change, both MV Link modes, and reopening the world. For Link changes, also test a full destination and loss and restoration of power.
4. For a performance change, run the same setup before and after. Use /scriptevent ava:timing start and report the Link call count, average time per call, and maximum call time.

The add-on is listed under [GNU GPL v3 on CurseForge](https://www.curseforge.com/minecraft-bedrock/addons/advanced-void-automation/license).
