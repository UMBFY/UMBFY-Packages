# UMBFY Media Order

Improve Umbraco Media-library sorting and upload workflows without replacing the native Media experience.

UMBFY Media Order extends the native Umbraco Media collection with practical server-side sorting options and predictable post-upload ordering so editors can find recently uploaded assets quickly.

## Who it is for

- Editors managing large Media libraries
- Agencies that want a better native Media workflow without replacing Umbraco Media
- Teams that need consistent newest-first behavior after uploads
- Sites where file-size sorting is useful for operational cleanup and asset management

## Supported versions

- Umbraco CMS 17.x
- Umbraco CMS 18.x
- NuGet dependency range: `[17.0.0,19.0.0)`

## Installation

```bash
dotnet add package UMBFY.Umbraco.MediaOrder
```

Consumers do not need Node.js.

See [Installation](installation.md) and [Quick Start](quick-start.md).

## Core features

### Upload Date sorting

Sort Media by creation/upload date. The default behavior is newest first, making recent uploads immediately visible.

### Name sorting

Sort Media alphabetically by name in ascending or descending order.

### File Size sorting

Sort Media by `umbracoBytes` so larger or smaller assets can be surfaced quickly.

### Post-upload behavior

After an upload, the Media listing returns to Upload Date descending so newly uploaded items appear first instead of being hidden elsewhere in the current sort order.

### Remembered editor preference

The package can remember a user's selected sort field and direction in namespaced local storage.

### Native collection integration

Sorting applies to the native `Umb.Collection.Media` experience and uses server-side collection ordering rather than replacing the entire Media library UI.

## Default sort fields

| Display name | Field | Default direction |
| --- | --- | --- |
| Name | `name` | Ascending |
| Upload Date | `createDate` | Descending |
| File Size | `umbracoBytes` | Descending |

Changing sort resets pagination to the first page.

## Configuration

```json
{
  "UMBFY": {
    "MediaOrder": {
      "DefaultSortField": "createDate",
      "DefaultSortDirection": "desc",
      "RememberUserChoice": true,
      "MaxPageSize": 100
    }
  }
}
```

| Setting | Default | Purpose |
| --- | --- | --- |
| `DefaultSortField` | `createDate` | Initial sort field |
| `DefaultSortDirection` | `desc` | Initial sort direction |
| `RememberUserChoice` | `true` | Persist the editor's preference |
| `MaxPageSize` | `100` | Upper bound for package server-side paging behavior |

See [Configuration](configuration.md).

## Known scope

- Sorting targets the native Umbraco Media collection.
- Upload Date and File Size are enabled through package integration rather than by permanently mutating Umbraco Media list-view configuration.
- The package should preserve the surrounding native Backoffice workflow wherever possible.

## Documentation

### Start here

- [Installation](installation.md)
- [Quick Start](quick-start.md)
- [Configuration](configuration.md)

### Feature guides

- [Sorting](sorting.md)
- [Upload Folders](upload-folders.md)

### Help

- [Troubleshooting](troubleshooting.md)
- [FAQ](faq.md)

## Documentation status

The Media Order guide should include real Backoffice screenshots for list and grid views, each sort mode, direction changes, post-upload behavior, and upload-folder behavior. Examples should use a stable demo Media library so screenshots remain comparable between releases.

## Support

Use the UMBFY Packages issue forms for bugs, compatibility reports, feature requests, and support. Never include credentials, connection strings, API keys, license keys, or other secrets in public issues.
