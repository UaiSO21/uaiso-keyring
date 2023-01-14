# Maintainer: Barnabé di Kartola <barnabedikartola@gmail.com>

pkgname=uaiso21-keyring
pkgver=$(date +%y.%m.%d)
pkgrel=$(date +%H%M)
pkgdesc="Key for UaiSO21 repository"
arch=('any')
url="https://github.com/UaiSO21/$pkgname"
license=('GPL3')
# depends=('')
provides=("$pkgname")
# conflicts=('')
source=("git+${url}.git")
md5sums=('SKIP')
if [ -e "${pkgname}.install" ];then
    install=${pkgname}.install
fi


package() {
    
    ${pkgdir}
    
    install -dm755 ${pkgdir}/usr/share/pacman/keyrings/
	install -m0644 ${srcdir}/${pkgname}/uaiso21{.gpg,-trusted,-revoked} ${pkgdir}/usr/share/pacman/keyrings/
}
