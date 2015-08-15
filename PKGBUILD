# Maintainer: Eugeni Dodonov <eugeni@dodonov.net>
# Contributor: Eugeni Dodonov <eugeni@dodonov.net>

pkgname=fatback
pkgver=1.3
pkgrel=1
pkgdesc="A *nix tool for recovering files from FAT file systems. "
url="http://fatback.sourceforge.net/"
license=('GPL')
arch=('i686' 'x86_64')
depends=()
optdepends=()
source=(http://downloads.sourceforge.net/${pkgname}/${pkgname}-${pkgver}.tar.gz)
install=fatback.install
md5sums=('4f1beb13670a7eff5b66cff84e5fd42a')

build() {
  cd ${srcdir}/${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}
  make DESTDIR="$pkgdir/" install
}
