# Maintainer: Ulises Jeremias <ulisescf.24@gmail.com>
pkgname=create-vlang-app
pkgver=0.0.1
pkgrel=1
pkgdesc="V-native scaffolding CLI for the V programming language"
arch=('x86_64' 'aarch64')
url="https://github.com/Create-Vlang-App/create-vlang-app"
license=('MIT')
depends=('git')
makedepends=('vlang')
# Bootstrap pin until the first tag `create-vlang-app@X.Y.Z` exists.
# `publish-aur.yml` in create-vlang-app retargets this to release tarballs.
_commit=e5c07f5
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/Create-Vlang-App/create-vlang-app/archive/${_commit}.tar.gz")
sha256sums=('2db15ba3f4992eb5dcf1dffbd5a26826e433a77523fb102c6e47d7c3d965d1de')

prepare() {
  cd "create-vlang-app-${_commit}"
  mkdir -p .vmodules
  ln -sfn "$PWD/modules/create_vlang_app_core" .vmodules/create_vlang_app_core
}

build() {
  cd "create-vlang-app-${_commit}/modules/create_vlang_app"
  VMODULES="$PWD/../../.vmodules" v -prod -o create-vlang-app .
}

package() {
  cd "create-vlang-app-${_commit}/modules/create_vlang_app"
  install -Dm755 create-vlang-app "$pkgdir/usr/bin/create-vlang-app"
}
