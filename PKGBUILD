pkgname=libotf
pkgver=0.9.13
pkgrel=1
pkgdesc='A Library for handling OpenType Font'
url='http://www.nongnu.org/m17n/'
license=('LGPL')
arch=('x86_64')
depends=('libxaw' 'freetype2')
source=("http://download.savannah.gnu.org/releases/m17n//${pkgname}-${pkgver}.tar.gz")
sha1sums=('66bb81958f5f07ee1f8917d3cb7e359ae559d873')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	./configure --prefix=/usr --disable-static
	make
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	make DESTDIR="${pkgdir}" install
}
