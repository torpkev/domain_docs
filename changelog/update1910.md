![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.9.10

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

This update adds a new flag, alters behavior or two others, and includes some bug fixes.

New Flag:
PREVENT_CROP_PLANTING_BY_NONALLOWED

This flag will prevent non-allowed players from planting crops in the field

If updating, please add the following to flags.yml

 PREVENT_CROP_PLANTING_BY_NONALLOWED:
    name: "&bPrevent Crop Planting"
    lore: "&fPrevents Non-Allowed Players from planting crops"
    icon_on: LIME_STAINED_GLASS_PANE
    icon_off: RED_STAINED_GLASS_PANE
    locked: false
    
And the following to lang.yml

crop_planting_refused: "&4You cannot plant crops here"

With this change, PREVENT_BREAK no longer protects harvesting crops (use PREVENT_CROP_HARVEST_BY_NONALLOWED) and PREVENT_BUILD will no longer prevent crops from being planted (use PREVENT_CROP_PLANTING_BY_NONALLOWED)

Bug fixes include, but are not limited to console log spamming when working with permissions.
