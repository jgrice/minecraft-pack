# Create Server mod pack

The mod list for the "create" Minecraft server (1.21.1, NeoForge 21.1.267), as a
[packwiz](https://packwiz.infra.link/) pack. The server and every player's Prism Launcher
instance install from the same pack, so they always match. This repo only lists mods and
where to download them; it holds no mod files, worlds or settings.

Pack URL: https://jgrice.github.io/minecraft-pack/pack.toml

## Players (Prism Launcher)

Import the instance from the latest release (`Create-Server.zip`): Add Instance, Import,
pick the zip. Every time you press Play it checks this pack and updates your mods first.
JourneyMap and Xaero's Minimap are optional; you're asked on first launch.

## Updating the pack

```bash
packwiz modrinth add --project-id <slug> --version-id <id>    # or: packwiz update <mod>
packwiz refresh
git commit -am "..." && git push
```

The server picks up the change on its next restart; players on their next launch.

## Prism instance

`prism/` holds the instance files for the release zip. Rebuild the zip with those two files plus
`.minecraft/packwiz-installer-bootstrap.jar` (v0.0.3 from packwiz/packwiz-installer-bootstrap).
Bump the NeoForge version in `prism/mmc-pack.json` when `pack.toml` changes it.
