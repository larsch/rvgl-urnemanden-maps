# Maintainer: Lars Christensen <larsch@belunktum.dk>
pkgname=rvgl-urnemanden-maps
pkgver=1.0
pkgrel=1
epoch=
pkgdesc=""
arch=(any)
url=""
license=('None')
groups=()
depends=(rvgl-bin)
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(
	"pisa.zip::https://www.revoltworld.net/dl/pisa/?filename=pisa.zip&wpdmdl=4983"
    "JungleVolt.zip::https://www.revoltworld.net/dl/junglevolt/?ind=0&filename=JungleVolt.zip&wpdmdl=3517"
    "ragarden.zip::https://www.revoltworld.net/dl/ragarden/?ind=0&filename=ragarden.zip&wpdmdl=1969")
noextract=()
sha256sums=(
	'4f51d0e02469e04ac20267db1724bff843754b4f3abfe568ac7d157fe295dbac'
    '145623126e3cace64362dd54982a946c98bd59bf2c7b0cde6db72711bf309d07'
	'18882f98f0b2b885002b9239d71d27aab8ad4021aaf82658625415bf60cb3d3a')
validpgpkeys=()

package() {
    mkdir -p "$pkgdir/opt/rvgl"
    cp -r gfx/ levels/ "$pkgdir/opt/rvgl/"
    find "$pkgdir/opt/rvgl" -type d -exec chmod 755 {} \;
    find "$pkgdir/opt/rvgl" -type f -exec chmod 644 {} \;
}
