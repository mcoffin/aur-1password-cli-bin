# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Matt Coffin <mcoffin13@gmail.com>
pkgname=1password-cli-bin
pkgver=1.8.0
pkgrel=1
epoch=
pkgdesc="1password password manager cli"
arch=('x86_64')
url='https://1password.com'
license=('custom:LicenseRef-1Password-Proprietary')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=('1password-cli')
conflicts=('1password-cli')
replaces=()
backup=()
options=()
install=
changelog=
source=("op.zip::https://cache.agilebits.com/dist/1P/op/pkg/v${pkgver}/op_linux_amd64_v${pkgver}.zip")
noextract=()
sha512sums=('405f3620681bbd7eb647fcda6fa410aa86cd3e3ca8432693a62bbc1119a139cc1e14eb53e0d207531a5183435da6562f66755a188b01a855faea8be5a7bb3f6b')
validpgpkeys=()

build() {
	cd "$srcdir"
	[ ! -e op.sig ] || gpg2 --verify-files op.sig
}

package() {
	cd "$srcdir"
	install -Dm 0755 -t "$pkgdir"/usr/bin op
}
