![Domain](/images/domain_alt_small.png)

# Renting

[Home](https://torpkev.github.io/domain_docs)

Domain allows you to rent out a field to other players.  While they are renting the field, they are considered the owner of the field as far as naming and permissions are applied.

It is important to know that when you rent out a field, the person renting it becomes the defacto owner of the field, and you will not have permission to enter and make changes while it is rented out.


#### Creating a rentable field

To make a field rentable, the [block configuration](https://torpkev.github.io/domain_docs/blockconfig) must have both of the following to be more than 0

    cost_to_rent: 100
    rent_days: 7

The Cost to rent field is how much to charge the player, with rent days being the number of days applied to the rent period.  In the above example, it would cost 100 to rent for 7 days.

#### Placing a Rent Sign

Domain fields are rented by right clicking a rent sign - to create a rent sign, take any sign, right click it on the Domain Block, and it will turn into a rent sign.  You can now place the rent sign as you would any other sign, however you will not be prompted to enter any text on the sign as it will auto-populate.

![Empty Sign](https://torpkev.github.io/domain_docs/images/empty_sign.png)

![Rent Sign](https://torpkev.github.io/domain_docs/images/domain_sign.png)

#### Renting the field

To rent the field, the player needs to right click a Rent Sign that shows the cost and number of days

![Rent Sign](https://torpkev.github.io/domain_docs/images/placed_sign.png)

Once they have right clicked, they will be prompted to confirm:

![Rent Confirm](https://torpkev.github.io/domain_docs/images/rent_confirm.png)

To confirm, click the confirmation in green.

Once rented, the player will receive a message informing them of their new balance

![Rented](https://torpkev.github.io/domain_docs/images/rented.png)

Any rent signs will be updated with the renter and expiration

![Rented Signs](https://torpkev.github.io/domain_docs/images/rented_signs.png)

#### Changing the rent cost/days

You can modify the block configuration as needed, however, players can also override the cost/days from the config file per-field they rent out.  Once the field is rented, the cost/days cannot be modified for the current term, but would be applied next time the rent is extended out, or when a new player rents the field.

If the field is not currently rented, the rent signs will update to the new amount automatically

##### To change the cost:

- Right click the Domain Block with an empty hand

- Click Field Information

![Field Info](https://torpkev.github.io/domain_docs/images/field_info.png)

- Click Rent Cost

![Rent Cost](https://torpkev.github.io/domain_docs/images/rent_cost.png)

- Type in the new amount and press Enter

![Rent Cost Set](https://torpkev.github.io/domain_docs/images/rent_cost_set.png)

- You will receive a message indicating the cost has changed, and any signs (when not currently rented) will update


##### To change the days:

- Right click the Domain Block with an empty hand

- Click Field Information

![Field Info](https://torpkev.github.io/domain_docs/images/field_info.png)

- Click Rent Days

![Rent Days](https://torpkev.github.io/domain_docs/images/rent_days.png)

- Type in the new number of days and press Enter

![Rent Days Set](https://torpkev.github.io/domain_docs/images/rent_days_set.png)

- You will receive a message indicating the days have changed, and any signs (when not currently rented) will update

#### Getting info about your Rentable field


- Right click the Domain Block with an empty hand

- Click Field Information

![Field Info](https://torpkev.github.io/domain_docs/images/field_info.png)

- Click Rent Info

![Rent Info](https://torpkev.github.io/domain_docs/images/rent_info_info.png)

- You will receive a notification about the field

![Rent Rented Info](https://torpkev.github.io/domain_docs/images/rent_rented_info.png)

#### Stopping my field from being rented

To prevent a field being rented, set the cost or days to 0.  Both must be more than 0 to be available.  When the field is not available, it will change as so:

![Rent NA](https://torpkev.github.io/domain_docs/images/rent_na.png)

#### Evicting Players

Evicting players is not currently available to players

### Data File

The data file populates some different fields when a field is rented, as shown below:

    field_name: "Rent Plot 1"
    welcome_msg: "Welcome to plot 1"
    farewell_msg: "Leaving plot 1"
    owner: a98447b6-be3b-43ba-999c-43772708d1de
    allowed:
    - a98447b6-be3b-43ba-999c-43772708d1de
    allowed_clans: []
    renter: 1d75ffda-98b9-458f-9bf0-6cf6f79d2703
    rent_until: 1616510830824
    rent_field_name: "Daves Store!"
    rent_welcome_msg: "Welcome to big Daves house of fun"
    rent_farewell_msg: "So long!"
    rent_allowed:
    - 1d75ffda-98b9-458f-9bf0-6cf6f79d2703
    rent_allowed_clans: []
    
When rented, the rented version of each value (field name, welcome message, farewell message, owner/renter, allowed_clans, allowed players) is overridden with the rent equivalent.  So if the name was queried in the above example, "Daves Store!" would return.

When a rent period ends, these rent values are removed and Domain will default back to using the original values.
