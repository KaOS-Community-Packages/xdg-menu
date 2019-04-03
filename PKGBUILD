
pkgname=xdg-menu
pkgver=0.7.6.3
pkgrel=1
pkgdesc="automatically generate WM menu from xdg files"
arch=('x86_64')
url="https://wiki.archlinux.org/index.php/XdgMenu"
license=("GPL")
depends=('perl' 'perl-xml-parser')
backup=("etc/update-menus.conf"
	"etc/xdg/menus/arch-applications.menu")
source=("https://arch.p5n.pp.ru/~sergej/dl/2018/arch-xdg-menu-$pkgver.tar.gz")
sha256sums=('b99668bee882da7bf0ac247e1d9274b75a062bfe0af12efb994d97e40e361914')

package() {
  cd "$srcdir"
  install -D -m 0755 xdg_menu "$pkgdir"/usr/bin/xdg_menu
  install -D -m 0755 xdg_menu_su "$pkgdir"/usr/bin/xdg_menu_su
  install -D -m 0755 update-menus "$pkgdir"/usr/bin/update-menus
  install -D -m 0644 update-menus.conf "$pkgdir"/etc/update-menus.conf
  mkdir -p "$pkgdir"/usr/share/desktop-directories/
  cp arch-desktop-directories/* "$pkgdir"/usr/share/desktop-directories/
  mkdir -p "$pkgdir"/etc/xdg/menus/
  cp arch-xdg-menu/* "$pkgdir"/etc/xdg/menus/
  mkdir -p "$pkgdir"//var/cache/xdg-menu
}
