# Maintainer: Simon "ALSimon" Gilliot <simon@gilliot.fr>
# Contributor: Simon "ALSimon" Gilliot <simon@gilliot.fr>

pkgname=owncloud-app-reader-git
pkgver=42138ed
pkgrel=2
pkgdesc="An ebook reader"
arch=('any')
url="https://github.com/Yetangitu/owncloud-apps"
license=('AGPL')
depends=('owncloud')
makedepends=()
options=('!strip')
conflicts=()
source=("git+https://github.com/Yetangitu/owncloud-apps.git")
sha512sums=("SKIP")

pkgver() {
  cd "$SRCDEST/${_pkgname}"
  git describe --always | sed 's|-|.|g' | cut -f2 -d"v"
}

package() {
  install -d "${pkgdir}/usr/share/webapps/owncloud/apps"
  cp -a "${srcdir}/owncloud-apps/files_reader" "${pkgdir}/usr/share/webapps/owncloud/apps/files_reader"
}
