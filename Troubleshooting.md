# Troubleshooting

## Troubleshooting and safe pack updates

Essence Table idle: craft the crystal at a normal Crafting Table first. Then insert essence + crystal, previous gear + next-tier ingots, or Supremium gear + charm. Its input grid is not a general crafting bench. It needs no Watt Pipe.

**Flight persists after removing Supremium armor.** Verify that the world is using matching Behavior and Resource Pack versions and reload. Include the Bedrock version when reporting a persistent issue.

No essence from a few dirt blocks: it is a chance drop, not guaranteed. The six-click flow is tested at all mesh tiers. Process more dirt and collect physical drops safely.

**Moving a machine.** Eligible machines with stored items drop a Packed Machine when mined. Place it to restore the contents. MV Links, Composters, and barrels are excluded. Leave hidden storage hosts intact.

Wrong transfers: check intake direction, active ALLOW/BLOCK mode, saved filter items, priority, MV Link direction, power, loaded storage and free destination space.

Two pack versions: an older embedded world pack can coexist with a new imported library version. Check BP and RP descriptions, then reload Minecraft. You do not have to delete the world.

Sound log: [Sound][error]-<world> | no valid version passed by the caller or found in the input. This pack ships no custom sound-definition files; audited script calls use vanilla sounds. The exact cause has not been confirmed as an addon defect, so no unrelated sound override is supplied to hide the message.

For a comparable performance capture, use /scriptevent ava:timing start in a test world with commands enabled. Run the same machines for each capture and compare ticks per second and average milliseconds per call. Scheduler totals include nested machine calls.

[Back to guide](README.md)
