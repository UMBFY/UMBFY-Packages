# UMBFY Packages — Issues & Feedback

This repository is the public support and feedback tracker for UMBFY Umbraco packages.

Use it to:

- report reproducible bugs
- request features and improvements
- ask package usage/configuration questions

## Before opening an issue

Please search existing issues first. Include the affected package, exact package version, Umbraco version, environment, and clear reproduction steps where applicable.

Never post passwords, connection strings, API keys, license keys, personal information, customer-sensitive URLs, or other secrets in public issues.

## Supported issue forms

### Bug Report

Use this when a UMBFY package behaves incorrectly or throws an error.

Please include:

- UMBFY package
- exact package version
- Umbraco major and exact version
- .NET version where relevant
- environment/topology
- expected behavior
- actual behavior
- reproduction steps
- sanitized logs/screenshots

### Feature Request

Use this to suggest an improvement to an existing package, a shared UMBFY capability, or a future package idea.

Please focus on the problem/workflow and who benefits, not only on an implementation preference.

### Support / Question

Use this when you need help configuring or using a UMBFY package and are not yet sure you have found a product defect.

## Package identification

Issues are organized by package using labels such as:

- `package: content-guard`
- `package: collaboration`
- `package: media-order`
- `package: ecosystem`
- `package: other`

Package versions are captured as a required issue-form field rather than creating a label for every released version. This keeps the label taxonomy manageable while preserving exact version information for support and regression analysis.

## Umbraco compatibility labels

Issues may be classified with:

- `umbraco: 17`
- `umbraco: 18`

## Issue type labels

- `type: bug`
- `type: feature`
- `type: support`

## Triage status labels

- `status: needs-triage`
- `status: needs-info`
- `status: confirmed`
- `status: in-progress`
- `status: blocked`
- `status: ready-for-release`

## Priority labels

- `priority: critical`
- `priority: high`
- `priority: normal`

Priority is assigned during UMBFY triage. Reporters do not need to choose it.

## Automatic triage

The repository includes an issue-triage workflow that ensures the standard label taxonomy exists and automatically applies package, Umbraco-major, issue-type, and initial triage labels when possible.

## Package support links

Each UMBFY package README and, later, the UMBFY Hub should link users to this repository for issue reporting and feedback.

When the UMBFY Hub is introduced, package name/version and Umbraco version can be pre-filled or attached to the support flow so users have less information to enter manually.

---

Built by **UMBFY** for the Umbraco ecosystem.
