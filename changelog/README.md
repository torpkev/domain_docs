![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Update Logs

[Home](https://torpkev.github.io/domain_docs)

## 1.9.18 - Bug fix

This update addresses the deprecation of the TNTPrimed event in Paper - for versions 1.19+, Domain will use the Bukkit version of this event regardless. This deprecated (but working) event was causing warnings to appear in console

## 1.9.17 - Bug fixes and new flag

This update includes a couple of bug fixes provided to members of the Discord, as well as a new flag

Bugs squashed include (but not limited to) being able to open a protected chest by throwing an enderpearl at the same moment

### New Flag

PREVENT_GROW_ALL - This flag rolls up all the other PREVENT_GROW_* flags into a single handy flag

## 1.9.14 - New Flags, PlaceholderAPI support, Particle Visualizations, Default naming, Bug fixes

### New Flags

PREVENT_SPAWN_WARDEN - Which is pretty self explanatory - it prevents a warden being spawned in the field
ANIMAL_MAGNET
MONSTER_MAGNET

The magnet flags pull either animals or monsters towards a fixed point - This will help greatly with things like mob grinders - instead of using complex water traps, you can instead drop a magnet location to where your pit-drop or other is, or even just to gather them together to make it easier to kill them.

To use it, add either flag as needed to the field, and then right click the block with an open hand, go to Edit Field > Admin Commands > Magnet
This will give you a magnet wand, then left click the spot you want the mobs drawn to with the wand, then left click the Domain block with the wand to set.

The mobs will be drawn to that spot continually (they may try and wander off, but won't get far) - This can be especially powerful if you add the magnet flags to a Spawner block

Add the following to config.yml

    magnet_range: 5

### PlaceholderAPI Support

You can now use %domain_total_blocks% and %domain_current_field% - these will update every x number of seconds as laid out in the config

Add the following to config.yml

    papi_update_time: 10

### Particle Visualizations

You can now choose particle visualzations in the configs instead of glass blocks

Add the following to the block yml file

    visualization: PARTICLE_CUBE

### Default naming of new fields

Fields were previously named like player name's type field - they can now be set in the block config

Add the following to block yml file

    default_new_name: "<%player%>'s <%type%> field"

## OLDER

[1.9.13](https://torpkev.github.io/domain_docs/changelog/update1913) - Bug fixes

[1.9.12](https://torpkev.github.io/domain_docs/changelog/update1912) - Added Vouchers!

[1.9.11](https://torpkev.github.io/domain_docs/changelog/update1911) - Bug fixes, code cleanup, API changes

[1.9.10](https://torpkev.github.io/domain_docs/changelog/update1910) - Adds a new flag, updates behavior on PREVENT_BREAK/PREVENT_BUILD, bug fixes

[1.9.9](https://torpkev.github.io/domain_docs/changelog/update199) - Provides 1.19 support & new flag

[1.9.8](https://torpkev.github.io/domain_docs/changelog/update198) - Bug fixes

[1.9.7](https://torpkev.github.io/domain_docs/changelog/update197) - Adds a new API function for Bazaar 1.2.0

[1.9.6](https://torpkev.github.io/domain_docs/changelog/update196) - Added expand/shrink, resize, and open commands + bug fixes

[1.9.0 - 1.9.5](https://torpkev.github.io/domain_docs/changelog/update190_195) - Adds to snap to chunk, WorldGuard support, 1.17 and 1.18 compatibility, and various bug fixes

[1.8.3](https://torpkev.github.io/domain_docs/changelog/update183) - Idle kicking, kick from field, /domain me command, + bug fixes

[1.8.2](https://torpkev.github.io/domain_docs/changelog/update182) - 2 new commands for troubleshooting + bug fixes

[1.8.1](https://torpkev.github.io/domain_docs/changelog/update181) - 2 new flags + bug fixes

[1.8.0](https://torpkev.github.io/domain_docs/changelog/update180) - Major Update

