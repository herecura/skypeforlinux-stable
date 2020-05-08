# Maintainer: mark.blakeney at bullet-systems dot net
# Original Maintainer: Jameson Pugh <imntreal@gmail.com>

_pkgname=skypeforlinux
pkgname=$_pkgname-stable
pkgver=8.60.76.73
pkgrel=1
pkgdesc="Skype for Linux - Stable/Release Version"
arch=("x86_64")
url="http://www.skype.com"
license=("custom")
depends=("gtk3" "libxss" "alsa-lib" "libxtst" "libsecret" "nss" "glibc>=2.28-4")
optdepends=("gnome-keyring")
conflicts=("$_pkgname" "$_pkgname-bin" "$_pkgname-preview-bin" "$_pkgname-beta-bin" "skype")
replaces=("$_pkgname-bin" "$_pkgname-preview-bin" "$_pkgname-beta-bin" "skype")
provides=("$_pkgname" "skype")
source=(
"https://repo.skype.com/deb/pool/main/s/$_pkgname/${_pkgname}_${pkgver}_amd64.deb"
)
sha256sums=('e8c0417013687f6b7ad8e8596a83ab031b32ec569ab9e97b6483f8dae7d2a929')

package() {
  tar -xJC "$pkgdir" -f data.tar.xz
  install -d "$pkgdir/usr/share/licenses/$pkgname"
  mv "$pkgdir/usr/share/$_pkgname/LICENSES.chromium.html" \
    "$pkgdir/usr/share/licenses/$pkgname/"
  rm -rf "$pkgdir/opt"
}

# vim:set ts=2 sw=2 et:
