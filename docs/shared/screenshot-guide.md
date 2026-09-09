# UMBFY Screenshot Guide

Screenshots are part of the product documentation and should be reproducible, current, and useful rather than decorative.

## Capture source

Use a controlled UMBFY demo Umbraco installation with stable sample content. Keep the same representative content tree and Media library between releases where possible so visual changes are easy to compare.

## Required screenshots

For each user-visible feature, capture the important states customers need to understand:

- Entry point / where the feature is located
- Normal populated state
- Empty state when meaningful
- Warning / validation state
- Confirmation / blocked state where applicable
- Success or refreshed state when it materially helps the workflow
- Configuration UI when the package provides Backoffice configuration

## Naming

Use descriptive paths and filenames, for example:

```text
assets/content-guard/where-used/workspace.png
assets/content-guard/where-used/results.png
assets/content-guard/safe-delete/confirmation.png
assets/collaboration/presence/resource-presence.png
assets/media-order/sorting/upload-date-desc.png
```

Avoid names such as `Screenshot1.png`, `image2.png`, or `final-final.png`.

## Quality rules

- Capture the full relevant Backoffice context, not an unexplained crop.
- Do not expose real customer names, email addresses, domains, secrets, IDs, or confidential content.
- Keep browser zoom and viewport consistent.
- Prefer current supported Umbraco UI over mockups.
- Re-capture screenshots when layout, labels, icons, states, or workflows materially change.
- Add annotations only when they make a workflow substantially clearer.

## Release rule

A release with a user-visible UI change must either update the affected screenshots or explicitly confirm that existing screenshots are still accurate.
