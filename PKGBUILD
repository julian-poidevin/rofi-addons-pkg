# Maintainer: Julian Poidevin <poidevin dot julian at gmail dot com>
pkgname=rofi-addons
pkgver=r98.e119e2c
pkgrel=1
epoch=
pkgdesc="A huge collection of Rofi based custom Applets, Launchers & Powermenus."
arch=('any')
url="https://github.com/julian-poidevin/rofi-addons.git"
license=(GPL3)
groups=()
depends=('rofi')
makedepends=(git)
optdepends=()
provides=('rofi-addons')
conflicts=('rofi-addons' 'rofi-adi1090x')
backup=('usr/share/sddm/themes/tokyo-night-sddm/theme.conf')
source=('git+https://github.com/julian-poidevin/rofi-addons.git')
sha256sums=('SKIP')

pkgver() {
	cd "${srcdir}/rofi-addons"
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

prepare() {
	cd "${srcdir}/rofi-addons"
	chmod +x setup.sh
}

package() {
	cd "${srcdir}/rofi-addons"
	./setup.sh
}
