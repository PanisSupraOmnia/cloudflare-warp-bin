#!/hint/bash -e
# Maintainer: Leon Mergen <leon@solatis.com>
# Co-Maintainer: Barfin
pkgname=cloudflare-warp-bin
pkgver=2021.8.1
pkgrel=3
pkgdesc="Cloudflare Warp Client"

url="https://developers.cloudflare.com/warp-client/"
license=("unknown")

depends=("dbus")
arch=('x86_64')
provides=("${pkgname%-bin}" 'warp-cli' 'warp-diag' 'warp-svc')
conflicts=("${pkgname%-bin}")

# https://pkg.cloudflareclient.com/packages/cloudflare-warp
source=("https://pkg.cloudflareclient.com/uploads/cloudflare_warp_2021_8_1_1_amd64_a8f66bae8a.deb")

sha256sums=('4a4937bc3fceb5fa69332d6cbfd42496959d99053bf3d7661dcf6fbee1f85341')
install=$pkgname.install

prepare() {
    tar -xzvf data.tar.gz
}

package() {
    install -dm755 "$pkgdir/usr"
    cp -rt "$pkgdir/usr" "bin/" "lib/" "usr/share"
}
