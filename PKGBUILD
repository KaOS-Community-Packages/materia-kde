pkgname=materia-kde
pkgver=20200214
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
source=("https://github.com/PapirusDevelopmentTeam/${pkgname}/archive/${pkgver}.tar.gz")
md5sums=('f6cff946b5305382556737aaaff3450c')

package() {
    cd ${srcdir}/$pkgname-$pkgver
    make \
        PREFIX=/usr \
        IGNORE=aurorae \
        DESTDIR="${pkgdir}" \
        install
}
 
