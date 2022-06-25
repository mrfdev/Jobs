
## How do I stop registering furnaces?

Short answer: I do not know. Maybe you can set the permission to 0

Try it and find out.

Update:

If you keep getting "payment for this furnace has been disabled", you have to a- make sure your Jobs and CMILib jar files are the latest version. And b- Its already shows this message only once for each registered block when payment from it gets disabled
There was an isues with older version which flooded chat with this message, but it should no longer do that, unless you keep interacting with furnaces which have connected hoppers which keep transporting items into those, and you keep reloging.

From the last few changelogs:

Limiting message informing you about disabled payment from specific block you own to only once every relog, so no more spam if you have furnace with hopper connected and you keep opening its UI to take out items.

Fix where player could loose block ownership if you have PreventHopperFillUps or PreventBrewingStandFillUps enabled. Now player will receive message that specific block and specific location got disabled instead. This will remain in disabled state until player interacts with that block which will inform about reenabled block or server restart. While block is in disabled state, payments for smelting or potion crafting wont be given out. Additionally /jobs ownedblocks will indicate which blocks are disabled, if any, with additional information why if you hover over it, just to minimize confusion from players who tries to figure out why payments are not coming in when those should.

Update 5.1.0.0:

Added option to disable information messages about disabled payments from owned blocks entirely, in case you dont want to bother showing those messages to the players. You can always double check if block is active and paying money to you by using /jobs ownedblocks