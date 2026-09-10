# CompilePilot Companion

Signed and notarized builds of **CompilePilot Companion**, the menu bar app that connects
[CompilePilot](https://compilepilot-app.web.app) on your iPhone or iPad to Xcode on your
Mac. The source code is not in this repository.

## Install

Download the DMG from the [latest release](https://github.com/compilepilot/companion/releases/latest),
open it, and drag **CompilePilot Companion** to Applications.

Requires an Apple silicon Mac running macOS 14 Sonoma or later, with Xcode.

## Updates

The Companion keeps itself up to date. Each release publishes an EdDSA-signed
`appcast.xml`, and the app installs an update only if that signature matches the key
built into it.

## Support

[compilepilot-app.web.app/support](https://compilepilot-app.web.app/support)
