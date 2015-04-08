pkgname=translate-shell
pkgver=0.8.23
pkgrel=1
pkgdesc="Google Translate to serve as a command line tool"
arch=('x86_64')
url="http://www.soimort.org/translate-shell/"
license=('Public Domain')
provides=('google-translate-cli-git')
replaces=('google-translate-cli-git')
conflicts=('google-translate-cli-git')
depends=('gawk' 'bash' 'fribidi' 'groff')
optdepends=('rlwrap: A readline wrapper with history')
source=("https://github.com/soimort/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('f7fa96b113fb23e2cb1f0dd331882db3')

package() {
	cd ${pkgname}-${pkgver}
	install -d "${pkgdir}/usr/bin"
	make install INSTDIR="${pkgdir}/usr/bin"
	install -d "${pkgdir}/usr/share/licenses/${pkgname}"
	install -Dm644 "LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
