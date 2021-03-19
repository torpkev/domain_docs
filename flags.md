# Flags

Domain has over 200 flags that can be combined in order to grant or prevent access to nearly anything in the game.

Each flag can be either true or false.  If true, the flag is active in that field, if false, the flag is not active in that field.  

    FLAGNAME_1: true
    FLAGNAME_2: false

Nested fields allow for more complex mixes of contradictory flags, for example, if the parent field has this:

    FLAGNAME_1: true
    FLAGNAME_2: true
    
And the child field had:

    FLAGNAME_1: false


FLAGNAME_1 would be active in the parent field, but not the child, but FLAGNAME_2 would be active in both parent and child.

A full breakdown of each flag is listed below:

---

| Flag Name | Description |
| --- | --- |
| DISPLAY_FAREWELL | Displays a message when a player leaves the field |
| DISPLAY_WELCOME | Displays a message when a player enters the field |

EFFECT_BLINDNESS_NONALLOWED

    Gives Blindness effect to non-allowed players

EFFECT_CONFUSION_NONALLOWED

    Gives Confusion effect to non-allowed players

EFFECT_HUNGER_NONALLOWED

    Gives Hunger effect to non-allowed players

EFFECT_LEVITATION_ALLOWED

    Gives Levitation effect to allowed players

EFFECT_MINERS_HASTE_ALLOWED

    Gives Miners Haste effect to allowed players

EFFECT_NIGHT_VISION_ALLOWED

    Gives Night Vision effect to allowed players

EFFECT_SLOW_DIGGING_NONALLOWED

    Gives Slow Digging effect to non-allowed players

EFFECT_WATER_BREATHING_ALLOWED

    Gives Water Breathing effect to allowed players

EFFECT_WEAKNESS_NONALLOWED

    Gives Weakness effect to non-allowed players

EFFECT_WITHER_NONALLOWED

    Gives Wither effect to non-allowed players

ENABLE_FLY_FOR_ALLOWED

    Allowed players can fly within the field

EPIDEMIC_PREVENT_AFFLICT

    Prevents Epidemic ailments from afflicting players here

EPIDEMIC_PREVENT_SYMPTOMS

    Prevents Epidemic symptoms from affecting players here

GLOW_NONALLOWED_PLAYER_ON_PVP

    Causes non-allowed players to glow if they hit another player

HARM_NONALLOWED_PLAYER

    Causes damage to non-allowed players

HEAL_ALL_PLAYERS

    Heals any player in the field

HEAL_ALLOWED_PLAYER

    Heals allowed players in the field

INSTANT_HEAL_ALLOWED_PLAYER

    Instantly heals allowed players in the field

MEMBERS_ONLY

    Prevents access to any player without a specific permission as defined in block config

PREVENT_ACCESS_BY_NONALLOWED

    Prevents non-allowed players from entering the field, and will teleport them back to spawn if they try repeatedly

PREVENT_ALLOWED_PLAYER_CONTACT_DAMAGE

    Prevents allowed players from taking contact damage

PREVENT_ALLOWED_PLAYER_DROWN

    Prevents allowed players from taking drowning damage

PREVENT_ALLOWED_PLAYER_EXPLOSION_DAMAGE

    Prevents allowed players from taking explosion damage

PREVENT_ALLOWED_PLAYER_FALL_DAMAGE

    Prevents allowed players from taking fall damage

PREVENT_ALLOWED_PLAYER_FIRE_DAMAGE

    Prevents allowed players from taking fire damage

PREVENT_ALLOWED_PLAYER_WITHER_DAMAGE

    Prevents allowed players from taking wither damage

PREVENT_ANIMAL_DAMAGE_BY_ALL

    Prevents animals taking damage from any source

PREVENT_ANIMAL_DAMAGE_BY_ALLOWED

    Prevents animals taking damage from allowed players

PREVENT_ANIMAL_DAMAGE_BY_NONALLOWED

    Prevents animals taking damage from non-allowed players

PREVENT_ANIMAL_DAMAGE_BY_NONPLAYER

    Prevents animals taking damage from non-players (monsters)

PREVENT_ARROW_INTERACT

    Prevents arrows interacting with buttons

PREVENT_BAZAAR_BUY_BY_NONALLOWED

    Prevents Non-Allowed players from buying from a Bazaar shop

PREVENT_BAZAAR_CREATE_BY_NONALLOWED

    Prevents Non-Allowed players from creating a Bazaar shop

