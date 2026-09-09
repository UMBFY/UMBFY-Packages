# UMBFY Release Documentation Checklist

Use this checklist for every package release that changes customer-facing behavior.

## Package information

- [ ] Package name and NuGet ID are correct
- [ ] Supported Umbraco versions match package metadata and validation
- [ ] Installation command is correct
- [ ] Configuration examples match real option names and defaults
- [ ] Security / permission behavior is documented

## Feature documentation

- [ ] Every new public feature has a user-facing guide
- [ ] Changed workflows are reflected in existing guides
- [ ] Limitations and unsupported scenarios are explicit
- [ ] Troubleshooting includes newly known failure modes
- [ ] FAQ is updated for recurring customer questions

## Screenshots

- [ ] New user-visible features have current Backoffice screenshots
- [ ] Changed UI has updated screenshots
- [ ] Existing screenshots were reviewed for accuracy
- [ ] No customer data, secrets, private domains, or personal information are visible
- [ ] Image paths and filenames follow the screenshot standard

## Release and upgrade

- [ ] Changelog / release notes describe material customer-facing changes
- [ ] Breaking changes are explicit
- [ ] Upgrade / migration instructions exist when required
- [ ] Database/storage changes include operational notes where relevant
- [ ] Compatibility differences between supported Umbraco versions are documented

## Publishing quality

- [ ] Internal links resolve
- [ ] Public docs navigation includes new pages
- [ ] Package README points to the correct docs and issue tracker
- [ ] Marketplace / NuGet documentation URLs are correct
- [ ] Documentation is reviewed as part of the release PR

A feature is not considered release-complete when code is finished but its user-visible documentation is stale or missing.
