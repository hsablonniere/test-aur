# Maintainer: Clever Cloud CI <ci@clever-cloud.com>

pkgname=clever-tools-bin
pkgver=3.5.2
pkgrel=1
pkgdesc="Command Line Interface for Clever Cloud."
arch=('x86_64')
url="https://github.com/CleverCloud/clever-tools"
license=('Apache-2.0')

OPTIONS=(!strip)

source=("clever-tools-3.5.2_linux.tar.gz::https://clever-tools.clever-cloud.com/releases/3.5.2/clever-tools-3.5.2_linux.tar.gz")
sha256sums=('1ed712626177b1192cfedf3b7e2ece7c859207b2ec784e288662e3d1a3ea2358')

package() {
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/bash-completion/completions"
  install -d "${pkgdir}/usr/share/zsh/site-functions"

  install "${srcdir}/clever-tools-3.5.2_linux/clever" "${pkgdir}/usr/bin/clever"

  "${srcdir}/clever-tools-3.5.2_linux/clever" --bash-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/bash-completion/completions/clever"
  "${srcdir}/clever-tools-3.5.2_linux/clever" --zsh-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/zsh/site-functions/_clever"
}
