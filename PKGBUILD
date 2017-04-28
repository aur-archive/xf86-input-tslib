# Maintainer: Christian Hesse <mail@eworm.de>

pkgname=xf86-input-tslib
pkgver=0.0.7
pkgrel=1
pkgdesc="X.org tslib input driver"
arch=(arm i686 x86_64)
license=('custom')
url="http://xorg.freedesktop.org/"
depends=('glibc')
makedepends=('xorg-server')
options=('!libtool')
groups=('xorg-drivers' 'xorg')
backup=("etc/ts.conf")
source=("https://github.com/merge/${pkgname}/releases/download/${pkgver}/${pkgname}-${pkgver}.tar.bz2")

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
  make DESTDIR="${pkgdir}" install
  install -D -m644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/COPYING"
}
sha256sums=('6f23cc9702b0ae16086d364b275335c094efbf6acde57f8a030e4db5b9aece03')
