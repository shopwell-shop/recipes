# Shopwell repository rules

This repository is the independently maintained Shopwell Flex recipe catalog.

- Preserve UTF-8 and existing user changes.
- Shopwell-owned code uses the Apache License 2.0 (`Apache-2.0`); root `LICENSE` contains the standard text.
- Preserve every upstream legal text verbatim in root `NOTICE`.
- Outside `NOTICE`, do not reintroduce Shopware branding, package names, repositories, images, or Actions.
- Runtime workflows may use only registered Shopwell forks and normal public registries.
- Do not merge or cherry-pick unrelated upstream history, copy upstream tags, or force-push.
- Before commit, push, release, or sync completion, run:
  `../sync-upstream/bin/syncctl audit-license recipes` and
  `../sync-upstream/bin/syncctl audit-upstream-dependencies recipes`.
- A failed audit blocks completion.
