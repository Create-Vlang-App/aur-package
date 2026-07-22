# Maintainer: Ulises Jeremias <ulisescf.24@gmail.com>
pkgname=create-vlang-app
pkgver=0.1.0
pkgrel=1
pkgdesc="V-native scaffolding CLI for the V programming language"
arch=('x86_64' 'aarch64')
url="https://github.com/Create-Vlang-App/create-vlang-app"
license=('MIT')
depends=('git')
# Build requires the V compiler from https://github.com/vlang/v (official bootstrap /
# vlang/setup-v). Do NOT use the AUR `vlang` package — it is outdated and unused in CI.
# GitHub tag archive for create-vlang-app@0.1.0
_tag="create-vlang-app@${pkgver}"
_srcdir="create-vlang-app-create-vlang-app-${pkgver}"
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/Create-Vlang-App/create-vlang-app/archive/refs/tags/${_tag}.tar.gz")
sha256sums=('f7c1f62f8eab3bcd4e55b05700924c864f182247ff7c050c39884f5013592729')

prepare() {
  cd "${_srcdir}"
  mkdir -p .vmodules
  ln -sfn "$PWD/modules/create_vlang_app_core" .vmodules/create_vlang_app_core
}

build() {
  cd "${_srcdir}/modules/create_vlang_app"
  VMODULES="$PWD/../../.vmodules" v -prod -o create-vlang-app .
}

package() {
  cd "${_srcdir}/modules/create_vlang_app"
  install -Dm755 create-vlang-app "$pkgdir/usr/bin/create-vlang-app"
}
