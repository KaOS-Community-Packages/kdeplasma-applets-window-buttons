pkgname=kdeplasma-applets-window-buttons
_pkgname=applet-window-buttons
pkgver=0.8.1
pkgrel=1
pkgdesc="Plasma 5 applet in order to show window buttons in your panels"
arch=(x86_64)
url="https://github.com/psifidotos/applet-window-buttons"
license=('GPL2')
makedepends=(extra-cmake-modules)
source=("https://github.com/psifidotos/${_pkgname}/archive/${pkgver}.tar.gz")
md5sums=('24ec39e8991562cf5ca9bad6c693b5b9')

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
