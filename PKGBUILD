# Maintainer: udeved <udeved@openrc4arch.site40.net>

pkgname=kde-servicemenus-repo-management-git
pkgver=0.r13.90778d8
pkgrel=1
pkgdesc="Kde servicemenu for local repo-management"
arch=('any')
url="https://github.com/udeved/kde-repo-management-servicemenu"
license=('GPL2')
depends=('kdebase-dolphin' 'pacman')
makedepends=('git')
conflicts=('kde-servicemenus-repo-management')
install=repo-management.install
source=("$pkgname"::'git://github.com/udeved/kde-repo-management-servicemenu.git')
md5sums=('SKIP')

pkgver() {
      cd "$srcdir/$pkgname"
      printf "0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
      cd "$pkgname"

      install -Dm755 bin/repo-magic $pkgdir/usr/bin/repo-magic
      install -Dm644  ServiceMenus/repo-magic.desktop $pkgdir/usr/share/kde4/services/ServiceMenus/repo-magic.desktop
      install -Dm644 mime/application/x-xz-pkg.xml $pkgdir/usr/share/mime/application/x-xz-pkg.xml
      install -Dm644 mime/packages/application-x-xz-pkg.xml $pkgdir/usr/share/mime/packages/application-x-xz-pkg.xml
}
