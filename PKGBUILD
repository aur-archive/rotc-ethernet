pkgname="rotc-ethernet"
pkgver=p.5.4
pkgrel=1
pkgdesc="Revenge Of The Cats - Two teams fight for zones in this innovative multiplayer FPS"
arch=('i686' 'x86_64')
url="http://ethernet.wasted.ch//"
license=('GPL')
[ "$CARCH" = "i686" ] && depends=('libgl' 'sdl' 'libtheora' 'libxft')
[ "$CARCH" = "x86_64" ] && depends=('lib32-libgl' 'lib32-sdl' 'lib32-libtheora' 'lib32-libxft')
source=(http://files.wasted.ch/software/rotc-ethernet/$pkgname-$pkgver-linux.tar.gz $pkgname.desktop $pkgname.png $pkgname $pkgname-dedicated)
md5sums=('47df64a1bb4187a121aa918b529c3e39' '2a29d38c2720848429587e7da8bdb335' '48aa51d2b2694dd61b16c2d11087ffc8' 'e015c8fe46e71d3bd5626e04cd4cf9a8' '6d43c5740ea811df43668c2b75b1a882')

build() {
   mkdir -p $pkgdir/usr/share/applications
   mkdir -p $pkgdir/usr/share/pixmaps
   mkdir -p $pkgdir/usr/bin
   cp -R $srcdir/$pkgname-$pkgver-linux/ $pkgdir/usr/share/$pkgname
   cp $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/
   cp $srcdir/$pkgname.png $pkgdir/usr/share/pixmaps/
   cp $srcdir/$pkgname $pkgdir/usr/bin/
   cp $srcdir/$pkgname-dedicated $pkgdir/usr/bin/
   chmod 755 -R $pkgdir/usr/share/$pkgname
   chmod 755 $pkgdir/usr/bin/rotc-ethernet
   chmod 755 $pkgdir/usr/bin/rotc-ethernet-dedicated
}
