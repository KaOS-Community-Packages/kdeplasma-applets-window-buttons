pkgname=kdeplasma-applets-window-buttons
_pkgname=applet-window-buttons
pkgver=0.3
pkgrel=1
pkgdesc="Plasma 5 applet in order to show window buttons in your panels"
arch=(x86_64)
url="https://github.com/psifidotos/applet-window-buttons"
license=('GPL2')
makedepends=(extra-cmake-modules)
source=("https://github.com/psifidotos/${_pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('be215b66fc0aaf700c2a51807bdb8f13')

prepare() {
  mkdir -p ${_pkgname}-${pkgver}/build
}

build() {
  cd ${_pkgname}-${pkgver}/build
  cmake .. \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -Wnodev
  make
}

package() {
  cd ${_pkgname}-${pkgver}/build
  make DESTDIR="$pkgdir" install
}
