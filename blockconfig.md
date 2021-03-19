# Block Configuration

[Home](https://torpkev.github.io/domain_docs)

Below is a breakdown of each value that is used in the block configuration along with a detailed explanation and sample values.  To see the defafault configurations, click [here](https://torpkev.github.io/domain_docs/defaultfiles) - they are an excellent starting point for creating your own Domain Blocks configurations.

---



#### Block Key

Block key is the internal name used to identify this type of block.  It MUST remain unique and should not contain spaces or any special characters

    block_key: griefprevent

#### Base Material

Base Material of the Domain Block. This is the block that 'is' the Domain block. This MUST be a valid Minecraft block, and is required. 

    base_material: GOLD_BLOCK
 
#### Field Display Material

Domain uses the field display material to display the field visualization.  By default, it uses colored glass, and can be set here.  As with base material, it MUST be a valid Minecraft block and is required.

    field_display_material: ORANGE_STAINED_GLASS

#### Field Display Seconds

The visualization is displayed by default for 30 seconds, if that is too long or too short, you can set it here

    field_display_secs: 30

#### Display Name

Display name is what the block is called when you hover over it in your inventory.  You can use & color codes

    display_name: "&bGrief Prevent"

#### Lore

Lore is the item lore on the Domain Block that you see when you hover over it in your inventory.  You can use & color codes here, and use | to indicate a new line.  Note that the color resets on each line, so if you change color, apply it again at the start of the line.

    lore: "&fGrief Prevent fields protect your builds|&ffrom player griefing and allow|&fyou to claim the area as your own|&dVolume: &725000 blocks" 

#### Volume

Volume is the number of blocks ***available*** in the field.  This is *NOT* necessarily the number of blocks being used.  You can calculate your volume by using (width x depth x height).
For example, if you wanted to create a field that was 25 by 25 and 15 tall, you'd do 25 x 25 x 15 = 9375, so you'd want to allow for at least the 9375 blocks, though in practice, rounding up to 9500 makes life a bit easier.

    volume: 25000

#### Positions 1 to 9

Positions 1 through 9 are for creating the recipe to build your own Domain Block. 
***Note, this approach will be deprecated as of 1.8.0 and future versions will require a new layout.***

Position 1-3 is the top row of a crafting table, as seen left to right.  Position 4-6 is the middle row, and Position 7-9 would be the bottom row.  Each position MUST be filled, and must be a valid Minecraft Material.

You can use AIR to indicate an empty slot, and if you want to make the field unbuildable to most players, BARRIER works well

    position_1: ORANGE_DYE
    position_2: BARRIER
    position_3: ORANGE_DYE
    position_4: BLUE_DYE
    position_5: REDSTONE_BLOCK
    position_6: BLUE_DYE
    position_7: GOLD_INGOT
    position_8: IRON_BLOCK
    position_9: GOLD_INGOT

#### Field Order

Field Order indicates the precedence of fields. The highest number is the field you would be considered indicate the field you would be considered 'in' if you were inside of an area with overlapping fields.
This is especially useful if you wanted to create an area inside a larger field that has contradictory flags, such as allowing mob spawning when the larger field prevents it

    field_order: 2
 
#### Block In Field

Block in field is a true/false field that indicates if the Domain Block must be within the field.  If true, the block must remain within the cuboid during resizing, if false, then you can set the cuboid away from where the block is.  This is convenient for spawn fields and similar where you want want to keep the blocks in a central location, but have the fields somewhere else.

    block_in_field: true 

#### Flags

Flags are the most important thing in Domain - they decide what can happen inside a claimed area.  Domain has over 200 different flags that can be applied (see [here](https://torpkev.github.io/domain_docs/flags))
Keep in mind that some flags are for everyone, some are for the environment, some impact allowed players or non-allowed players etc.  

Be mindful of what flags you apply, and when you nest fields (place one field within another) keep in mind that the child field can override the flag of the parent.  
For example, if you have a field that prevents monsters from spawning, and a child field that allows monsters to spawn, in the child field, the monsters would be allowed to spawn.  This is only true however if it is contradictory.  If you prevent doors being accessed in the parent field and only have monster spawning in the child field, doors will still not be able to be accessed in the child field.

Each flag can be true or false.  If true, that flag will be applied, if false, that flag will NOT be applied.  If both a parent and a child field had for example PREVENT_SPAWN, with the parent set to true and the child set to false, in the parent field, mobs would not spawn.  In the child field, mobs could spawn.

    flags:
      DISPLAY_WELCOME: true
      DISPLAY_FAREWELL: true
      PREVENT_INTERACT_ARMOR_STAND_BY_NONALLOWED: true
      PREVENT_EXPLOSION_DAMAGE: true
      PREVENT_PLAYER_EXPLOSION_DAMAGE: false

#### Cost to Buy

The cost to buy this Domain block using /domain buy. Set to 0 if it should not be purchasable.  *This requires Vault and a valid economy plugin*

    cost_to_buy: 500

#### Cost to Place

The cost to place this Domain Block. Useful if you want to allow players to make their own blocks, but charge them to place them. *This requires Vault and a valid economy plugin*

    cost_to_place: 0
    
#### Cost to Refund

The cost refunded to the player if they 'Take' the field back. *This requires Vault and a valid economy plugin*

    cost_to_refund: 0
    
#### Cost to Rent

Default cost to rent this field *This requires Vault and a valid economy plugin*

    cost_to_rent: 0
    
#### Days to Rent

Default number of days this field can be rented for

    rent_days: 0

#### Default Radius

Default radius is applied when placing the field the first time.  It is the number of blocks along the X and Z axis from the Domain block.  For example, if you want a field that is 10x10, you'd use a radius of 5

    default_radius: 15

#### Default Height Up

Default Height Up is applied when placing the field the first time.  It is the number of blocks up from the Domain Block.  If you placed the Domain block on the ground and wanted it to extend up 7 blocks, set it to 7.

    default_height_up: 10

#### Default Height Down

Default Height Down is applied when placing the field the first time.  It is the number of blocks down from the Domain Block.

    default_height_down: 5

#### Invalid Worlds

Invalid worlds is the list of worlds in which the Domain Block cannot be placed.  Any world not in this list can have it placed there.  This is a list, so you can apply multiple worlds as necessary.

    invalid_worlds:
      - world_nether
      - world_the_end

#### Offline Days

Number of days before the field is considered abandoned. If the owner is offline for this number of days consecutively, the field will auto-expire.  If they owner comes back online, the number of days as offline resets to 0.

This is important especially for high-traffic servers.  Without expiring the fields, you could have a large number of players play one time and claim a field, over time this could include large amounts of prime real-estate.  When the fields expire, the field becomes disabled, and the flags will no longer apply.  There is a purge command which can be used in conjunction with offline_days in order to clear your server of old fields.

    offline_days: 30

#### Ignore Y-Axis

If true, the Y axis (height) is ignored on this block and regardless of resize, will stretch from bedrock to max height. Defaults to false.

    ignore_y_axis: false

#### Max Merge

Merging blocks is used to increase the available volume within a field.  When configured to allow it, a player could have a field with a 25,000 block volume, but may neeed more space.  To save the player placing another field and having to maintain 2 fields, they can instead merge the field, which would increase the available volume (without actually resizing the field).  Max Merge controls how many times a field can be merged, effectively placing a cap on the maximum number of blocks allowed in the field.

    max_merge: 3

#### Max Blocks

Max blocks is the limit per player for this type of Domain Block.  For example, if you set this to 3, then if they tried to place a fourth field, they would receive an error.  This number can be overridden however by using the domain.**BLOCK KEY**.limit.**NUMBER** where block key is the key from the configuration and number is the limit.  Whichever is higher is the limit applied to the player.  So if it was 3 in the configuration, but they had domain.griefprevent.limit.5, then they could place 5 blocks.  If they had domain.griefprevent.limit.1, then they could place 3 as the max blocks value would override.

    max_block: 4

#### Prevent Resize

If true, prevent resize will stop the user from resizing the field by using the option in the menu.  Instead, they will be constrained to whatever is in the default_radius/default_height_up/default_height_down, regardless of the available volume

    prevent_resize: false

#### One-time Use

If true, one time use will prevent a player from 'taking' a field they have already placed.  When set to false, the player can take the field, which will remove the field and return the Domain Block to the player so they can place it again.  If true, attempting to take the field will destroy it.

    one_time_use: false

#### Visualize Corners

If true, visualize corners will force any Domain visualization to only display the corner blocks.  This is especially useful for very large field types where visualizing the field may cause some lag for the player.  If false, the cube visualization is used by default.

    visualize_corners: false

#### Visualize Ring

If true, visualize ring will force any Domaian visualization to use the 'ring' visualization which surrounds the field, but only at player height.  If false, it will use either corner visualization if that is set true, if not, then it will default back to cube visualization.

    visualize_ring: false

#### Spawner

Spawner fields allow mobs to spawn inside of a Domain field in the same manner as using a mob spawner block.  This allows you to create a field for a particular mob and it will continually spawn that type (within limits) without the need to issue a spawner block or eggs to a player.  You can also prevent players from placing a spawner block by utilizing the domain.**BLOCK KEY**.limit.0 permission on them while setting max_blocks to 0.

You could also utilize a spawn block over a large area to spawn in multiple mobs on a continuous basis, for example, if you had a PVE server and wanted to make life difficult for your players, you could spawn 10 zombies every 20 seconds within the field, the exact spawn location would differ each time, and would not need to be in a compressed area like a mob spawner block.

Spawner fields can spawn multiple types of mob at the same time, spawn based on chance, if they're in a specific world, spawn as baby (where the mob is Ageable), can prevent spawning if not over/in water or in a slime chunk or if a maximum number of mobs exist within a range.  You can also specify minimum and maximum light levels for the mobs to spawn in.

For a spawner block to work, a player must be within range, and that player MUST be in survival mode.  This prevents players from mob grinding in creative, or staff members triggering it while they're in spectator mode.  The field must also be enabled, and finally, MUST have the SPAWN flag enabled.  If the field is disabled or the SPAWN flag is set to false or not present, mobs will NOT spawn.

In the example below, the field would spawn a zombie every 20 seconds while players are in range (and field/flag are active), with a 1 in 10 chance that the zombie is a baby, up to a maximum number of 16 zombies within 32 blocks of where the mob is spawning in.

The same field can also spawn in zombie villagers, however, it is a 5/100 chance that they will spawn each 20 seconds, and only up to a maximum of 5 zombie villagers within 32 blocks of where the mob spawns.

    spawn:
      # Entity type to spawn
      # Zombie, only spawns if light level 0-10, 100/100 chance, max of 20 in field
      ZOMBIE:
        # Number of mobs to spawn every 20 seconds (max of 10)
        amount: 1
        # Chance out of 100 for a mob to spawn (100 = always)
        chance: 100
        # Worlds that the mob can spawn in
        worlds:
          - world
        # Minimum light level for spawning (measured at spawn point)
        min_light: 0
        # Maximum light level for spawning (measured at spawn point)
        max_light: 10
        # If requiring water, the mob will only spawn if above a water block (not flowing)
        req_water: false
        # If requiring a slime chunk, the mob will ONLY spawn if in a spawn chunk
        req_slime_chunk: false
        # Chance (0-100) that the mob will spawn as a baby IF it is an ageable mob (animals, zombies etc.)
        baby_chance: 10
        # The number of blocks to consider when checking for entities
        max_distance: 32
        # Sets a cap on the number of this type of entity that can spawn within 32 blocks
        max_entities: 20
      ZOMBIE_VILLAGER:
        # Number of mobs to spawn every 20 seconds (max of 10)
        amount: 1
        # Chance out of 100 for a mob to spawn (100 = always)
        chance: 5
        # Worlds that the mob can spawn in
        worlds:
          - world
        # Minimum light level for spawning (measured at spawn point)
        min_light: 0
        # Maximum light level for spawning (measured at spawn point)
        max_light: 10
        # If requiring water, the mob will only spawn if above a water block (not flowing)
        req_water: false
        # If requiring a slime chunk, the mob will ONLY spawn if in a spawn chunk
        req_slime_chunk: false
        # Chance (0-100) that the mob will spawn as a baby IF it is an ageable mob (animals, zombies etc.)
        baby_chance: 0
        # The number of blocks to consider when checking for entities
        max_distance: 32
        # Sets a cap on the number of this type of entity that can spawn within 32 blocks
        max_entities: 5
 
