# Maintainer: Filma Bem <filmabemtv2@gmail.com>
pkgname=fbpos-defaults
pkgver=22
pkgrel=2
epoch=
pkgdesc="FBP OS Default Settings"
packager=(Filma Bem <filmabemtv2@gmail.com>)
arch=('x86_64')
url="https://github.com/FilmaBem2/fbpos-wallpapers"
license=('MIT')
groups=()
depends=('fbpos-wallpapers')
makedepends=(git)
checkdepends=()
optdepends=()
provides=('fbpos-default-settings')
conflicts=()
replaces=()
backup=()
options=()
changelog=
source=(plasma-desktop.settings)
noextract=()
md5sums=('56e105210966a5173e5ade219fe7737e')
validpgpkeys=()

pkgver() {
	cd "${_pkgname}"
    printf "22" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    mkdir "${pkgdir}/etc"
    mkdir "${pkgdir}/etc/skel"
    mkdir "${pkgdir}/etc/skel/.config"
    mkdir "${pkgdir}/etc/skel/.config/kdedefaults"
    mv -f "${srcdir}/plasma-desktop.settings" "${srcdir}/plasma-org.kde.plasma.desktop-appletsrc"
    cp -R "${srcdir}/plasma-desktop.settings" "${pkgdir}/etc/skell/.config/plasma-org.kde.plasma.desktop-appletsrc"
    cp -R "${srcdir}/xsettingsd.conf" "${pkgdir}/etc/skel/.config/xsettingsd/xsettingsd.conf"
    cp -R "${srcdir}/kcminputrc" "${pkgdir}/et/skel/.config/kcminputrc"
    cp -R "${srcdir}/kcminputrc" "${pkgdir}/et/skel/.config/kdedefaults/kcminputrc"
}
