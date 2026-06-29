# eXc Launcher

A custom **Minecraft: Java Edition** launcher for personal and small-community use — built with **Rust + Tauri** and a **Svelte** frontend.

> ⚠️ eXc Launcher is an **unofficial** project. It is not affiliated with, endorsed by, or associated with Mojang or Microsoft. "Minecraft" is a trademark of Mojang Synergies AB.

## What it does

- Sign in with your **own Microsoft account** to play the Minecraft you legitimately own.
- Manage game instances: **Vanilla, Fabric, Forge, NeoForge, Quilt**.
- Pick a version and launch the game.
- A small, fast native app (Windows / macOS / Linux).

## Authentication & security

eXc Launcher takes account security seriously:

- Authentication uses **exclusively Microsoft's official OAuth2 device code flow** (`consumers` endpoint, `XboxLive.signin` scope).
- The launcher **never asks for, sees, or stores your password**.
- Refresh tokens are stored **only** in the operating system's secure credential store (Windows Credential Manager) and are **never logged, transmitted, or shared** with any third party.
- **No user data is collected** or sent to any server we control.
- The app only talks to the **official** Microsoft and Minecraft service endpoints.

## Tech stack

- **Backend:** Rust + Tauri 2 (game launching, authentication, instance management)
- **Frontend:** Svelte (UI)
- **Token storage:** OS keychain via `keyring`

## Status

Active development. Microsoft login is implemented via the official device code flow; this application is currently going through Mojang's Java Edition Game Service API approval process.

## Contact

Maintainer: Pascal Wölm — wolmpascal@gmail.com
