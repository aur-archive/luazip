pkgname="luazip"
pkgver="1.2.3"
pkgrel=2
pkgdesc="reading files inside zip files"
arch=('i686' 'x86_64')
url="http://www.keplerproject.org/luazip/"
license=('MIT')
depends=('lua' 'zziplib')
provides=()
conflicts=()

source=("http://luaforge.net/frs/download.php/2493/luazip-1.2.3.tar.gz")
md5sums=('8129ba93a8df6ebd324fee9adca23fae')

build() {
  cd $srcdir/luazip-1.2.3
  sed -i 's/5\.0/5.1/' config
  sed -i 's/500/510/' config
  sed -i "s#LUA_\([A-Z]*\)= /usr#LUA_\1= ${pkgdir}/usr#" config
  sed -i 's#local/##' config
  make lib || return 1
  make install || return 1
}
  