PREVENT_BAZAAR_REMOVE_BY_NONALLOWED

    Prevents Non-Allowed players from removing a Bazaar shop

PREVENT_BAZAAR_SELL_BY_NONALLOWED

    Prevents Non-Allowed players from selling to a Bazaar shop

PREVENT_BLOCK_BURN

    Prevents blocks from burning away

PREVENT_BREAK

    Prevents non-allowed players from breaking blocks

PREVENT_BREAK_BOAT_BY_NONALLOWED

    Prevents non-allowed players from breaking boats

PREVENT_BREAK_ITEM_FRAME_BY_NONALLOWED

    Prevents non-allowed players from breaking item frames

PREVENT_BREAK_MINECART_BY_NONALLOWED

    Prevents non-allowed players from breaking minecarts

PREVENT_BREAK_PAINTING_BY_NONALLOWED

    Prevents non-allowed players from breaking paintings

PREVENT_BREEDING

    Prevents mobs from breeding

PREVENT_BUCKET_FILL_BY_NONALLOWED

    Prevents non-allowed players from filling buckets

PREVENT_BUILD

    Prevents non-allowed players from buidling

PREVENT_BUILD_EXCEPT_DOMAINBLOCK

    Prevents players from building except placing Domain blocks

PREVENT_BUILD_IRON_GOLEM

    Prevents Iron Golems being built

PREVENT_BUILD_SNOWMAN

    Prevents Snowmen from being built

PREVENT_BUTTON_ACCESS_BY_NONALLOWED

    Prevents non-allowed players from interacting with buttons

PREVENT_CHORUSFRUIT_TO

    Prevents using chorus fruit to teleport into the field

PREVENT_COMMAND_CUSTOM1_BY_NONALLOWED

    Prevents non-allowed players from running commands in custom 1 slot in config

PREVENT_COMMAND_CUSTOM2_BY_NONALLOWED

    Prevents non-allowed players from running commands in custom 2 slot in config

PREVENT_COMMAND_CUSTOM3_BY_NONALLOWED

    Prevents non-allowed players from running commands in custom 3 slot in config

PREVENT_COMMAND_CUSTOM4_BY_NONALLOWED

    Prevents non-allowed players from running commands in custom 4 slot in config

PREVENT_COMMAND_HOME_BY_NONALLOWED

    Prevents non-allowed players from running home commands

PREVENT_COMMAND_TELEPORT_BY_NONALLOWED

    Prevents non-allowed players from running teleport commands

PREVENT_CROP_DAMAGE_BY_NONALLOWED

    Prevents non-allowed players from damaging crops

PREVENT_CROP_DAMAGE_BY_NONPLAYER

    Prevents non-players from damaging crops

PREVENT_DOOR_ACCESS_BY_NONALLOWED

    Prevents non-allowed players from accessing doors

PREVENT_DROP_ITEM_BY_NONALLOWED

    Prevents non-allowed players from dropping items

PREVENT_ELYTRA_GLIDING

    Prevent Elytra glinding

PREVENT_END_PORTAL_BY_NONALLOWED

    Prevents non-allowed players from using an end portal

PREVENT_ENDERPEARL_TO

    Prevents enderpearls being used to teleport into the field

PREVENT_EXIT_BY_NONALLOWED

    Prevents non-allowed players from leaving the field

PREVENT_EXPLOSION_DAMAGE

    Prevents explosion damage

PREVENT_FIRE_IGNITE

    Prevents fire ignition

PREVENT_FIRE_SPREAD

    Prevents fire spreading

PREVENT_FIREWORK_LAUNCH_BY_NONALLOWED

    Prevents non-allowed players from launching fireworks

PREVENT_GATE_ACCESS_BY_NONALLOWED

    Prevents non-allowed players from accessing gates

PREVENT_GROW_BAMBOO

    Prevent bamboo from growing

PREVENT_GROW_BEETROOTS

    Prevents beetroot from growing

PREVENT_GROW_CACTUS

    Prevents cactus from growing

PREVENT_GROW_CARROTS

    Prevents carrots from growing

PREVENT_GROW_CHORUS_FLOWER

    Prevents chrous flowers from growing

PREVENT_GROW_CHORUS_PLANT

    Prevents chrous plants from growing

PREVENT_GROW_COCOA

    Prevents cocoa from growing

PREVENT_GROW_KELP

    Prevents kelp from growing

PREVENT_GROW_MELON

    Prevents melons from growing

PREVENT_GROW_NETHER_WART

    Prevents nether wart from growing

