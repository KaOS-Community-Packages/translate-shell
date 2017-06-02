pkgname=translate-shell
pkgver=0.9.6.4
pkgrel=1
pkgdesc="Google Translate to serve as a command line tool"
arch=('x86_64')
url="http://www.soimort.org/translate-shell/"
license=('Public Domain')
depends=('gawk' 'bash' 'fribidi' 'groff')
optdepends=('rlwrap: A readline wrapper with history')
source=("https://github.com/soimort/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('23f8aecf6eb48276639c24f932807803')

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
