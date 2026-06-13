# Maintainer: Eric Hocking <ehocking@featherlinux.com>

pkgname=featherlinux-keyring
pkgver=20260613
pkgrel=1
pkgdesc="FeatherLinux PGP keyring"
arch=('any')
url="https://github.com/FeatherLinux/keyring"
license=('MIT')
depends=('pacman')
install="${pkgname}.install"
source=('Makefile'
        'featherlinux.gpg'
        'featherlinux-revoked'
        'featherlinux-trusted')
sha256sums=('b00e0304982253e15dc9ee076bd1c795585f1a1028112658a5d2c9f773c4d187'
            '5a10d8dc7b605d23b8c888aff8759b6e1134ffc8ef0730ea99c9ce1286a44a62'
            'af2081cc55ba21ec22226660fc8079f190ea7442008fe45d5de682860721972b'
            '279d15cdc4d66d8b6efe12c7a4945b8dfd235e635f97f102cd4a70afdb265eb3')

pkgver() {
  date +%Y%m%d
}

package() {
  make DESTDIR="${pkgdir}" install
}
