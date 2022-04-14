# Maintainer: Stefan Tatschner <stefan@rumpelsepp.org>

pkgname=poweralertd
pkgver=0.2.0
pkgrel=3
pkgdesc='UPower-powered power alerter '
url=https://git.sr.ht/~kennylevinsen/poweralertd
arch=(x86_64 aarch64)
license=(GPL3)
depends=(systemd-libs upower)
makedepends=(scdoc meson)
_commit="3c0c7c727db9c7fc03e790946541e2b2d0146cd2"
source=(
  "${pkgname}-${pkgver}::https://git.sr.ht/~kennylevinsen/poweralertd/archive/$_commit.tar.gz"
)
sha256sums=('SKIP')

build () {
	cd "${pkgname}-${_commit}"
	arch-meson build
	ninja -C build
}

package () {
	cd "${pkgname}-${_commit}"
	DESTDIR="${pkgdir}" ninja -C build install
}
