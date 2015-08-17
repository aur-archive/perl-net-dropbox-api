# Maintainer:  Michael Kogan <michael dot kogan at gmx dot net>

pkgname=perl-net-dropbox-api
pkgver=1.9
pkgrel=2
pkgdesc="Net::Dropbox::API - Perl dropbox API interface"
arch=('i686' 'x86_64')
url="http://search.cpan.org/~norbu/Net-Dropbox-API/lib/Net/Dropbox/API.pm"
license=('GPL, PerlArtistic')
depends=('perl-common-sense' 'perl-data-random' 'perl-http-message' 'perl-json' 'perl-libwww' 'perl-mouse' 'perl-net-oauth' 'perl-uri' 'perl-lwp-protocol-https')
source=(http://search.cpan.org/CPAN/authors/id/N/NO/NORBU/Net-Dropbox-API-${pkgver}.tar.gz)
md5sums=('5f5d053f7a116d0f645ce6835e545cb8')
sha1sums=('c1c5ba827492e171cb65124b65ece4da2442ea84')

build() {
    cd "$srcdir/Net-Dropbox-API-${pkgver}"
    perl Makefile.PL INSTALLDIRS=vendor
    make || return 1
}
package() {
    cd "$srcdir/Net-Dropbox-API-${pkgver}"
    make DESTDIR=$pkgdir install || return 1
}
