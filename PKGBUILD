# Maintainer: Francisco Gonzalez <gzmorell @ gmail.com>
pkgname=mongo-cxx-driver
pkgver=v3.2
_pkgname=$pkgname-releases-$pkgver
pkgrel=1
pkgdesc="The official MongoDB C++ driver library"
arch=('i686' 'x86_64')
url="http://docs.mongodb.org/ecosystem/drivers/cpp/"
license=('Apache')
groups=()
depends=("libmongoc" )
makedepends=("cmake")
source=("https://github.com/mongodb/mongo-cxx-driver/archive/releases/$pkgver.tar.gz")
sha512sums=('e4e1762959ebb94c03dfc5fc67c1295b66eaa021624dc08320dfcbd3e56a83a19a05b31aa0e9febf26d7a8e5a91d8d4cfbf99476a2f925d29035813737ef46aa')

prepare() {
 cd "$pkgname-releases-$pkgver"
}

build() {
 cd "$srcdir/$_pkgname/build"
 cmake -DCMAKE_BUILD_TYPE=Release .. -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_CXX_STANDARD=17
}

package() {
cd "$srcdir/$_pkgname/build"
make DESTDIR="${pkgdir}" install
}
