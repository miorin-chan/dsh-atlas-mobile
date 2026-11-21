# Mobile Atlas

[简体中文](README.zh.md)

Install two mobile Web enhancements on one Plugins card.
Each row has its own switch.

- [Left-edge swipe](../dsh-swipe-back/README.en.md) uses a rightward swipe from the left edge at phone widths.
  In a Home Screen app or a tab without browser history, it dismisses the open surface or opens the session drawer.
  An open drawer can be swiped away in either direction, including in a regular tab.
- [iOS top clearance](../dsh-ios-top-clearance/README.md) insets the frame in the iOS Home Screen app at phone widths.

Use the `web` profile when launching through `dsh-mobile`.

## Install

Requires DeepSeek Harness 0.2.2-rc.3 or newer with the Web client.

1. Run `pnpm install` in this directory to resolve the linked source packages.
2. If any source bundle is installed independently in the target profile, record its switch state and remove the bundle.
   Both forms use the same row IDs, so merely turning off a row leaves the duplicate ID in place.
3. In **Plugins → Add plugin**, select this directory.
   Check that its card has two rows and restore their switch states.

[Project documentation](docs/README.md)
