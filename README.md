![Slogan](https://cdn.modrinth.com/data/cached_images/8c6523b4f7db0a49d11f606fc5222efcdc9da1a8.png)

> A lightweight and fully configurable warp plugin for Bukkit/Spigot/Paper — with custom sounds, colors, actionbar support, and live config reloads.

---

> [!NOTE]
> BetterWarpSystem is discontinued. Use [WarpSystem](https://github.com/erikzimmermann/WarpSystem-Code) instead.

## ⚡ Features

- 🧭 **Warps** — set, teleport to, list, and delete named warps with ease
- 💾 **Persistent Storage** — every warp is saved as a YAML file on disk, nothing gets lost
- 🎨 **Fully Configurable** — customize messages, colors, and sounds via `config.yml`
- 🔁 **Live Reloading** — apply config changes at runtime without restarting
- ✅ **Deletion Confirmation** — prevent accidents with a built-in confirmation flow (with TTL)
- 💬 **Flexible Notifications** — choose between chat messages, actionbar alerts, or both

---

## 🕹️ Commands

| Command | Description | Permission |
|:--------|:------------|:----------:|
| `/setwarp <name>` | Set a warp at your location | `warpsystem.setwarp` |
| `/warp <name>` | Teleport to a warp | *(everyone)* |
| `/warps` | List all available warps | *(everyone)* |
| `/delwarp <name>` | Start deletion flow | `warpsystem.delete` |
| `/delwarp confirm <name>` | Confirm deletion within TTL | `warpsystem.delete` |
| `/warpsysreloadconfig` | Reload the config live | `warpsystem.*` |

---

## 🔐 Permissions

| Permission | Description | Default |
|:-----------|:------------|:-------:|
| `warpsystem.setwarp` | Create warps | OP |
| `warpsystem.delete` | Delete warps | OP |
| `warpsystem.*` | Full access | OP |

---

## ⚙️ Configuration

All messages, colors, and sounds are defined in `config.yml`. Key settings:

| Setting | Default | Description |
|:--------|:-------:|:------------|
| `actionbar` | `true` | Show actionbar notifications |
| `message` | `true` | Send chat messages |
| `sound` | `true` | Play sounds on actions |
| `color.primary` | `&7` | Primary text color |
| `color.secondary` | `&a` | Highlight/accent color |
| `warps.folder` | `warplocations` | Folder for warp files |

### 🔊 Sounds
```yaml
sounds:
  success: 'ENTITY_VILLAGER_TRADE'
  fail: 'ENTITY_VILLAGER_NO'
  delete_confirm: 'BLOCK_ANVIL_PLACE'
```

### 🧨 Deletion Confirmation
```yaml
confirmation:
  delete:
    enabled: true
    ttl_seconds: 20
```

### 💬 Messages
```yaml
messages:
  warp-set: '&aSuccessfully set warp "{warp}".'
  warp-deleted: '&aWarp "{warp}" deleted successfully.'
  delete-confirm: '&ePlease confirm: &c/delwarp confirm {warp} &ewithin {seconds}s.'
```

> 💡 **Tip:** Use `&` for color codes — it's more readable than `§`.

---

## 🛠️ Installation

1. Download the `.jar` file
2. Place it in your server's `/plugins` folder
3. Restart your server — config auto-generates ✅
4. Edit `plugins/WarpSysPlugin/config.yml` to your liking
5. Use `/warpsysreloadconfig` to apply changes live

---

## 🔧 Requirements

| | |
|:-|:-|
| **Java** | 21+ |
| **Server** | Spigot / Paper 1.21.x |

---

## 🧩 Troubleshooting

- **Warps not saving?** Make sure the plugin has write access to the `plugins/` folder
- **Sounds not working?** Double-check Bukkit `Sound` enum names — invalid names fall back to defaults

---

## 🔗 Source Code & Contributing

This plugin is **open source** — contributions, bug reports, and feature requests are welcome!

👉 [View on GitHub](https://github.com/larroxtv/BetterWarpSystem) · [Report Issues](https://github.com/larroxtv/BetterWarpSystem/issues)

---

<div align="center">

*Made with ❤️ by Larrox*

</div>
