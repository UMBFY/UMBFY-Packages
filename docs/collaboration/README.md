# UMBFY Collaboration

Realtime collaboration and editing awareness for Umbraco Backoffice teams.

UMBFY Collaboration helps editors understand who is online, who is viewing or editing the same resource, and when relevant content changes occur. Its purpose is awareness and conflict prevention without bypassing normal Umbraco permissions.

## Who it is for

- Editorial teams working in the Backoffice at the same time
- Agencies with multiple editors and administrators
- Load-balanced Umbraco installations that need shared presence state
- Teams that want fewer accidental editing conflicts

## Supported versions

- Umbraco CMS 17.x
- Umbraco CMS 18.x
- NuGet dependency range: `[17.0.0,19.0.0)`

## Installation

```bash
dotnet add package UMBFY.Umbraco.Collaboration
```

Consumers do not need Node.js.

See [Installation](installation.md) and [Quick Start](quick-start.md).

## Core features

### Online presence

Shows active Backoffice users with privacy-aware display information.

### Resource presence

Shows when another authorized editor is currently on the same content or media resource.

### Editing awareness

Surfaces editing state so users can see when concurrent work may conflict.

### Change notifications

Relevant changes can be surfaced to active collaborators without exposing resource information to users who do not have permission to see it.

### Conflict prevention

The package provides awareness signals intended to reduce accidental concurrent edits. It does not replace Umbraco authorization or content-versioning behavior.

### Multi-node support

Single-node installations use local in-memory presence. Load-balanced installations can use Redis-backed distributed presence so multiple nodes share collaboration state.

## Configuration

Single-node is the default:

```json
{
  "UMBFY": {
    "Collaboration": {
      "Distributed": {
        "Enabled": false
      }
    }
  }
}
```

For multi-node environments, enable distributed mode and configure the Redis connection name and key prefix. Do not commit Redis secrets to source control.

Privacy settings control whether resource names and editing state are shown. These settings never bypass Umbraco permissions.

See [Configuration](configuration.md) and [Load-Balanced Setup](load-balanced-setup.md).

## Security and privacy

- Backoffice authorization remains authoritative.
- Resource presence is scoped to users allowed to browse the resource.
- Client-supplied identity is not trusted as authority.
- Presence is ephemeral awareness data, not a long-term activity history.
- Public DTOs should not expose connection IDs, claims, email addresses, IP addresses, Redis internals, or content property values.

## Documentation

### Start here

- [Installation](installation.md)
- [Quick Start](quick-start.md)
- [Configuration](configuration.md)

### Feature guides

- [Presence](presence.md)
- [Editing Awareness](editing-awareness.md)
- [Load-Balanced Setup](load-balanced-setup.md)

### Help

- [Troubleshooting](troubleshooting.md)
- [FAQ](faq.md)

## Documentation status

User-facing collaboration flows should be documented with real Backoffice screenshots showing online presence, same-resource presence, editing awareness, notification states, and representative multi-user scenarios. Load-balanced setup guidance must include a verified configuration example and diagnostics for Redis/connectivity problems.

## Support

Use the UMBFY Packages issue forms for bugs, compatibility reports, feature requests, and support. Never post passwords, Redis connection strings, API keys, license keys, or other secrets in public issues.
