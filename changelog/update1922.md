![Domain](https://torpkev.github.io/domain_docs/images/domain_alt_small.png)

# Change Log 1.9.10

[Home](https://torpkev.github.io/domain_docs) - [Back to Change Logs](https://torpkev.github.io/domain_docs/changelog)

Bug fixes (multiple)

Significant code cleanup, including removing duplicate functions, inconsistent logging, removing deprecated, unused functions

debug_to_file has been removed - having it in the config file will no longer do anything - (it already saves to latest.log)

Deprecated API calls have been removed

Current API calls have now been deprecated and will be removed in an upcoming version and have been moved to Domain.instance().api().FUNCTIONNAME

