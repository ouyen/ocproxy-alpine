# Contributor: Kevin Cernekee <cernekee@gmail.com>
# Maintainer: Ouyen <ouyen1@outlook.com>
pkgname=ocproxy
pkgver=1.60
pkgrel=0
pkgdesc="SOCKS proxy for openconnect"
url="https://github.com/cernekee/ocproxy"
arch="all"
license="custom"
depends="libevent"
makedepends="linux-headers libevent-dev libc-dev autoconf automake gcc binutils make"
source="$pkgname-$pkgver.tar.gz::https://github.com/cernekee/ocproxy/archive/refs/tags/v$pkgver.tar.gz"
subpackages="$pkgname-doc"

build() {
	./autogen.sh
	./configure --prefix=/usr \
		--sysconfdir=/etc \
		--mandir=/usr/share/man \
		--infodir=/usr/share/info
	make
}


package() {
	install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
	make DESTDIR="$pkgdir" install
}

sha512sums="
fab00b35e8c291a8af7e6c7184fabb82aeab68afa0fef0cad3f24f99dae633e4af9c0f6fc9744956cce27dbede64fa4961388fec4c07ec60bf6dddf63faa11eb  ocproxy-1.60.tar.gz
"
