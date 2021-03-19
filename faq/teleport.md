# Creating a Teleport Portal

[Home](https://torpkev.github.io/domain_docs) - [Back to FAQ](https://torpkev.github.io/domain_docs/faq)

Domain Teleport Fields will teleport a player to a preset location.  This location can be in any active world, but will assess the area before teleportingg to ensure that it is safe.

A teleport block is included in the [default files](https://torpkev.github.io/domain_docs/defaultfiles), however, you can add the flag to any field.

    TELEPORT_TO: true
    
When this flag is active and the location is set, the player will be teleported when they enter the field.

## How do I set the location to teleport to?

Once you place the field, following the instructions below:

- Right click the Domain Block with an open hand to open the menu

- Click into the Edit Menu

 ![editbutton](/images/edit_button.png)

- Click into the Admin Menu

 ![adminbutton](/images/admin_button.png)

- Click the Teleport button

 ![teleportbutton](/images/teleport_button.png)
  
- You will be given a Domain Teleport Wand

 ![teleportwand](/images/teleport_wand.png)

- Left click the location you wish to teleport to

- Return to the Domain Block and left click with the wand to set the location

- If it is a valid location, your teleport location is now set

- Check that the TELEPORT_TO flag is enabled

## How do I lock the teleport location to allowed players only?

The easiest way to lock your teleport location is to also apply the PREVENT_ACCESS_TO_NONALLOWED flag

## My location is set but I'm not teleporting!

Either the location you want to teleport to is no longer safe, or you're in Domain Bypass mode.

## How do I fix that?

Reset the teleport location by repeating the steps you used to create it.

If you're in domain bypass mode, turn it off
