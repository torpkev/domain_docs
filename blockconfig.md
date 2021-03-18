# Block Configuration

[Home](https://torpkev.github.io/domain_docs)

Base Material of the Domain Block. This is the block that 'is' the Domain block. This MUST be a valid Minecraft block, and is required. 

> base_material: GOLD_BLOCK
 
Domain uses the field display material to display the field visualization.  By default, it uses colored glass, and can be set here.  As with base material, it MUST be a valid Minecraft block and is required.

> field_display_material: ORANGE_STAINED_GLASS

The visualization is displayed by default for 30 seconds, if that is too long or too short, you can set it here

> field_display_secs: 30

Display name is what the block is called when you hover over it in your inventory.  You can use & color codes

> display_name: "&bGrief Prevent"

Lore is the item lore on the Domain Block that you see when you hover over it in your inventory.  You can use & color codes here, and use | to indicate a new line.  Note that the color resets on each line, so if you change color, apply it again at the start of the line.

> lore: "&fGrief Prevent fields protect your builds|&ffrom player griefing and allow|&fyou to claim the area as your own|&dVolume: &725000 blocks" 

Volume is the number of blocks ***available*** in the field.  This is *NOT* necessarily the number of blocks being used.  You can calculate your volume by using (width x depth x height).
For example, if you wanted to create a field that was 25 by 25 and 15 tall, you'd do 25 x 25 x 15 = 9375, so you'd want to allow for at least the 9375 blocks, though in practice, rounding up to 9500 makes life a bit easier.

> volume: 25000

Positions 1 through 9 are for creating the recipe to build your own Domain Block.  Note, this approach will be deprecated as of 1.8.0 and future versions will require a new layout.
Position 1-3 is the top row of a crafting table, as seen left to right.  Position 4-6 is the middle row, and Position 7-9 would be the bottom row.  Each position MUST be filled, and must be a valid Minecraft Material.

You can use AIR to indicate an empty slot, and if you want to make the field unbuildable to most players, BARRIER works well

> position_1: ORANGE_DYE
> position_2: BARRIER
> position_3: ORANGE_DYE
> position_4: BLUE_DYE
> position_5: REDSTONE_BLOCK
> position_6: BLUE_DYE
> position_7: GOLD_INGOT
> position_8: IRON_BLOCK
> position_9: GOLD_INGOT
 
Field Order indicates the precedence of fields. The highest number is the field you would be considered indicate the field you would be considered 'in' if you were inside of an area with overlapping fields.
This is especially useful if you wanted to create an area inside a larger field that has contradictory flags, such as allowing mob spawning when the larger field prevents it

> field_order: 2
 
Block in field is a true/false field that indicates if the Domain Block must be within the field.  If true, the block must remain within the cuboid during resizing, if false, then you can set the cuboid away from where the block is.  This is convenient for spawn fields and similar where you want want to keep the blocks in a central location, but have the fields somewhere else.

> block_in_field: true 

Flags are the most important thing in Domain - they decide what can happen inside a claimed area.  Domain has over 200 different flags that can be applied (see [here](https://torpkev.github.io/domain_docs/flags))
Keep in mind that some flags are for everyone, some are for the environment, some impact allowed players or non-allowed players etc.  

Be mindful of what flags you apply, and when you nest fields (place one field within another) keep in mind that the child field can override the flag of the parent.  
For example, if you have a field that prevents monsters from spawning, and a child field that allows monsters to spawn, in the child field, the monsters would be allowed to spawn.  This is only true however if it is contracdictory.  If you prevent doors being accessed in the parent field and only have monster spawning in the child field, doors will still not be able to be accessed in the child field.

Each flag can be true or false.  If true, that flag will be applied, if false, that flag will NOT be applied.  If both a parent and a child field had for example PREVENT_SPAWN, with the parent set to true and the child set to false, in the parent field, mobs would not spawn.  In the child field, mobs could spawn.

> flags:
>   DISPLAY_WELCOME: true
>   DISPLAY_FAREWELL: true
>   PREVENT_INTERACT_ARMOR_STAND_BY_NONALLOWED: true
>   PREVENT_EXPLOSION_DAMAGE: true
>   PREVENT_PLAYER_EXPLOSION_DAMAGE: true
   
