# Maintainer: Hooregi <hooregi@halo.fm>
pkgname=slock-hooregi-git
pkgver=1.4.r582.d7109c1
pkgrel=1
epoch=
pkgdesc="Hooregi's build of suckless' simple locker (slock)"
arch=(x86_64)
url="https://gitlab.com/Hooregi/slock.git"
license=('MIT')
groups=()
depends=('libxext' 'libxrandr')
makedepends=('git')
checkdepends=()
optdepends=()
provides=(slock)
conflicts=(slock)
replaces=()
backup=()
options=()
install=
changelog=
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
	cd "${_pkgname}"
    printf "1.4.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd slock
    make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
    cd slock
    mkdir -p ${pkgdir}/opt/${pkgname}
    cp -rf * ${pkgdir}/opt/${pkgname}
    make PREFIX=/usr DESTDIR="${pkgdir}" install
    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    install -Dm644 README "${pkgdir}/usr/share/doc/${pkgname}/README"
}
