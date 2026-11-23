# Mobile Modular Improvement Plan

[简体中文](README.zh.md)

Two independently switchable improvements for DSH on phones.

- [Left-edge swipe](../dsh-swipe-back/README.en.md) goes back or opens the session drawer
  in a Home Screen app or a tab with no history.
  Swipe either way to close an open drawer, including in a regular tab.
- [iOS top clearance](../dsh-ios-top-clearance/README.md) adds space above the interface in the iOS Home Screen app.

## Install

Requires the Web client on DeepSeek Harness `0.2.2-rc.3` or later.
With `dsh-mobile`, use the `web` profile.

1. Run `pnpm install` in this directory.
2. If any included plugin is installed separately in this profile, note its switch state
   and remove its bundle to avoid duplicate plugin IDs.
3. In **Plugins → Add plugin**, select this directory.
   Restore any saved switch states on the new card.

[Maintenance and verification](docs/README.md)
