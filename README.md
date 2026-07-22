# create-vlang-app — AUR package

[![Discord](https://img.shields.io/discord/1527933660764831825?label=Discord&logo=discord&logoColor=white)](https://discord.gg/dwFTsR7fK2)

Arch Linux packaging for [create-vlang-app](https://github.com/Create-Vlang-App/create-vlang-app).

Pinned to tag [`create-vlang-app@0.1.0`](https://github.com/Create-Vlang-App/create-vlang-app/releases/tag/create-vlang-app%400.1.0).

## Install

```bash
yay -S create-vlang-app
# or
paru -S create-vlang-app
```

## Manual build

Requires the **official V toolchain** (not the AUR `vlang` package — it is outdated).
Same pin as CI: [`.v-version`](.v-version) via [`vlang/setup-v`](https://github.com/vlang/setup-v) or https://github.com/vlang/v.

```bash
# Example: bootstrap V 0.5.2, then build the package
git clone --depth 1 --branch 0.5.2 https://github.com/vlang/v ~/v && make -C ~/v
export PATH="$HOME/v:$PATH"

git clone https://github.com/Create-Vlang-App/aur-package.git
cd aur-package
makepkg -d -si   # -d: skip pacman deps; V is already on PATH
```

## Other channels

| Channel | How |
|---------|-----|
| GitHub Release | [linux amd64 binary](https://github.com/Create-Vlang-App/create-vlang-app/releases/tag/create-vlang-app%400.1.0) |
| Homebrew | `brew tap Create-Vlang-App/tap && brew install create-vlang-app` |
| Source | Build from [create-vlang-app](https://github.com/Create-Vlang-App/create-vlang-app) |

## Automation

[`publish-aur.yml`](https://github.com/Create-Vlang-App/create-vlang-app/blob/main/.github/workflows/publish-aur.yml) retargets this PKGBUILD after each `create-vlang-app@X.Y.Z` Release.

## Links

- AUR: https://aur.archlinux.org/packages/create-vlang-app
- CLI: https://github.com/Create-Vlang-App/create-vlang-app
- Templates: https://github.com/Create-Vlang-App/cva-templates

## Contributors

<a href="https://github.com/Create-Vlang-App/aur-package/contributors">
  <img src="https://contrib.rocks/image?repo=Create-Vlang-App/aur-package" alt="contrib.rocks"/>
</a>
