# Create Vlang App — AUR package mirror

GitHub mirror of the AUR packages:

| AUR package | Type | Install |
|-------------|------|---------|
| [`create-awesome-vlang-app`](https://aur.archlinux.org/packages/create-awesome-vlang-app) | Source build (`vlang`) | `yay -S create-awesome-vlang-app` |
| [`create-awesome-vlang-app-bin`](https://aur.archlinux.org/packages/create-awesome-vlang-app-bin) | Prebuilt `linux-x86_64` | `yay -S create-awesome-vlang-app-bin` |

Both provide `create-vlang-app` / `create-awesome-vlang-app` and conflict with each other.

## Install

With [yay](https://github.com/Jguer/yay):

```bash
yay -S create-awesome-vlang-app      # source build (needs vlang toolchain)
yay -S create-awesome-vlang-app-bin  # prebuilt linux-x86_64 binary (faster)
```

With [paru](https://github.com/Morganamilo/paru):

```bash
paru -S create-awesome-vlang-app
paru -S create-awesome-vlang-app-bin
```

Pick **one**: the two packages conflict. Prefer `-bin` unless you want to build from source (requires `base-devel`, `git`, and `vlang`).

Alternatives: the [website installer](https://create-awesome-vlang-app.vercel.app) (`install.sh`) or a [GitHub Release](https://github.com/Create-Vlang-App/create-vlang-app/releases) binary.

## Version sync

`pkgver` in each `PKGBUILD` tracks the [`create-vlang-app@X.Y.Z`](https://github.com/Create-Vlang-App/create-vlang-app/releases) GitHub Release tags. This mirror is updated automatically by [`publish-aur.yml`](https://github.com/Create-Vlang-App/create-vlang-app/blob/main/.github/workflows/publish-aur.yml) in `create-vlang-app` (GitHub environment `release`), so a new CLI release usually lands here within minutes. If `yay -Syu` shows an older version than the latest GitHub Release, the sync workflow is still running — check its [runs](https://github.com/Create-Vlang-App/create-vlang-app/actions/workflows/publish-aur.yml).

## Troubleshooting

- `target not found`: refresh your helper (`yay -Syu`) or install the AUR helper itself first; these packages live in the AUR, not the official repos.
- `conflicting packages`: you have both variants installed — remove one (`yay -Rns create-awesome-vlang-app` or `...-bin`).
- Source build fails (`vlang` errors): install the toolchain (`sudo pacman -S --needed base-devel git` plus `vlang`) or switch to the `-bin` package.
- `makepkg` checksum errors: delete the cached sources (`~/.cache/yay/<pkg>`) and retry; persistent mismatches mean the mirror is mid-sync (see above).
- Still stuck: ask on [Discord](https://discord.gg/bR5VyATgka) or search the [CLI issues](https://github.com/Create-Vlang-App/create-vlang-app/issues).

Automation: [`publish-aur.yml`](https://github.com/Create-Vlang-App/create-vlang-app/blob/main/.github/workflows/publish-aur.yml) in `create-vlang-app` (GitHub environment `release`).
