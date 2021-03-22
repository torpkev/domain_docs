![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# How do I use Domain to protect my spawn area?

[Home](https://torpkev.github.io/domain_docs) - [Back to FAQ](https://torpkev.github.io/domain_docs/faq)

Domain does a great job at protecting your spawn, but care needs to be taken when setting the fields up.  Before you start, ask yourself the following questions:

- How big of an area should I cover?
- Will I want players to be invincible here?
- Should animals or hostile mobs spawn here?
- Will players need to access chests here?
- Will you want teleport portals set up?

Once you have the answers to these questions, you're ready to start.

## Step 1

Create a new Domain Block that provides the level of protection that you want across the ENTIRE spawn area
*You can see [here](https://torpkev.github.io/domain_docs/createnew) for details on creating a new Domain Block*

This Domain Block should be used ONLY for your spawn and should not be accessible to your players.

Set field order to 1 (This will be important for [nested fields](https://torpkev.github.io/domain_docs/faq/nestedfields))

## Step 2

Place that Domain Block in a central location and resize your field.  
*For most servers, keep in mind that you probably want to set ignore_y_axis to true for spawn, this prevents anyone from tunnelling up or using Elytra over the top of spawn*

## Step 3

Convert the field into an Admin field.  This removes you as the owner and allows other admins to access it.

Open the Domain Block by right clicking it with an open hand
Go into Edit menu
Go into Admin menu
Click to change the block into an Admin field

## Step 4

Set the name, welcome and farewell messages
Open the Domain Block by right clicking it with an open hand
Go into Edit menu
Click the name/welcome/farewell buttons and set them to be sensible values

## Step 5

Identify any areas where you need to allow a flag you're preventing in your main spawn area.

If you have some, create the Domain Block for them, again, this block should be considered for spawn ONLY.  This will save your headaches later on, which you will have if players start using it and the config needs to change.

Make sure the field_order is a higher number than spawn, I find increasing to 5 is helpful as it gives some wiggle room in case you want to add more in.

Place the new fields, repeat step 3 and 4 on the new field.  
