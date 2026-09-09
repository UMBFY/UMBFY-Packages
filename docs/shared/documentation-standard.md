# UMBFY Package Documentation Standard

Every UMBFY package must follow the same documentation structure so customers do not have to relearn where information lives.

## Required sections

1. Overview and value proposition
2. Intended users / use cases
3. Supported Umbraco and .NET versions
4. Installation
5. Quick Start
6. Feature guides
7. Configuration
8. Permissions, security, and privacy behavior
9. Screenshots for user-visible features
10. Operations / diagnostics where relevant
11. Troubleshooting
12. FAQ
13. Upgrade / migration guidance when behavior or storage changes
14. Changelog / release notes
15. Support and issue-reporting guidance

## Audience separation

Documentation should distinguish:

- **Editors** — how to use the feature safely in the Backoffice.
- **Administrators** — installation, configuration, permissions, diagnostics, and operations.
- **Developers** — architecture, APIs, extension points, events, storage, and integration behavior where public extension points exist.

Do not force editors to read implementation-level material to understand a workflow.

## Feature-page template

Each major feature page should contain:

```text
# Feature name

What it does
Why / when to use it
Where to find it
Required permissions

## Step-by-step
1. ...
2. ...
3. ...

## Understanding the result

## Screenshots

## Examples

## Limitations

## Troubleshooting

## Related features
```

## Terminology

Use Umbraco terminology consistently. Prefer **Umbraco Backoffice**, **Document**, **Media**, **Workspace**, and the official UMBFY feature name. Avoid switching between admin panel, backend, CMS panel, and Backoffice for the same concept.

## Accuracy rules

- Never document planned behavior as released behavior.
- Mark preview/beta functionality explicitly.
- Document security and permission boundaries, not only happy paths.
- Configuration examples must match real option names and defaults.
- Supported-version claims must match package metadata and CI coverage.
- Remove stale screenshots when UI behavior changes.

## Definition of done

A user-visible feature is not release-complete until its documentation is updated. The release PR should include the affected feature guide, screenshots when the UI changed, configuration/permission updates, troubleshooting notes when relevant, and release notes for material customer-facing changes.
