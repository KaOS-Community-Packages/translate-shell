pkgname=translate-shell
pkgver=0.9.3.1
pkgrel=1
pkgdesc="Google Translate to serve as a command line tool"
arch=('x86_64')
url="http://www.soimort.org/translate-shell/"
license=('Public Domain')
depends=('gawk' 'bash' 'fribidi' 'groff')
optdepends=('rlwrap: A readline wrapper with history')
source=("https://github.com/soimort/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('91b3f5a9ef78d3e4c8f1f5eaa1bc92a4')

build() {
	cd ${pkgname}-${pkgver}
	make release
}

package() {
	cd ${pkgname}-${pkgver}
	install -d "${pkgdir}/usr/bin"
	install -d "${pkgdir}/usr/share/man/man1"
	make install PREFIX="${pkgdir}/usr"
	install -d "${pkgdir}/usr/share/licenses/${pkgname}"
	install -Dm644 "LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