PREVENT_GROW_POTATOES

    Prevents potatoes from growing

PREVENT_GROW_PUMPKIN

    Prevents pumpkin from growing

PREVENT_GROW_SUGAR_CANE

    Prevents sugar cane from growing

PREVENT_GROW_SWEET_BERRY_BUSH

    Prevents sweet berry bushes from growing

PREVENT_GROW_TURTLE_EGG

    Prevents turtle eggs from growing

PREVENT_GROW_VINE

    Prevents vines from growing

PREVENT_GROW_WHEAT

    Prevents wheat from growing

PREVENT_HEAL_ZOMBIE_VILLAGER_BY_NONALLOWED

    Prevents non-allowed players from healing zombie villagers

PREVENT_INTERACT

    Prevents non-allowed players from interacting with interactable blocks

PREVENT_INTERACT_ANVIL_BY_NONALLOWED

    Prevents non-allowed players from interacting with anvils

PREVENT_INTERACT_ARMOR_STAND_BY_NONALLOWED

    Prevents non-allowed players from interacting with armor stands

PREVENT_INTERACT_BARREL_BY_NONALLOWED

    Prevents non-allowed players from accessing barrels

PREVENT_INTERACT_BED_BY_NONALLOWED

    Prevents non-allowed players from interacting with beds

PREVENT_INTERACT_BEEHIVE_BY_NONALLOWED

    Prevents non-allowed players from interacting with beehives

PREVENT_INTERACT_BEENEST_BY_NONALLOWED

    Prevents non-allowed players from interacting with bee nests

PREVENT_INTERACT_BELL_BY_NONALLOWED

    Prevents non-allowed players from interacting with bells

PREVENT_INTERACT_BLAST_FURNACE_BY_NONALLOWED

    Prevents non-allowed players from interacting with blast furnaces

PREVENT_INTERACT_BREWING_STAND_BY_NONALLOWED

    Prevents non-allowed players from interacting with brewing stands

PREVENT_INTERACT_CAKE_BY_NONALLOWED

    Prevents non-allowed players from interacting with cakes

PREVENT_INTERACT_CAMPFIRE_BY_NONALLOWED

    Prevents non-allowed players from interacting with campfires

PREVENT_INTERACT_CARTOGRAPHY_TABLE_BY_NONALLOWED

    Prevents non-allowed players from interacting with cartography tables

PREVENT_INTERACT_CHEST_BY_NONALLOWED

    Prevents non-allowed players from accessing chests

PREVENT_INTERACT_COMPOSTER_BY_NONALLOWED

    Prevents non-allowed players from interacting with composters

PREVENT_INTERACT_CRAFTING_TABLE_BY_NONALLOWED

    Prevents non-allowed players from interacting with crafting tables

PREVENT_INTERACT_DISPENSER_BY_NONALLOWED

    Prevents non-allowed players from interacting with dispensers

PREVENT_INTERACT_DROPPER_BY_NONALLOWED

    Prevents non-allowed players from interacting with droppers

PREVENT_INTERACT_ENCHANTING_TABLE_BY_NONALLOWED

    Prevents non-allowed players from interacting with enchanting tables

PREVENT_INTERACT_ENDERCHEST_BY_NONALLOWED

    Prevents non-allowed players from accessing enderchests

PREVENT_INTERACT_FURNACE_BY_NONALLOWED

    Prevents non-allowed players from interacting with furnaces

PREVENT_INTERACT_GRINDSTONE_BY_NONALLOWED

    Prevents non-allowed players from interacting with grindstones

PREVENT_INTERACT_HOPPER_BY_NONALLOWED

    Prevents non-allowed players from interacting with hoppers

PREVENT_INTERACT_LECTERN_BY_NONALLOWED

    Prevents non-allowed players from interacting with lecterns

PREVENT_INTERACT_LEVER_BY_NONALLOWED

    Prevents non-allowed players from interacting with levers

PREVENT_INTERACT_LODESTONE_BY_NONALLOWED

    Prevents non-allowed players from interacting with lodestones

PREVENT_INTERACT_LOOM_BY_NONALLOWED

    Prevents non-allowed players from interacting with looms

PREVENT_INTERACT_REDSTONE_REPEATER_BY_NONALLOWED

    Prevents non-allowed players from interacting with redstone repeaters

PREVENT_INTERACT_SHULKERBOX_BY_NONALLOWED

    Prevents non-allowed players from accessing shulkerboxes

PREVENT_INTERACT_SMITHINGTABLE_BY_NONALLOWED

    Prevents non-allowed players from interacting with smithing tables

