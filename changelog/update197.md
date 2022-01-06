![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.9.7

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

This update only adds a new API function that will be required by Bazaar 1.2.0 (but is available to anyone accessing the API)

FlagFunctions.flagAllowed(Player player, Location location, String flag)

If the flag exists at the location and the player has access to the field, will return true.

If the flag exists at the location and the player does not have access to the field, will return false

If the flag does not exist at the location, will return true.

    public boolean flagAllowed (org.bukkit.entity.Player player,
     org.bukkit.Location location,
     String flag)
    Checks if a player is allowed to perform the action prohibited by the flag provided
    Parameters:
    player - Player to check
    location - Location to check
    flag - Flag to check
    Returns:
    If false, the action is not allowed. If true, either allowed, or flag does not exist here
    
