# Maintainer: Ilya Medvedev <medved55rus [at] gmail [dot] com>

pkgname=urtconnector
pkgver=0.9.0
pkgrel=1
pkgdesc="Advanced UrbanTerror launcher program. Developed by members of russian clans =Xaoc=, Red*Army and Rus Devils Team. 
This program uses Qt4 and is written in C++."
arch=('i686' 'x86_64')
url="http://code.google.com/p/urtconnector"
license=('GPL')
depends=('qt>=4.6.2' 'phonon' 'sqlite')
makedepends=('pkgconfig' 'cmake>=2.6' 'boost' 'automoc4')
provides=('urtconnector')
conflicts=('urtconnector')
source=("https://urtconnector.googlecode.com/files/${pkgname}-${pkgver}.tar.gz")
md5sums=('fc60afa3c911f77a6d0ad57b44c626cb')

build() {
  cd "${srcdir}/urtconnector/"
  cmake ./ -DCMAKE_INSTALL_PREFIX=/usr
  make
}

package() {
  cd "${srcdir}/urtconnector/"
  make DESTDIR="$pkgdir" install
}