![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.8.1

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

Minor bug fixes, plus a new flag

- Missing entries in flags.yml was causing an error on startup
- No additional flags in a Domain field would cause a "not a config section" error on startup
- Expiration checking was using not getting the time from the OfflinePlayer correctly (seems to be only an issue when using Spigot rather than Paper, but resolved)
- Custom flag.yml files were not loading materials in correctly and were reverting to lime/red stained glass

### New Flag!

It seems I've missed a fairly obvious flag for a while now

**PREVENT_ENDERMAN_GRIEF**

This will cancel the event if it is an enderman changing the state of a block.

Make the following addition to your flags.yml file:

#### flags.yml

    PREVENT_ENDERMAN_GRIEF:
      name: "&bPrevent Enderman Grief"
      lore: "&fPrevents an enderman from picking|&fup a block in the field"
      icon_on: LIME_STAINED_GLASS_PANE
      icon_off: RED_STAINED_GLASS_PANE
      locked: false
      
