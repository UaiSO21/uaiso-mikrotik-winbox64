# Maintainer: Alexander Bruegmann <mail[at]abruegmann[dot]eu>
# Contributor: Tom Hetmer <tom.hetmer / outlook.cz>
# Contributor: Daniel Milde <daniel / milde.cz>

pkgname=winbox64
pkgver=3.37
pkgrel=1
pkgdesc="Mikrotik RouterOS GUI Configurator. 64-bit version for use with wine"
url="http://www.mikrotik.com"
arch=('x86_64')
license=('custom')
depends=('wine')
makedepends=('xdg-utils')
optdepends=(
  'ttf-ms-fonts: for better fonts'
)
install=${pkgname}.install
source=("${pkgname}-${pkgver}.exe::http://download.mikrotik.com/winbox/${pkgver}/${pkgname}.exe"
        "${pkgname}.desktop"
        "${pkgname}.png"
        "${pkgname}")
sha256sums=('SKIP')

package() {
  install -Dm755 "${srcdir}/${pkgname}-${pkgver}.exe" "${pkgdir}/opt/${pkgname}/${pkgname}.exe"
  install -Dm755 "${srcdir}/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
  install -Dm655 "${srcdir}/${pkgname}.png" "${pkgdir}/usr/share/pixmaps/${pkgname}.png"
  install -Dm655 "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications/${pkgname}.desktop"
}
