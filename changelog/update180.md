![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.8.0

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

This is a massive update for Domain - roughly 70% of the code has been rewritten from scratch, including the core DomainBlock classes, visualization, reading/writing from the yml files, and removal of a lot of duplicated code and classes.

Due to the extent of the change, please note the following:
BACKUP YOUR DOMAIN FOLDER AND JAR FILE NOW

If you have any issues with 1.8.0 please revert back to your backup.  I may not be able to support issues caused by upgrading if there is not a backup available.

Now that is out the way.. on to the changes.

There is a whole new set of documentation: [https://torpkev.github.io/domain_docs](https://torpkev.github.io/domain_docs) please review this before upgrading to 1.8.0

Massive amounts of back-end changes and bug fixes.  You should see an increase in performance and things should generally run a lot nicer

Commands have been rewritten and some have been removed, refer to documentation.  In particular, /domain locate has been removed and is replaced with an expanded /domain search as it was already doing the same work.

Some 'staff' commands will not work and will not show in tab completions unless you are in domain bypass mode

Renting was rewritten from the ground up.  You can read more about the renting process here but the long and short of it is that any field with the config set to cost and days > 0 are rentable, there is a new gui in the menu where players can set the rent cost/days.  Rent signs no longer need any interaction and will self-populate.  Rented fields have their own name, welcome/farewell message and allowed lists.  When the rent period is up, these get removed and it reverts the name/messages/allowed list back to what it was before renting.

Spawner Fields! - These are special types of Domain fields that can be used to spawn mobs, much like using a Mob spawner.  You can read all about Spawner fields here - but they're really cool and have some great advantages over using a spawner block

Members Only fields have been created, this is not documented or easily accessible in game, but, you can create a field where only those with a particular permission can enter.  To apply, simply add:

    members_only_perm: YOUR_PERMISSION_HERE
    
It works like a PREVENT_ACCESS_TO_NONALLOWED but is permission based.

When converting a field to an Admin Block, then owner field is now removed completely.  You can now also convert an admin block back to a player block

Support Changes

It is worth mentioning changes to the support system.
Due to a number of charge-backs and paypal disputes, I've had the Discord modified to only show the #domain channel for registered buyers.  Everyone can still talk in #general and can request help there, but will need to present their spigot username in order to receive any help from the development team.  Trial copies are still available and will be supported as previously.

Changes to Domain files

Add or modify the following entries to the respective files:

#### lang.yml

    admin_delete_block_success: "&aSUCCESS &f- Field has been &4removed"
    admin_disable_block_success: "&aSUCCESS &f- Field has been &4disabled"
    allow_player_alert_added: "&cYou have been given access to the <%name%> field by <%player%>"
    break_item_frame: "&cYou cannot break that here"
    clan_add_already_in: "&cUnable to add <%clan%> to this field, as it is already allowed"
    clan_remove_not_in: "&cUnable to remove <%clan%> from this field, it is not currently allowed"
    command_adminblock_back_success: "&2SUCCESS - Block has been converted from an Admin block"
    disallow_player_alert_removed: "&cYou have been removed from access to the <%name%> field by <%player%>"
    disallow_player_not_found: "&4Unable to disallow player.  Player not found"
    disallow_player_not_found1: "&4Player disallow cancelled.  You are now returned to chat."
    find_title: "<%player%> Owned Fields"
    gui_rent_title: "Rent"
    members_only: "&cSorry, this area is for members only"
    merge_error: "&4Unexpected error - Unable to merge field"
    remove_player_fail_not_allowed: "Unable to remove player, they are not allowed to the field"
    remove_wand: "&cWand not in use, removing it from inventory"
    rent_confirm: "Are you sure you want to rent this field? It costs &b$<%cost%> &rfor &b<%days%>&r days"
    rent_confirm_info: "&4Clicking YES will rent the field and debit your funds"
    rent_confirm_yes: " &f[&2YES - Rent the field&f]"
    rent_info_available: "Not currently rented out"
    rent_info_cost: "Cost $<%cost%> for <%days%> days"
    rent_info_na: "&4Field is not currently set as rentable"
    rent_info_rented: "Currently rented to <%renter%> until <%expires%>"
    rent_info_title: "\n&b************************************************\n&fRent Info\n&b************************************************"
    rent_na: "&4N/A"
    rent_own: "&4You cannot rent your own field"
    rent_set_cost: "Rent for this <%blocktype%> field has been set to $<%cost%>"
    rent_set_cost_info: "&eEnter the new rent cost in the chat.  It must be a valid number and will not be visible to other players.  Right click the Domain Block to cancel"
    rent_set_cost_zero: "This <%blocktype%> field is no longer available to rent.  Set the cost to at least $1 to make available"
    rent_set_days: "Number of days in the rent period for this <%blocktype%> field has been set to <%days%>"
    rent_set_days_info: "&eEnter the new rent days in the chat.  It must be a valid number and will not be visible to other players.  Right click the Domain Block to cancel"
    rent_set_days_zero: "This <%blocktype%> field is no longer available to rent.  Set the number of days in the rent period to at least 1 to make available"
    rent_unexpected_error: "Unable to rent field - Unexpected Error, please contact a member of staff"
    resize_wand_lore: "&f&lInstructions|&fLeft click corner 1 of desired field|&fRight click corner 2 of desired field|&fRight click domain block with wand to save"
    resize_wand_name: "&bDomain Resize Wand"
    search_hover_text: "Owner: <%owner%>\nType: <%blocktype%>\nLocation: <%location%>"
    sign_cost: "&lCost: &b&l$<%cost%>"
    sign_days: "&lDays: &b&l<%days%>"
    sign_rent: "&0&l[&d&lRent&0&l]"
    sign_rented: "&0&l[&b&lRented&0&l]"
    teleport_set_cancel: "&4Teleport location setting has been cancelled"
    teleport_set_notset: "&4Teleport location has not been set.  To cancel, right click the Domain Block with an open hand"
    teleport_set_ok: "&4Teleport location set.  Left click the Domain Block with the wand to save"
    teleport_set_unsafe: "&4Unable to set this location, it is unsafe for teleporting to"
    teleport_unsafe: "&4Unable to teleport.  Location is unsafe"
    teleport_wand_lore: "&f&lInstructions|&fLeft click the location you wish to teleport to|&fthen left click the Domain Block to save|&fRight click the Domain Block with an empty hand to cancel"
    teleport_wand_name: "&bDomain Teleport Wand"
    usage_allow: "Usage: /domain allow &b<player name>&r"
    usage_clan: "Usage: /domain clan &ballow&f|&bdisallow &6<clan tag>"
    usage_disallow: "Usage: /domain disallow &b<player name>&r"
    usage_display: "Usage: /domain display &bclear&f|&bcorners&f|&bcube&f|&bring"
    usage_get: "Usage: /domain get &6<block type>"
    usage_give: "/domain give &6<player name> &6<block name>"
    usage_search: "Usage: /domain search &bowner&f|&btype&f|&bworld &6<search term>&r"
    version: "<%name%> - Version <%ver%>"

#### gui.yml

    adminblock_set:
      material: PLAYER_HEAD
      name: "&4Admin Block"
      lore: "&fConvert back to a player block"
      enabled: true
    flag_add:
      material: LIME_CONCRETE
      name: "&aAdd Flag"
      lore: "&fAdds a new flag to the field"
    rent_info:
      material: BOOK
      name: "&bRent Info"
      lore: "&fDisplays rent information for this field"
    rent_cost:
      material: GOLD_INGOT
      name: "&bRent Cost"
      lore: "&fSets the rent cost"
    rent_days:
      material: CLOCK
      name: "&bRent Days"
      lore: "&fSets the rent days"

#### flags.yml

    SPAWN:
      name: "&dMob Spawning"
      lore: "&fEnables mob spawning in the field"
      icon_on: SPAWNER
      icon_off: BARRIER
      locked: false
    MEMBERS_ONLY:
      name: "&bMembers Only Area"
      lore: "&fPrevents access to players without a set permission"
      icon_on: LIME_STAINED_GLASS_PANE
      icon_off: RED_STAINED_GLASS_PANE
      locked: false
    PREVENT_BREAK_PAINTING_BY_NONALLOWED:
      name: "&bPrevent Break Painting"
      lore: "&fPrevents paintings being broken by Non-Allowed players"
      icon_on: LIME_STAINED_GLASS_PANE
      icon_off: RED_STAINED_GLASS_PANE
      locked: false
    PREVENT_BREAK_ITEM_FRAME_BY_NONALLOWED:
      name: "&bPrevent Break Item Frame"
      lore: "&fPrevents item frames being broken by Non-Allowed players"
      icon_on: LIME_STAINED_GLASS_PANE
      icon_off: RED_STAINED_GLASS_PANE
      locked: false
