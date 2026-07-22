# create-vlang-app — AUR package

Arch Linux packaging for [create-vlang-app](https://github.com/Create-Vlang-App/create-vlang-app).

Pinned to tag [`create-vlang-app@0.1.0`](https://github.com/Create-Vlang-App/create-vlang-app/releases/tag/create-vlang-app%400.1.0).

## Install

```bash
yay -S create-vlang-app
# or
paru -S create-vlang-app
```

## Manual build

```bash
git clone https://github.com/Create-Vlang-App/aur-package.git
cd aur-package
makepkg -si
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
