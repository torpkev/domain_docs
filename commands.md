# Commands

[Home](https://torpkev.github.io/domain_docs)

---

## Bypass Mode

Domain Bypass is a way for staff to interact with a players field as though they are the owner.  While in bypass mode, the restrictions placed on a player by Domain are ignored.
Running the command will toggle the status, while active, a bossbar will appear at the top of the screen.
*Requires domain.bypass or domain.admin*

    /domain bypass

## Debug Mode

Enabling debug mode should ONLY be done when troubleshooting an issue, and while it is enabled, output will be pushed to the console, resulting in potentially large log files.
Running the command will toggle the status.

    /domain debug

## Reloading the Configuration

Reloads the configuration and data files. It is intended mostly for troubleshooting purposes and is not recommended for while the server is live
*Requires domain.admin or run from console*

    /domain reload

## Display the Domain URL

Displays a link to this page

    /domain url

## Version

    /domain version

## Visualization

You can display your own fields by standing within them and running the display command.  

### Default display

This will display with the default visualization type**

    /domain display

### Clear

Clears any existing visualization

    /domain display clear

### Corner visualization

Will display only the corners of the field, intended for large fields

    /domain display corners

### Cube visualization

This will display a hollow cube of the field

    /domain display cube

### Ring Visualization

This will display a ring at player height around the field, intended for large fields

    /domain display ring

## Adding/Removing Players/Clans from the field.

Only the owner or current renter can run this command, and they must be standing in the field they want to add permission to.
Player being added must be online, or have played on the server before.
***Myriad Clans is the only clan plugin supported by Domain***

### Allow Player
    /domain allow <player name>

### Disallow Player
    /domain disallow <player name>

### Allow Clan
    /domain clan allow <clan tag>

### Disallow Clan
    /domain clan disallow <clan tag>

## Listing and Searching for fields

You can find the current fields you're in by running the list command.  It will display any field you are currently owner or renter of at your current location

    /domain list

As a staff member, you can use the search command to find fields 
Run from console, the results will be displayed, but cannot be interacted with.
Run in-game requires Domain bypass mode or domain.admin permission and will return 4 options, and results will be paged
- **Open** - Opens the Domain block - This can be accessed with domain bypass mode or domain.admin permission
- **TP** - Teleports you to the Domain block - This can be accessed with domain bypass mode or domain.admin permission
- **Disable** - Disables the field - This requires domain.admin permission
- **Delete** - Deletes the field and removes the block - This requires domain.admin permission

You can search on 3 different criteria:

### By owner

    /domain search owner <player name>

### By type

    /domain search type <block key>

### By world

    /domain search world <world name>

## Purging old data

Purging old data may become necessary on high-traffic servers - for every field created, that data must be loaded when Domain starts.  If you have players who place fields and then don't come back to the server, you could end up with a large number of fields that are expired (expiration is set within the configuration).
While these fields are expired and not active in-game, they are still loaded on startup.  You can run two different commands for purging, but understanding that this action can NOT be undone.  Once a field is purged, the data file is removed and cannot be recovered.  It is strongly recommended that you back your Domain folder up prior to purging

### Listing the fields that will be purged

This can be run in-game with the domain.admin permission or via console, and will output a list to the console of all the fields that will be removed if the purge command is run

    /domain purge_list

### Purging

Actually purging the fields can ONLY be run from console

    /domain purge

## Buying/Giving/Getting Domain Blocks

Domain blocks can be purchased or crafted, they can be limited by permission, and a charge can be levied when placing them.  The following commands concern only giving the physical block to the player.

### Opens the GUI to buy a Domain block.
*Requires domain.field*

    /domain buy

### Gets a Domain block without charge.

If no block key is provided, opens a GUI to allow you to choose the block.  If block key is provided, the block will be provided directly to the player
*Requires domain.admin*

    /domain get
    /domain get <block key>

### Gives a Domain block to a player without charge.  
*Player must be online and the block key must be valid*
*Requries the player to be in Domain Bypass mode or, run from console*

    /domain give <player> <block key>
