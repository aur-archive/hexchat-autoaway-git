# Maintainer: Andrey Vihrov <andrey.vihrov at gmail.com>

pkgname=hexchat-autoaway-git
_gitname=hexchat-autoaway
pkgver=0.16.168aeae
pkgrel=1
pkgdesc="A HexChat plugin to set away on idle"
arch=('i686' 'x86_64')
url="https://github.com/andreyv/hexchat-autoaway"
license=('GPL3')
depends=('hexchat' 'libx11' 'libxss')
makedepends=('git')
source=('git+https://github.com/andreyv/hexchat-autoaway.git')
sha256sums=('SKIP')

pkgver() {
  cd "$_gitname"
  echo "0.$(git rev-list --count HEAD).$(git describe --always)"
}

build() {
  cd "$_gitname"
  make
}

package() {
  cd "$_gitname"
  install -D autoaway.so "$pkgdir/usr/lib/hexchat/plugins/autoaway.so"
}

# vim:set ts=2 sw=2 et:
