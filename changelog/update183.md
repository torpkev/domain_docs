![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.8.3

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

## Idle Kicking, Kicking non-allowed from field, New Commands, Bug Fixes

### New Commands

#### List own fields

    /domain me
    
This command will display a list of all the Domain fields that you own.
If allow_self_teleport_to_field is set to true in the config, a teleport option will be available
Requires the domain.field permission

#### Back after idling

    /domain back

This command can only be called if a player has been kicked from a field for idling, only if they haven't moved (within a few blocks) since being kicked, only if they have the domain.idle.back permission

### Bug Fixes

- File generation errors on startup have been removed ('Unable to create flags.yml as it already exists' etc.)
- When a block has the same base type and name, it will no longer default to the wrong block, instead it will use the NBT tag to determine type
- Null error when players break blocks in an admin block area has been corrected
- Other not player facing fixes

### Permission Changes

    domain.idle.back
    
Required if you want the player to be able to use /domain back

### Config File changes

Add the following to config.yml

    # If true, when a player runs /domain me - they'll have an option to teleport to the field
    allow_self_teleport_to_field: false
    
    # If true, field kicks will always send the player to spawn
    field_kick_direct_to_spawn: false
    
    # Number of minutes between a new field being placed and the idle kick / kick command being accessible
    new_field_kick_cooldown: 10
    
    # Number of seconds between checking if someone is idle.  Set to 0 to disable completely
    idle_cycle_seconds: 20
    
    # Number of times the idle timer runs before considering someone idle
    # If idle_cycle_seconds = 20 and idle_cycles_before_kick = 6, then 20 * 6 = 120 seconds
    # So if someone does not change their location in 120 seconds, they are considered idle
    idle_cycles_before_kick: 6

### Block Config Changes (Optional - defaults to false)

Add the following to your block configurations if you wish to allow the Who is in Field button to kick players

    # Set allow_who_in_kick to true if you want to allow players to kick non-allowed players from their field
    allow_who_in_kick: true

### Update Flags File

Add the following to flags.yml

      KICK_OUT_IDLE_NONALLOWED:
        name: "&bKick idle players out"
        lore: "&fKicks out players who are not allowed|&fin the field if they idle for too long"
        icon_on: LIME_STAINED_GLASS_PANE
        icon_off: RED_STAINED_GLASS_PANE
        locked: false

### Update Language File

Add the following to lang.yml

    help_user: "&lDomain Help\n&5/domain allow &b<player name>&r - Allows a player into the current field\n&5/domain buy&r - Allows you to buy a Domain block\n&5/domain disallow &b<player name>&r - Disallows a player from the current field\n&5/domain display &bclear&f|&bcorners&f|&bcube&f|&bring&r - Displays the current field\n&5/domain get &6<block type>&r - Allows you to get a Domain Block\n&5/domain list&r - Lists all the fields at your current location\n&5/domain search &bowner&f|&btype&f|&bworld &6<search term>&r - Searches for Domain Blocks\n&5/domain url&r - Displays the URL for the help pages for Domain"
    help_admin: "&lAdmin Commands\n&d/domain bypass&r - Toggles bypass mode\n&d/domain debug&r - Toggles debug mode &4[use with caution]\n&d/domain give &6<player name> &6<block name>&r - Gives a Domain block to the player\n&d/domain purge &4- Purges old Domain Blocks [USE WITH EXTREME CAUTION!]&r\n&d/domain purge_list&r - Lists the Domain Blocks that can be purged\n&d/domain reload&r - Reloads the config\ndomain version&r - Displays the current version"
    command_me_no_results: "&4No Domain fields found"
    command_me_header: "&5Your Domain Fields"
    command_back_success: "&2You have been returned to your prior location"
    command_back_disabled: "&4Idle kick is disabled, so the Back command cannot be used"
    command_back_no_prior: "&4No prior idle location found"
    command_back_not_safe: "&4Unable to return to prior idle location as it is not a safe place to teleport to"
    command_back_too_far: "&4Unable to return to prior idle location, you have moved too far from where you were kicked to"
    idle_kick: "&4You have been kicked out of the Domain field for idling"
    idle_kick_warning: "&4You have been idle in this Domain field for too long and will be kicked out of it shortly.  To avoid this, move away from your current location"
    who_in: "<%color%><%player%>"
    who_in_hover: "&fClick here to kick the player out of the field"
    who_in_title: "&lPlayers in Field: "