PREVENT_INTERACT_SMOKER_BY_NONALLOWED

    Prevents non-allowed players from interacting with smokers

PREVENT_INTERACT_STONECUTTER_BY_NONALLOWED

    Prevents non-allowed players from interacting with stonecutters

PREVENT_INTERACT_SWEET_BERRY_BUSH_BY_NONALLOWED

    Prevents non-allowed players from interacting with sweet berry bushes

PREVENT_ITEM_FRAME_ACCESS_BY_NONALLOWED

    Prevents non-allowed players from accessing item frames

PREVENT_ITEM_PICKUP_BY_NONALLOWED

    Prevents non-allowed players from picking up items

PREVENT_ITEM_PICKUP_BY_VILLAGER

    Prevents villagers picking up items

PREVENT_LAVA_FLOW

    Prevents lava flow

PREVENT_LAVA_FLOW_TO

    Prevents lava flowing into a field

PREVENT_LAVA_PLACE

    Prevents emptying lava in the field

PREVENT_LEAD_BY_NONALLOWED

    Prevents non-allowed players from using a lead

PREVENT_LINGERINGPOTION_EFFECT

    Prevents lingering potion effects

PREVENT_MAGIC

    Prevents magic damage

PREVENT_MOB_CONTACT_DAMAGE

    Prevents mobs from taking contact damage

PREVENT_MOB_DROWN

    Prevents mobs from taking drowning damage

PREVENT_MOB_EXPLOSION_DAMAGE

    Prevents mobs from taking explosion damage

PREVENT_MOB_FALL_DAMAGE

    Prevents mobs from taking fall damage

PREVENT_MOB_FIRE_DAMAGE

    Prevents mobs from taking fire damage

PREVENT_MOB_WITHER_DAMAGE

    Prevents mobs from taking wither damage

PREVENT_MONSTER_DAMAGE_BY_ALL

    Prevents damage to monsters by any source

PREVENT_MONSTER_DAMAGE_BY_ALLOWED

    Prevents allowed players from damaging monsters

PREVENT_MONSTER_DAMAGE_BY_NONALLOWED

    Prevents non-allowed players from damaging monsters

PREVENT_MONSTER_DAMAGE_BY_NONPLAYER

    Prevents non-players (other mobs) from damaging monsters

PREVENT_MOUNT_ANIMAL_BY_NONALLOWED

    Prevents non-allowed players from mounting animals

PREVENT_NETHER_PORTAL_BY_NONALLOWED

    Prevents non-allowed players from using nether portals

PREVENT_PISTON_MOVE_INTO_FIELD

    Prevents pistons moving blocks into the field

PREVENT_PISTON_MOVE_OUT_FIELD

    Prevents pistons moving blocks out of the field

PREVENT_PLACE_PAINTING_BY_NONALLOWED

    Prevents non-allowed players from placing paintings

PREVENT_PLAYER_ATTACK_DAMAGE_BY_CREATURE

    Prevents players taking attack damage by any living entity

PREVENT_PLAYER_CONTACT_DAMAGE

    Prevent any player taking contact damage

PREVENT_PLAYER_DROWN

    Prevent any player from taking drowning damage

PREVENT_PLAYER_EXPLOSION_DAMAGE

    Prevent any player from taking explosion damage

PREVENT_PLAYER_FALL_DAMAGE

    Prevent any player from taking fall damage

PREVENT_PLAYER_FIRE_DAMAGE

    Prevent any player taking fire damage

PREVENT_PLAYER_WITHER_DAMAGE

    Prevent any player taking wither damage

PREVENT_PRESSURE_PLATE_ACCESS_BY_NONALLOWED

    Prevents non-allowed players from interacting with pressure plates

PREVENT_PROJECTILE_ITEM_FRAME

    Prevents projectiles such as arrows/tridents from interacting with item frames

PREVENT_PROJECTILE_PAINTING

    Prevents projectiles such as arrows/tridents from interacting with paintings

PREVENT_PVP

    Prevents player on player damage

PREVENT_PVP_BY_NONALLOWED

    Prevents non-allowed players from attacking other players

PREVENT_PVP_TELEPORT_FROM

    Prevents teleporting from the field after hitting another player

PREVENT_PVP_TELEPORT_TO

    Prevents teleporting to the field after hitting another player

PREVENT_SADDLE_BY_NONALLOWED

    Prevents non-allowed players from saddling an animal

