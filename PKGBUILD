pkgname=materia-kde
pkgver=20190319.r0.g4996669
pkgrel=1
pkgdesc="Materia theme for KDE Plasma 5"
arch=('any')
url="https://github.com/PapirusDevelopmentTeam/materia-kde"
license=('GPL3')
optdepends=('kvantum: For the Qt application style'
            'materia-gtk-theme: Matching GTK theme'
            'papirus-icon-theme: For the Papirus icon theme'
            'yakuake: For the Yakuake skin')
makedepends=('git' 'make')
conflicts=("${pkgname%-*}")
provides=("${pkgname%-*}")
options=(!strip)
source=("${pkgname%-*}::git+${url}.git")
sha256sums=('SKIP')

pkgver() {
    cd "${pkgname%-*}"
    git describe --long --tags | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}

package() {
    make -C "${pkgname%-*}" \
        PREFIX=/usr \
        IGNORE=aurorae \
        DESTDIR="${pkgdir}/" \
        install
} 
