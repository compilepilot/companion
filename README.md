# CompilePilot Companion

Signed and notarized builds of **CompilePilot Companion**, the free menu bar app that connects
[CompilePilot](https://compilepilot-app.web.app) on your iPhone or iPad to Xcode on your
Mac. The source code is not in this repository.

## What it does

CompilePilot builds, runs, and tests over SSH with nothing installed on the Mac. The
Companion adds what SSH cannot do:

- **Coding agents.** Open Claude Code, Codex or opencode, whichever you have installed, on
  the project you picked. The agent runs on your Mac in a terminal of its own, keeps working
  when you leave the screen, and you answer its permission prompts from the phone. Several
  at once. Send Claude Code its next instruction from Siri or the Apple Watch when it has
  finished its turn, and see a one-line summary of what it said.
- **At a glance.** Siri, widgets and the Apple Watch app ask the Mac how the build is going
  and whether an agent is waiting for you, in one quick answer.
- **Away from home.** If you turn them on, notifications when a build finishes or Claude Code
  is waiting, and a Live Activity with the build's progress, also when your iPhone is not on
  your local network. Each notification is encrypted on the Mac with a key your iPhone
  created, and the CompilePilot service that passes it to Apple cannot read it.
- **Build with Xcode.** Build, run, and test with Xcode itself, not only `xcodebuild`.
- **SwiftUI previews.** Rendered by Xcode on your Mac, shown on your phone.
- **Live Simulator.** Watch the simulator and touch it: gestures, keyboard, and hardware
  buttons, through CoreSimulator, with no Accessibility or Screen Recording permission.
- **Less friction.** Your Mac shows up in the app on its own, builds keep running when you
  leave the screen, and the Mac does not idle-sleep halfway through one.

Building with Xcode, previews, and Xcode's tools for agents need Xcode 26.3 or later, and
are set up once for the whole Mac from the app, with an administrator password on the Mac.

## Install

Download the DMG from the [latest release](https://github.com/compilepilot/companion/releases/latest),
open it, and drag **CompilePilot Companion** to Applications. Then pair it with the app
using the six-digit code it shows. The full guide is at
[compilepilot-app.web.app/companion](https://compilepilot-app.web.app/companion).

Requires an Apple silicon Mac running macOS 14 Sonoma or later, with Xcode.

## Privacy

The Companion talks to the devices you paired, directly, over your local network or your
tailnet. There is no account and no relay. To recognize the same project on two Macs, it
sends those devices a fingerprint of each project's Git remote, never the remote itself. On its own, it connects out to check this
repository for updates and, only if you turn on notifications away from your local network
on your iPhone, to send each notification, encrypted, to the address your iPhone gave it. An
agent you open talks to its own provider, with your account, as it does when you use it on
the Mac.

## Updates

The Companion keeps itself up to date. Each release publishes an EdDSA-signed
`appcast.xml`, and the app installs an update only if that signature matches the key
built into it.

## Support

[compilepilot-app.web.app/support](https://compilepilot-app.web.app/support)

Claude Code, Codex and opencode belong to their respective owners. CompilePilot is not
affiliated with them, or with Apple.
