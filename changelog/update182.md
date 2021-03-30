![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.8.2

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

## Bug Fixes + Undocumented/unsupported commands

### New Commands

Two new commands that will remain undocumented and unsupported.  They toggle whether the events run or not.
You must either have **domain.admin** permission or run from console

#### Toggle Creature Spawn Event

    /domain spawnevent

#### Toggle Player Move Event

    /domain playermove

### Bug Fixes

- Data files with worlds that no longer exist will NOT load and will generate an error on startup

### Update Language File

Add the following to lang.yml

    spawn_event_disabled: "Spawn event is disabled"
    spawn_event_enabled: "Spawn event is enabled"
    move_event_disabled: "Player Move event is disabled"
    move_event_enabled: "Player Move event is enabled"
