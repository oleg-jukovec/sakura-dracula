pkgname=sakura-dracula
pkgver=3.6.0
pkgrel=0
pkgdesc="The sakura terminal emulator fork with dracula palette."
arch=('i686' 'x86_64')
url="https://github.com/oleg-jukovec/sakura-dracula"
license=('GPL')
depends=('vte3' 'vte-common' 'libxft')
makedepends=('git' 'cmake' 'gcc' 'make')
provides=('sakura-dracula')
conflicts=('sakura')
source=("git+https://github.com/oleg-jukovec/sakura-dracula.git#branch=master")
md5sums=('SKIP')

build() {
  cd $srcdir/${pkgname}

  # build & install	
  cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=RELEASE . 
  make 
}

package() {
  cd $srcdir/${pkgname}

  make DESTDIR=${pkgdir} install 
}