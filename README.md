# Create Vlang App — AUR package mirror

GitHub mirror of the AUR packages:

| AUR package | Type | Install |
|-------------|------|---------|
| [`create-awesome-vlang-app`](https://aur.archlinux.org/packages/create-awesome-vlang-app) | Source build (`vlang`) | `yay -S create-awesome-vlang-app` |
| [`create-awesome-vlang-app-bin`](https://aur.archlinux.org/packages/create-awesome-vlang-app-bin) | Prebuilt `linux-x86_64` | `yay -S create-awesome-vlang-app-bin` |

Both provide `create-vlang-app` / `create-awesome-vlang-app` and conflict with each other.

Automation: [`publish-aur.yml`](https://github.com/Create-Vlang-App/create-vlang-app/blob/main/.github/workflows/publish-aur.yml) in `create-vlang-app` (GitHub environment `release`).
