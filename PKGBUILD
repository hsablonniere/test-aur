# Maintainer: Clever Cloud <ci@clever-cloud.com>

pkgname=clever-tools-bin
pkgver=3.19.0
pkgrel=1
pkgdesc="Command Line Interface for Clever Cloud."
arch=('x86_64')
url="https://github.com/CleverCloud/clever-tools"
license=('Apache-2.0')

OPTIONS=(!strip)

source=("clever-tools-3.19.0_linux.tar.gz::https://clever-tools.clever-cloud.com/releases/3.19.0/clever-tools-3.19.0_linux.tar.gz")
sha256sums=('5971e4bb7dcdc11e9970a62db741d82b44ba1d01eb20b462d2a9ce9bf0181a6b')

package() {
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/bash-completion/completions"
  install -d "${pkgdir}/usr/share/zsh/site-functions"

  install "${srcdir}/clever-tools-3.19.0_linux/clever" "${pkgdir}/usr/bin/clever"

  "${srcdir}/clever-tools-3.19.0_linux/clever" --bash-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/bash-completion/completions/clever"
  "${srcdir}/clever-tools-3.19.0_linux/clever" --zsh-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/zsh/site-functions/_clever"
}