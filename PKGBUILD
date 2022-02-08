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
source=(fbpos-defaults.zip)
noextract=()
md5sums=('cd56fbd7ae8391743c20699ba8170e31')
validpgpkeys=()

pkgver() {
	cd "${_pkgname}"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    mkdir "${pkgdir}/etc"
    mkdir "${pkgdir}/etc/skel"
    mkdir "${pkgdir}/etc/skel/.config"
    mkdir "${pkgdir}/etc/skel/.config/kdedefaults"
    mkdir "${pkgdir}/etc/skel/.config/xsettingsd"
    mkdir "${pkgdir}/etc/pacman.d"
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
    cp -R "${srcdir}fbpmirrors" "${pkgdir}/etc/pacman.d/"
    echo "" >> "${pkgdir}/etc/pacman.conf"
    echo "[fbpos-main]" >> "${pkgdir}/etc/pacman.conf"
    echo "SigLevel = Optional TrustAll" >> "${pkgdir}/etc/pacman.conf"
    echo "Include = /etc/pacman.d/fbpmirrors" >> "${pkgdir}/etc/pacman.conf"
    echo "" >> "${pkgdir}/etc/pacman.conf"
    echo "[fbpos-themes]" >> "${pkgdir}/etc/pacman.conf"
    echo "SigLevel = Optional TrustAll" >> "${pkgdir}/etc/pacman.conf"
    echo "Include = /etc/pacman.d/fbpmirrors" >> "${pkgdir}/etc/pacman.conf"
    echo "" >> "${pkgdir}/etc/pacman.conf"
    echo "[fbpos-games]" >> "${pkgdir}/etc/pacman.conf"
    echo "SigLevel = Optional TrustAll" >> "${pkgdir}/etc/pacman.conf"
    echo "Include = /etc/pacman.d/fbpmirrors" >> "${pkgdir}/etc/pacman.conf"
    echo "" >> "${pkgdir}/etc/pacman.conf"
    echo "[fbpos-drivers]" >> "${pkgdir}/etc/pacman.conf"
    echo "SigLevel = Optional TrustAll" >> "${pkgdir}/etc/pacman.conf"
    echo "Include = /etc/pacman.d/fbpmirrors" >> "${pkgdir}/etc/pacman.conf"
    echo "" >> "${pkgdir}/etc/pacman.conf"
}
