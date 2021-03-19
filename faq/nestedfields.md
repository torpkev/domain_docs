# Nested Fields

[Home](https://torpkev.github.io/domain_docs) - [Back to FAQ](https://torpkev.github.io/domain_docs/faq)

## What are nested fields?

Nested fields occur when you have a field placed within a field.
The field you're placing the field INTO is referred to as the parent field
The field you're placing is referred to as the child field.

## Why would I use a nested field?

When used properly, nested fields can vastly improve the ability to configure your fields as they allow a level of granularity to a field.

For example, if you had the following setup:

#### Parent Field

    FLAGNAME_1: true
    FLAGNAME_2: true
    
#### Child Field
 
     FLAGNAME_1: false
     FLAGNAME_3: true
     
In your parent field, you would have FLAGNAME_1 and FLAGNAME_2 active
In the child field however, you would have FLAGNAME_2 and FLAGNAME_3 active.  FLAGNAME_1 is NOT active because it is overridden in the child.

In a real world example, you could have a parent field that prevents mobs from spawning, but you want to place a mob grinder down - in that case  you would apply the flag to prevent spawning and set it to true in the parent field, then you'd have the same flag set to false in the child field.  The result here would be that in the parent field, mobs would not spawn, but in the child field they would.

## Field Ordering

In order to properly set up your parent/child fields, you should use field ordering.

When a flag is applied, it gets all the Domain fields at your current location, then sorts it by field order from the block configuration.  The lowest field_order value be considered first, and then the next lowest, then the next and so on.

So if you have your field orders set up like:

    PARENT FIELD
    field_order: 2
    flags:
      PREVENT_SPAWN: true
    
    CHILD FIELD
    field_order: 4
    flags: 
      PREVENT_SPAWN: false
    
The parent field would be considered first, so mobs would not spawn.  But then the chlld field would be considered and would allow mobs to spawn at the location it is checking.

If you had a higher field order in your parent field, then it would be considered AFTER the child field, and therefore mobs would not spawn.

## How can I tell what field is being considered?

As a staff member, you can simply enable Bypass mode, and you will see the current field in your action bar
