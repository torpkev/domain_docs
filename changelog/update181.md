![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.8.1

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

## Two new flags and Bug Fixes


### New Flags

It seems I've missed a couple of fairly obvious flags for a while now

**PREVENT_ENDERMAN_AGGRESSION**

    This will prevent an enderman becoming hostile towards a player when they look at it (if player is in the field, the enderman does NOT have to be in the same field)

**PREVENT_ENDERMAN_GRIEF**

    This will cancel the event if it is an enderman is changing the state of a block (picking it up)


Make the following additions to your flags.yml file:

#### flags.yml

    PREVENT_ENDERMAN_AGGRESSION:
      name: "&bPrevent Enderman Aggression"
      lore: "&fPrevents an enderman from becoming|&fhostile when a player looks at them"
      icon_on: LIME_STAINED_GLASS_PANE
      icon_off: RED_STAINED_GLASS_PANE
      locked: false
    PREVENT_ENDERMAN_GRIEF:
      name: "&bPrevent Enderman Grief"
      lore: "&fPrevents an enderman from picking|&fup a block in the field"
      icon_on: LIME_STAINED_GLASS_PANE
      icon_off: RED_STAINED_GLASS_PANE
      locked: false
      
#### Bug Fixes

- Missing entries in flags.yml was causing an error on startup, should not display a Warning instead
- No additional flags in a Domain field would cause a "not a config section" error on startup
- Expiration checking was using not getting the time from the OfflinePlayer correctly (seems to be only an issue when using Spigot rather than Paper, but resolved)
- Custom flag.yml files were not loading materials in correctly and were reverting to lime/red stained glass
