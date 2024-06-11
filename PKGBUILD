# Maintainer: Clever Cloud CI <ci@clever-cloud.com>

pkgname=clever-tools-bin
pkgver=3.7.0
pkgrel=1
pkgdesc="Command Line Interface for Clever Cloud."
arch=('x86_64')
url="https://github.com/CleverCloud/clever-tools"
license=('Apache-2.0')

OPTIONS=(!strip)

source=("clever-tools-3.7.0_linux.tar.gz::https://clever-tools.clever-cloud.com/releases/3.7.0/clever-tools-3.7.0_linux.tar.gz")
sha256sums=('9f3e423cc4f4b014d4176623ae829c0a8d584c63923f56a1d12ae7f25d157ec1')

package() {
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/bash-completion/completions"
  install -d "${pkgdir}/usr/share/zsh/site-functions"

  install "${srcdir}/clever-tools-3.7.0_linux/clever" "${pkgdir}/usr/bin/clever"

  "${srcdir}/clever-tools-3.7.0_linux/clever" --bash-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/bash-completion/completions/clever"
  "${srcdir}/clever-tools-3.7.0_linux/clever" --zsh-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/zsh/site-functions/_clever"
}
