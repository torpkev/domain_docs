![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.9.6

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

## Expand/shrink, resize and block opening commands added, Bug fixes

### New Commands

## Domain Open

Opens the current field the player is standing in if they are the owner

    /domain open

## Domain Resize

Gives the player the resize wand for the field they are standing in if they are the owner (also puts the field into resize mode)

    /domain resize
    
## Domain Expand

Expands the current field in the direction specified by the number of blocks requested
Direction can be:  north, east, south, west, up, down   (or alternately: n, e, s, w, u, d)
Blocks is the number of blocks in that direction the field will expand to, keeping in mind that the field is a cuboid, so it will expand for full width/height
Note: Standard resize rules apply (block in field, max volume etc.)

    /domain expand <direction> <blocks>
    
## Domain Shrink

Shrinks the current field in the direction specified by the number of blocks requested
Direction can be:  north, east, south, west, up, down   (or alternately: n, e, s, w, u, d)
Blocks is the number of blocks in that direction the field will shrink to, keeping in mind that the field is a cuboid, so it will shrink for full width/height
Note: Standard resize rules apply (block in field, max volume etc.)

    /domain shrink <direction> <blocks>
    
### Bug Fixes

- Unexpected error would occur in rare cases where the player was unable to open a domain block they own
- Removed unnecessary looping within block checks
- Minor code cleanup

### Update Language File

Add the following to lang.yml

    usage_expand: "Usage: /domain expand &b <direction> <blocks>&r\nDirection is: north/east/south/west/up/down"
    usage_shrink: "Usage: /domain shrink &b <direction> <blocks>&r\nDirection is: north/east/south/west/up/down"
    no_field: "&4No Domain field found"
    unable_give_resize_wand: "&4Sorry, you must have an open inventory slot to get the resize wand"
