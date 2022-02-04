# Maintainer: Filma Bem <filmabemtv2@gmail.com>
pkgname=fbpos-defaults
pkgver=22
pkgrel=2
epoch=
pkgdesc="FBP OS Default Settings"
packager=('Filma Bem <filmabemtv2@gmail.com>')
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
source=(plasma-desktop.settings
        kcminputrc
        kdeglobals
        kscreenlockerrc
        ksplashrc
        kwinrc
        plasmarc
        xsettingsd.conf)
noextract=()
md5sums=('afdbb58f29e90280b0caaf6e410ef2a4'
         '20df043a7c00619072a4ad6c2641a63c'
         '6009f8fa5d42232b2740dcf6b116e7aa'
         '65a32833f4d32e3b95c5c1fe9c578613'
         '74ce8822203fdeeb7e5846ad19633488'
         'd1d66e90f7c3a99036884092fb3c9c30'
         'aa6bb29e14ad8a0091357b851c1d9953'
         '1f3374debb770f3bd3e56ff9fb20ad4e')
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
    mkdir "${pkgdir}/etc/skel/.config/xsettingsd"
    mv -f "${srcdir}/plasma-desktop.settings" "${srcdir}/plasma-org.kde.plasma.desktop-appletsrc"
    cp -R "${srcdir}/plasma-org.kde.plasma.desktop-appletsrc" "${pkgdir}/etc/skel/.config/"
    cp -R "${srcdir}/xsettingsd.conf" "${pkgdir}/etc/skel/.config/xsettingsd/"
    cp -R "${srcdir}/kcminputrc" "${pkgdir}/etc/skel/.config/"
    cp -R "${srcdir}/kcminputrc" "${pkgdir}/etc/skel/.config/kdedefaults/"
    cp -R "${srcdir}/kdeglobals" "${pkgdir}/etc/skel/.config/"
    cp -R "${srcdir}/kdeglobals" "${pkgdir}/etc/skel/.config/kdedefaults/"
    cp -R "${srcdir}/kscreenlockerrc" "${pkgdir}/etc/skel/.config/"
    cp -R "${srcdir}/kscreenlockerrc" "${pkgdir}/etc/skel/.config/kdedefaults/"
    cp -R "${srcdir}/ksplashrc" "${pkgdir}/etc/skel/.config/"
    cp -R "${srcdir}/ksplashrc" "${pkgdir}/etc/skel/.config/kdedefaults/"
    cp -R "${srcdir}/kwinrc" "${pkgdir}/etc/skel/.config/"
    cp -R "${srcdir}/kwinrc" "${pkgdir}/etc/skel/.config/kdedefaults/"
    cp -R "${srcdir}/plasmarc" "${pkgdir}/etc/skel/.config/"
    cp -R "${srcdir}/plasmarc" "${pkgdir}/etc/skel/.config/kdedefaults/"
}
