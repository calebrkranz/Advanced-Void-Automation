# Troubleshooting

## Troubleshooting and safe pack updates

Essence Table idle: craft the crystal at a normal Crafting Table first. Then insert essence + crystal, previous gear + next-tier ingots, or Supremium gear + charm. Its input grid is not a general crafting bench. It needs no Watt Pipe.

Flight stays after armor removal: 0.1.221 adds a forced active-flight reset after mayfly is revoked. Use both current packs and reload. Native engine behavior still needs checking on your client build.

No essence from a few dirt blocks: it is a chance drop, not guaranteed. The six-click flow is tested at all mesh tiers. Process more dirt and collect physical drops safely.

Machine will not break: remove contents and upgrade boards first. Step back if a hidden inventory host intercepts mining. Do not delete storage hosts to force removal.

Wrong transfers: check intake direction, active ALLOW/BLOCK mode, saved filter items, priority, MV Link direction, power, loaded storage and free destination space.

Two pack versions: an older embedded world pack can coexist with a new imported library version. Check BP and RP descriptions, then reload Minecraft. You do not have to delete the world.

Sound log: [Sound][error]-<world> | no valid version passed by the caller or found in the input. This pack ships no custom sound-definition files; audited script calls use vanilla sounds. The exact cause has not been confirmed as an addon defect, so no unrelated sound override is supplied to hide the message.

Automated checks verify definitions, recipes, simulated state transitions and conservation. They do not prove native rendering, controls or sound. Keep a world backup before major upgrades.

For a comparable performance capture, use /scriptevent ava:timing start in a test world with commands enabled. Run the same machines for each capture and compare ticks per second and average milliseconds per call. Scheduler totals include nested machine calls.

[Back to guide](README.md)
