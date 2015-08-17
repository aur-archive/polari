# Maintainer: Kai Korla <balticer[at]balticer[dot]de>
pkgname=polari
pkgver=3.11.2
pkgrel=2
pkgdesc="Internet Relay Chat (IRC) client designed for GNOME 3."
url="https://wiki.gnome.org/Apps/Polari"
arch=('x86_64' 'i686')
license=('GPLv2')
depends=('gjs')
optdepends=()
makedepends=('gnome-common' 'intltool')
conflicts=()
replaces=()
backup=()
install='polari.install'
source=("https://git.gnome.org/browse/polari/snapshot/${pkgname}-${pkgver}.tar.gz")
md5sums=('fc59fff82251f07083018df7dcd6b85b')

build() {
      cd "${srcdir}/${pkgname}-${pkgver}"
      ./autogen.sh --prefix=/usr
      make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
  install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
