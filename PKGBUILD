# Maintainer:  fluffymadness
# fluffymadness(at)posteo.de

pkgname=headphonestatus-git
_gitname=headphonestatus
pkgver=a0764f2
pkgrel=1
pkgdesc="An Headphone Status Indicator, that shows if the headphones are plugged it"
arch=('i686' 'x86_64')
url="https://github.com/fluffymadness/headphonestatus"
license=('GPLv2')
depends=('python2' 'python2-pyqt4')
makedepends=('git')
# The git repo is detected by the 'git:' or 'git+' beginning. The branch
# 'pacman41' is then checked out upon cloning, expediating versioning:
#source=('git+https://github.com/falconindy/expac.git'
source=('git://github.com/fluffymadness/headphonestatus.git')
# Because the sources are not static, skip Git checksum:
md5sums=('SKIP')

pkgver() {
  cd $_gitname
  # Use the tag of the last commit
  git describe --always | sed 's|-|.|g'
}



package() {
  cd $_gitname
  install -Dm755 "headphonestatus.py" "$pkgdir/usr/bin/headphonestatus"
  install -Dm755 "icons/headphonestatus-active.png" "$pkgdir/usr/share/pixmaps/headphonestatus-active.png"
  install -Dm755 "icons/headphonestatus-inactive.png" "$pkgdir/usr/share/pixmaps/headphonestatus-inactive.png"
}
