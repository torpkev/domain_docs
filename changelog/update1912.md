![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.9.12

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)
Vouchers!

Vouchers have been in the pipeline for a while, and are intended as a way to improve a Domain field without having to replace the entire block.

Here is a brief Vouchers FAQ

What are they?
Vouchers are a piece of paper that you can right click a Domain block with, and the properties of the voucher are applied to the Domain block

What kind of properties?
Vouchers can currently do two things
They can add additional space to a field - Each field has a maximum volume that your user can resize - with a voucher, you can apply additional space, either as a reward, or as a purchase the player makes.
Additional flags can be applied to a field - Each field is set up with a base set of flags, such as PREVENT_BREAK etc.  You can apply additional flags with a voucher, so for example, if you wanted to give the a no-pvp option, you could give them the base field, and provide them an additional, voucher for PREVENT_PVP.  You can apply multiple flags to a single voucher.

What if they already have that flag?
If the field already has the flag, the voucher is applied, but that flag will not be impacted

What if they break the field?
Vouchers are set as either single use, or not single use.  If single use, they can be applied once only and if the field is broken, they lose the voucher.  If not single use, when the field is broken, the voucher is put in their inventory (or dropped on the ground if the inventory is full)

How do you set them up?
Vouchers are very simple to set up, you simply need to create a yml in the Vouchers folder for it

How do I get a voucher?
As an admin, you can type
/domain voucher <voucher key>

Where <voucher key> is the name of the yml file without the .yml (for example, if you have minershaste.yml, the key is minershaste)

Can I remove a voucher without destroying the block?
Not currently - that is planned for the future

Can I add multiple vouchers of the same type?
No - This is deliberate in order to prevent out of control sized fields.  However, depending on interest, I may add a max uses field

Do I HAVE to use vouchers?
No - If you don't want to use them, just don't provide them to your players!

Can I as the admin disable a voucher?
To remove a voucher from EVERYONE, simply remove the voucher from your Vouchers folder, when you reload, the benefits of the voucher will not be applied.  However, any resize the player has done will NOT roll back, but they will be limited if they resize again.

Falling out of the world

An option has been added to the config which, if enabled, will prevent players from falling out of the world if they go below bedrock (not that they SHOULD be going beneath bedrock!) -  This is a GLOBAL option, and is not applied by Domain field. If they drop outside the upper/lower height limits for the world, they will be teleported.  You can specify where they teleport to in the config, if that is not a safe location, they will teleport to their bed, and if that is not available, will teleport to world spawn.  The player will receive feather falling and slowness for 3 seconds in order to offset any potential downwards velocity that might make them go splat.

Additional 1.19 Support

Added support for Mangrove doors, gates, trapdoors, buttons, and pressure plates
Added support for Tadpole buckets

Cleanup

- Removed deprecated command functions
- Removed deprecated API calls from 1.9.11
- Removed deprecated Vault functions
- Removed unused functions
- Corrected documentation of API functions

