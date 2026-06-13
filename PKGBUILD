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
sha256sums=('51847637e9a8f87c9387a4661a43d35cfe7d8fb414a448a7cebaa8b2ce39a0e3'
            'ecdf58d59ef4433d5c7e1b39e836a664b2d048a37de09a55604203e0eeee193a'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            'e86a41172d0edf93dbe3742e25e9836204c7c576e034ca2b16a6b93e679e4d8e')

pkgver() {
  date +%Y%m%d
}

package() {
  make DESTDIR="${pkgdir}" install
}
