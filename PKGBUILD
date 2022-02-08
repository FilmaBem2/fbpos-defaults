# Maintainer: Filma Bem <filmabemtv2@gmail.com>
pkgname=fbpos-defaults
pkgver=r7.6f01f77
pkgrel=1
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
md5sums=('3098dea87b1857b22626ba60349028a3')
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
    mkdir "${pkgdir}/root"
    mkdir "${pkgdir}/root/.config"
    mkdir "${pkgdir}/root/.config/kdedefaults"
    mkdir "${pkgdir}/root/.config/xsettingsd"
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
    cp -R "${srcdir}/plasma-org.kde.plasma.desktop-appletsrc" "${pkgdir}/root/.config/"
    cp -R "${srcdir}/xsettingsd.conf" "${pkgdir}/root/.config/xsettingsd/"
    cp -R "${srcdir}/kcminputrc" "${pkgdir}/root/.config/"
    cp -R "${srcdir}/kcminputrc" "${pkgdir}/root/.config/kdedefaults/"
    cp -R "${srcdir}/kdeglobals" "${pkgdir}/root/.config/"
    cp -R "${srcdir}/kdeglobals" "${pkgdir}/root/.config/kdedefaults/"
    cp -R "${srcdir}/kscreenlockerrc" "${pkgdir}/root/.config/"
    cp -R "${srcdir}/kscreenlockerrc" "${pkgdir}/root/.config/kdedefaults/"
    cp -R "${srcdir}/ksplashrc" "${pkgdir}/root/.config/"
    cp -R "${srcdir}/ksplashrc" "${pkgdir}/root/.config/kdedefaults/"
    cp -R "${srcdir}/kwinrc" "${pkgdir}/root/.config/"
    cp -R "${srcdir}/kwinrc" "${pkgdir}/root/.config/kdedefaults/"
    cp -R "${srcdir}/plasmarc" "${pkgdir}/root/.config/"
    cp -R "${srcdir}/plasmarc" "${pkgdir}/root/.config/kdedefaults/"
    cp -R "${srcdir}/fbpmirrors" "${pkgdir}/etc/pacman.d/"
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
