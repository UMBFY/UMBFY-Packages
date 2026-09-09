# UMBFY Content Guard

Protect Umbraco content relationships before they break.

UMBFY Content Guard gives editors and administrators dependency intelligence directly in the Umbraco Backoffice. It helps teams understand where content is referenced, prevent unsafe deletion and publishing, monitor content health, validate multilingual relationships, and assess downstream impact.

## Who it is for

- Editors who need confidence before changing, unpublishing, or deleting content
- Administrators responsible for content integrity across large sites
- Agencies managing complex Umbraco implementations with many references
- Multilingual teams that need culture-aware dependency validation
- Developers who want dependency information without repeatedly scanning the full content tree

## Supported versions

- Umbraco CMS 17.x
- Umbraco CMS 18.x
- Package dependency range: `[17.0.0, 19.0.0)`

## Installation

```bash
dotnet add package UMBFY.Umbraco.ContentGuard
```

After first installation, Content Guard creates its dependency-index storage and bootstraps existing content automatically. Existing content does not need to be manually re-saved.

See [Installation](installation.md) and [Quick Start](quick-start.md).

## Core features

### Where Used

Shows which content or media items reference the current item, including source name, property context, path, culture/segment, state, and authorization-aware navigation.

### Safe Delete

Protects referenced content and media from accidental deletion. Supported policies are Warn, Require Confirmation, and Block. Safety decisions fail closed when the dependency index is incomplete or unhealthy.

### Publish Guard

Detects unhealthy dependencies before publishing, including missing, trashed, unpublished, and culture-specific dependency problems.

### Content Health

Provides a centralized view of dependency integrity with status, metrics, paging, filters, and explicit index-health states.

### Multilingual Validation

Validates references across cultures and language fallback behavior, including missing or unpublished cultures and unavailable fallback targets.

### Dependency Impact

Shows inbound and outbound relationships, bounded dependency depth, and risk classification so editors can understand the likely effect of a change before making it.

### Existing-site bootstrap

Builds a durable dependency index for existing content on first install, so the package works on populated sites without requiring a manual re-save campaign.

### Realtime refresh

Where Used, Impact, Content Health, and guard dialogs can refresh after relevant index mutations. Management APIs remain authoritative; realtime delivery is a UX synchronization layer only.

## Supported reference types

- Content Picker
- Media references
- Multi URL Picker internal links
- Rich Text Editor internal links
- Supported nested references inside Block Grid / Block List structures
- Culture-specific reference values

External URLs are not treated as internal content dependencies. Third-party custom property editors require explicit scanner support.

## Security and permissions

Content Guard respects Umbraco Backoffice permissions. Restricted dependencies may still affect risk and guard decisions without exposing restricted names or details to unauthorized users.

## Configuration

Key configuration areas include:

- Package enable/disable
- Safe Delete policy and confirmation lifetime
- Publish Guard policy and confirmation lifetime
- Visible-result limits
- Multilingual validation and language fallback behavior

See [Configuration](configuration.md).

## Operations

The durable dependency index powers Where Used, Safe Delete, Publish Guard, Content Health, and Impact. Important operational states include Initializing, Rebuilding, Ready, and Unhealthy. When completeness matters, an incomplete index must never be reported as safe or healthy.

See [Rebuild Index](rebuild-index.md) and [Troubleshooting](troubleshooting.md).

## Documentation

### Start here

- [Installation](installation.md)
- [Quick Start](quick-start.md)
- [Configuration](configuration.md)

### Feature guides

- [Where Used](where-used.md)
- [Safe Delete](safe-delete.md)
- [Publish Guard](publish-guard.md)
- [Content Health](content-health.md)
- [Multilingual Validation](multilingual-validation.md)
- [Impact](impact.md)

### Operations and help

- [Rebuild Index](rebuild-index.md)
- [Troubleshooting](troubleshooting.md)
- [FAQ](faq.md)
- [Tutorials](tutorials/README.md)

## Documentation status

The package documentation should include real Umbraco Backoffice screenshots, step-by-step workflows, configuration examples, permissions behavior, troubleshooting guidance, and release-specific upgrade notes. Screenshot and documentation quality are part of the package release definition of done.

## Support

Use the issue forms in the UMBFY Packages repository for bugs, feature requests, and support. Never include passwords, connection strings, API keys, license keys, or other secrets in public issues.