PREVENT_SHEAR_BY_NONALLOWED

    Prevents non-allowed players from shearing sheep

PREVENT_SHEEP_DYE

    Prevents sheep being dyed

PREVENT_SHEEP_REGROW_WOOL

    Prevents sheep from regrowing their wool

PREVENT_SPAWN

    Prevents any entity from being spawned

PREVENT_SPAWN_EVOKER

    Prevents Evokers from being spawned

PREVENT_SPAWN_FISH_FROM_BUCKET_BY_NONALLOWED

    Prevents non-allowed players from spawning fish from a bucket

PREVENT_SPAWN_HOSTILE

    Prevents hostile entities from being spawned

PREVENT_SPAWN_ILLUSIONER

    Prevents illusioners from being spawned

PREVENT_SPAWN_NONHOSTILE

    Prevents non-hostile entities from being spawned

PREVENT_SPAWN_PHANTOM

    Prevents phantoms from being spawned

PREVENT_SPAWN_PILLAGER

    Prevents Pillagers from spawning

PREVENT_SPAWN_RAVAGER

    Prevents Ravagers from spawning

PREVENT_SPAWN_VEX

    Prevents Vex from being spawned

PREVENT_SPAWN_VINDICATOR

    Prevents Vindicators from being spawned

PREVENT_SPAWN_WANDERING_TRADER

    Prevents wandering trader from spawning

PREVENT_SPAWNER_EGG

    Prevents the use of spawner eggs

PREVENT_SPLASHPOTION_EFFECT

    Prevents the splash potion effects

PREVENT_SPONGE_ABSORB

    Prevents sponges from absorbing water

PREVENT_TAME_BY_NONALLOWED

    Prevents non-allowed players from taming animals

PREVENT_TELEPORT_TO

    Prevents teleporting into the field

PREVENT_TNT_PRIMING

    Prevents TNT priming (PaperMC Only)

PREVENT_TRAPDOOR_ACCESS_BY_NONALLOWED

    Prevents non-allowed players from accessing trapdoors

PREVENT_VEHICLE_ENTER_ALL

    Prevents all entities from entering vehicles

PREVENT_VEHICLE_ENTER_BY_NONALLOWED

    Prevents non-allowed players from entering vehicles

PREVENT_VEHICLE_ENTER_BY_NONPLAYER

    Prevents monsters and animals from entering a vehicle

PREVENT_VEHICLE_EXIT_ALL

    Prevents all entities from exiting vehicles

PREVENT_VEHICLE_EXIT_BY_NONALLOWED

    Prevents non-allowed players from exiting vehicles

PREVENT_VEHICLE_EXIT_BY_NONPLAYER

    Prevents monsters and animals from exiting vehicles

PREVENT_VEHICLE_PLACE_BY_NONALLOWED

    Prevents non-allowed players from placing vehicles

PREVENT_VILLAGER_DAMAGE_BY_ALL

    Prevents villagers taking damage from any source

PREVENT_VILLAGER_DAMAGE_BY_ALLOWED

    Prevents allowed players from damaging villagers

PREVENT_VILLAGER_DAMAGE_BY_NONALLOWED

    Prevents non-allowed players from damaging villagers

PREVENT_VILLAGER_DAMAGE_BY_NONPLAYER

    Prevents non-players from damaging villagers

PREVENT_VILLAGER_FIRE

    Prevents villagers taking fire damage

PREVENT_VILLAGER_TRADE_BY_ALL

    Prevents any player from trading with a villager

PREVENT_VILLAGER_TRADE_BY_NONALLOWED

    Prevents non-allowed players from trading with villagers

PREVENT_WATER_FLOW

    Prevents water flowing in the field

PREVENT_WATER_FLOW_TO

    Prevents water flowing into the field

PREVENT_WATER_PLACE

    Prevents emptying a bucket of water

REMOVE_FIRED_ARROWS_BY_NONALLOWED

    Removes arrows fired by non-allowed players

REMOVE_FIRED_FLAME_ARROWS_BY_NONALLOWED

    Removes flame arrows fired by non-allowed players

REPAIR_MAIN_HAND_ITEM

    Repairs the item in the main hand

RUN_COMMAND

    Runs enter/leave commands

SNITCH_ON_ENTER

    Snitches to the owner of the field when you enter (if they are online)

SNITCH_ON_LEAVE

    Snitches to the owner of the field when you leave (if they are online)

SPAWN

    Allows spawning of mobs in Spawn fields

TELEPORT_TO

    Teleports the player to a set location
	
