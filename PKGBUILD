
pkgname=glportal
pkgver=0.0.7
pkgrel=1
pkgdesc="A free action adventure puzzle game"
arch=('i686' 'x86_64')
url="http://glportal.de/"
license=('ZLIB')
depends=('assimp' 'sdl2_mixer' 'glew' 'tinyxml')
makedepends=('cmake' 'git' 'boost')
source=("git+https://github.com/GlPortal/glPortal.git")
md5sums=('SKIP')

build() {
  cd "$srcdir/glPortal"
  mkdir -p build && pushd build
  cmake -DCMAKE_INSTALL_PREFIX=/usr ..
  make
}

package() {
  cd "$srcdir/glPortal/build"
  make DESTDIR="$pkgdir" install
}

