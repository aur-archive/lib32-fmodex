# Maintainer: Mateus Rodrigues Costa <charles [dot] costar [at] gmail [dot] com>
# Contributor: Sven-Hendrik Haase <sh [at] lutzhaase [dot] com>
# Contributor: Christoph Zeiler <archNOSPAM [at] moonblade [dot] dot [dot] org>
# Contributor: Bartlomiej Piotrowski <nospam [at] bpiotrowski [dot] pl> 
# Contributor: kfgz <kfgz [at] interia [dot] pl>
# Contributor: Christos Kotsaris <christos [dot] kotsaris [at] gmail [dot] com>
# Contributor: Florian Pritz <flo [at] xinu [dot] at>

_pkgbasename=fmodex
pkgname=lib32-$_pkgbasename
pkgver=4.44.41
pkgrel=1
pkgdesc="An advanced audio engine"
url="http://www.fmod.org/"
arch=('x86_64')
license=('custom')
depends=("$_pkgbasename>=$pkgver" "lib32-gcc-libs")
source=(http://www.fmod.org/download/fmodex/api/Linux/fmodapi${pkgver//./}linux.tar.gz)
md5sums=('0537faee354a5f302b08000e6816fcdc')

package() {  
  msg2 "Copying libs"
  mkdir -p "$pkgdir"/usr/lib32
  cp -d fmodapi${pkgver//./}linux/api/lib/* "$pkgdir"/usr/lib32/
  rm "$pkgdir"/usr/lib32/*64*
  
  msg2 "Creating symlink for license directory"
  mkdir -p "$pkgdir"/usr/share/licenses/
  ln -s $_pkgbasename "$pkgdir"/usr/share/licenses/$pkgname
}
