# Spawner

[Home](https://torpkev.github.io/domain_docs) - [Back to FAQ](https://torpkev.github.io/domain_docs/faq)

## Why would I use a spawner field instead of a mob spawner?

Domain Spawner fields offer more flexibility and security to mob spawning than a standard mob spawner.

- Ability to spawn multiple mob types at once

- You can specify a chance out of 100 for if the mob spawns

- You get to choose the size of the area where they can spawn

- You can spawn mobs in specific light levels that you choose 

- You can limit Domain spawner fields to players with specific permissions

- You can track where the fields are at all times

## How do I use one?

First, you need to create a Spawner field.  There are 2 included in the default files that you can use, or you can modify the defaults to suit your own purposes

Once a spawner block has been created, make sure that the proper limits are set for the player placing it (domain.**BLOCK_KEY**.limit.**MAX_NUMBER**)

The field can now be placed like any other Domain field.  Note that the SPAWN flag MUST be on the field in order for it to work.  It is recommended that it is included, but set to false, allowing the player to turn the field on when they are ready.  This could be especially important with hostile mob spawning.  

NOTE: It is recommended to allow the block to be placed outside of the field - this will allow the player to turn the field on/off as needed without putting themselves at unnecessary risk.

## How do I set up the spawner in the block configuration?

View the block configuration instructions [here](https://torpkev.github.io/domain_docs/blockconfig) which explains each required field

## No mobs are spawning!

For the mob spawner to work, several conditions must be met.

- There must be a player within range.  This player MUST be in survival mode.

- The spawn point must be within the minimum/maximum light levels

- If it requires a slime chunk, the mob being spawned must be in a spawn chunk

- If requires water is true, the mob being spawned must be in or above water (not flowing)

- There is a chance for the mob to spawn, if this is set too low, they may not spawn in

- The mob being spawned might be pushing the entity type limit beyond the maximum

- The field must be enabled

- The SPAWN flag must be set to true

- The mob being spawned cannot be in a PREVENT_SPAWN area

## I checked all that and it STILL isn't working!

Turn on debug mode and check the console.

***NOTE: Debug mode will spam your console - be sure to turn it off again after about a minute***

    /domain debug
    
