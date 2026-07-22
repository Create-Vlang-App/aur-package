# create-vlang-app — AUR package

AUR package for [create-vlang-app](https://github.com/Create-Vlang-App/create-vlang-app).

Primary install path for V developers is **VPM**:

```bash
v install create-vlang-app
```

AUR is a secondary channel for Arch Linux users.

## Install (Arch Linux)

```bash
# using yay
yay -S create-vlang-app

# using paru
paru -S create-vlang-app
```

## Manual build

```bash
git clone https://github.com/Create-Vlang-App/aur-package.git
cd aur-package
makepkg -si
```

## Automation

The [`create-vlang-app` publish-aur workflow](https://github.com/Create-Vlang-App/create-vlang-app/blob/main/.github/workflows/publish-aur.yml)
bumps `pkgver` / checksums after each GitHub Release tag `create-vlang-app@X.Y.Z` and
pushes to [aur.archlinux.org](https://aur.archlinux.org/packages/create-vlang-app).

## Source

- AUR: https://aur.archlinux.org/packages/create-vlang-app
- GitHub CLI: https://github.com/Create-Vlang-App/create-vlang-app
- VPM: `v install create-vlang-app`

## Contributors

<a href="https://github.com/Create-Vlang-App/aur-package/contributors">
  <img src="https://contrib.rocks/image?repo=Create-Vlang-App/aur-package"/>
</a>

Made with [contributors-img](https://contrib.rocks).
