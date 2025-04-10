# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=rvgl-bastian-maps
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
source=("pisa.zip::https://www.revoltworld.net/dl/pisa/?filename=pisa.zip&wpdmdl=4983"
"JungleVolt.zip::https://www.revoltworld.net/dl/junglevolt/?ind=0&filename=JungleVolt.zip&wpdmdl=3517"
"ragarden.zip::https://www.revoltworld.net/dl/ragarden/?ind=0&filename=ragarden.zip&wpdmdl=1969"
        )
noextract=(pisa.zip JungleVolt.zip ragarden.zip)
sha256sums=('4f51d0e02469e04ac20267db1724bff843754b4f3abfe568ac7d157fe295dbac'
            '145623126e3cace64362dd54982a946c98bd59bf2c7b0cde6db72711bf309d07'
            '18882f98f0b2b885002b9239d71d27aab8ad4021aaf82658625415bf60cb3d3a')
validpgpkeys=()

prepare() {
	mkdir -p "$pkgname-$pkgver"
}

build() {
	cd "$pkgname-$pkgver"
	unzip -o -q ../pisa.zip
	unzip -o -q ../JungleVolt.zip
	unzip -o -q ../ragarden.zip

	# rename PISA pisa levels/pisa/PISA.*
	# mv Gfx gfx
	# set -x
	# find -type f -iname 'junglevolt.*' -execdir rename junglevolt JungleVolt {} \;
	# find -type f -iname 'JUNGLEVOLT.*' -execdir rename JUNGLEVOLT JungleVolt {} \;

	# find -type f -name 'Loadlevel*.bmp' -execdir rename Loadlevel loadlevel {} \;
	# find -type f -name 'Fxpage*.bmp' -execdir rename Fxpage fxpage {} \;
	# for ltr in a b c d e f g h i j; do
	# 	upper=$(echo $ltr | tr 'a-z' 'A-Z')
	# 	find -type f -name 'JungleVolt*.bm*' -execdir rename JungleVolt$upper JungleVolt$ltr {} \;
	# done
	# find
	# exit 1
}

check() {
	return 0
}

package() {
	mkdir -p "$pkgdir/opt/rvgl"
	cd "$pkgname-$pkgver"
	cp -r * "$pkgdir/opt/rvgl/"
}
