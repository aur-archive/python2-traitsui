# Maintainer: Andrzej Giniewicz <gginiu@gmail.com>
pkgname=python2-traitsui
pkgver=4.2.0
_githubtag=cfd5c30
pkgrel=1
pkgdesc="Traits-capable user interfaces"
arch=('any')
url="https://github.com/enthought/traitsui"
license=('BSD')
depends=('python2-traits' 'python2-pyface')
makedepends=('python2-distribute')
conflicts=('python2-traitsui-git')
options=(!emptydirs)

source=("https://github.com/enthought/traitsui/tarball/${pkgver}")
md5sums=('e7888fb9de420c5d91793d8b35d8211e')

build() {
  cd "$srcdir/enthought-traitsui-${_githubtag}"

  python2 setup.py build
}

package() {
  cd "$srcdir/enthought-traitsui-${_githubtag}"

  python2 setup.py install --root="$pkgdir"/ --optimize=1

  install -D "LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

