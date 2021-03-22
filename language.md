![Domain](/images/domain_alt_small.png)

# Languages

[Home](https://torpkev.github.io/domain_docs/resources)

Domain supports language translations by modifing the [lang.yml](https://torpkev.github.io/domain_docs/resources/lang.yml) file.

Currently, only English is included, however, I will link other translations as provided by users, but will not be able to offer support on them.

The language file is broken out like:

    code: written text
    
In some cases, you will see values like <%value%> - these translate to an appropriate value in game, however, they are not persistent across all translations, so only use them if they exist in the english translation already.

For example:

    snitch_message_enter: "&3[Snitch]&r <%player%> has entered your <%blocktype%> field at <%location%>"
    teleported_to_spawn: "&4You have been teleported back to spawn"
    
You could not put <%player%>, <%blocktype%> or <%location%> into teleported_to_spawn as they may not apply.

I will try and keep [lang.yml](https://torpkev.github.io/domain_docs/resources/lang.yml) up to date with each update, but if changes are required from version to version, it will be noted in the change log.  If a code is ever missing from the lang.yml file, it will default to English.

---

Additional translated language files:

- [Russian](https://torpkev.github.io/domain_docs/resources/user/mircus/lang.zip) provided by Mircus Izgoi (zipped as it does not display properly in the browser)
