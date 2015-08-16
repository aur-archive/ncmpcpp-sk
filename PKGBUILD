# Maintainer: sudokode <sudokode@gmail.com>

pkgname=ncmpcpp-sk
pkgver=0.5.8
pkgrel=1
pkgdesc="An almost exact clone of ncmpc with some new features. Includes unicode, clock, outputs, taglib, and curl support."
arch=('i686' 'x86_64')
url="http://unkart.ovh.org/ncmpcpp/"
license=('GPL')
depends=('curl' 'libmpdclient' 'taglib' 'ncurses')
conflicts=('ncmpcpp', 'ncmpcpp-git')
install=ncmpcpp.install
source=(http://unkart.ovh.org/ncmpcpp/ncmpcpp-${pkgver}.tar.bz2)
md5sums=('288952c6b4cf4fa3683f3f83a58da37c')

build() {
  cd "$srcdir/ncmpcpp-${pkgver}"
  ./configure --prefix=/usr \
 	 --enable-unicode \
	 --enable-clock \
	 --enable-outputs \
  	 --with-taglib \
  	 --with-curl
  make
}

package() {
  cd "$srcdir/ncmpcpp-${pkgver}"

  make DESTDIR="$pkgdir" install
}
