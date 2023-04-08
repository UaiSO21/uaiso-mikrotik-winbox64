# Maintainer: Alexander Bruegmann <mail[at]abruegmann[dot]eu>
# Contributor: Tom Hetmer <tom.hetmer / outlook.cz>
# Contributor: Daniel Milde <daniel / milde.cz>

pkgname=uaiso-mikrotik-winbox64
_pkgname=winbox64
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
install=${_pkgname}.install
source=("${_pkgname}-${pkgver}.exe::http://download.mikrotik.com/winbox/${pkgver}/${_pkgname}.exe"
        "${_pkgname}.desktop"
        "${_pkgname}.png"
        "${_pkgname}")

package() {
  install -Dm755 "${srcdir}/${_pkgname}-${pkgver}.exe" "${pkgdir}/opt/${_pkgname}/${_pkgname}.exe"
  install -Dm755 "${srcdir}/${_pkgname}" "${pkgdir}/usr/bin/${_pkgname}"
  install -Dm655 "${srcdir}/${_pkgname}.png" "${pkgdir}/usr/share/pixmaps/${_pkgname}.png"
  install -Dm655 "${srcdir}/${_pkgname}.desktop" "${pkgdir}/usr/share/applications/${_pkgname}.desktop"
}
