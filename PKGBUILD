pkgname=materia-kde
pkgver=20210612
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
md5sums=('3040fac70ed9831d9b677711d4f9b043')

package() {
    cd ${srcdir}/$pkgname-$pkgver
    make \
        PREFIX=/usr \
        IGNORE=aurorae \
        DESTDIR="${pkgdir}" \
        install
}
 
