pkgname=materia-kde
pkgver=20190707
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
source=("https://github.com/PapirusDevelopmentTeam/materia-kde/archive/${pkgver}.tar.gz")
md5sums=('31bafc243a811e1de46b6416a60230a6')

package() {
    cd ${srcdir}/$pkgname-$pkgver
    make \
        PREFIX=/usr \
        IGNORE=aurorae \
        DESTDIR="${pkgdir}" \
        install
}
 
