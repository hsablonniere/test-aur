# Maintainer: Clever Cloud <ci@clever-cloud.com>

pkgname=clever-tools-bin
pkgver=1.24.0
pkgrel=1
pkgdesc="Command Line Interface for Clever Cloud."
arch=('x86_64')
url="https://github.com/CleverCloud/clever-tools"
license=('Apache-2.0')

OPTIONS=(!strip)

source=("clever-tools-1.24.0_linux.tar.gz::https://clever-tools.clever-cloud.com/releases/1.24.0/clever-tools-1.24.0_linux.tar.gz")
sha256sums=('3d77b4b848b90177d7b9e06e0391e1a90b0eb46f67cc58be0cf4b5c49d27aa26')

package() {
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/bash-completion/completions"
  install -d "${pkgdir}/usr/share/zsh/site-functions"

  install "${srcdir}/clever-tools-1.24.0_linux/clever" "${pkgdir}/usr/bin/clever"

  "${srcdir}/clever-tools-1.24.0_linux/clever" --bash-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/bash-completion/completions/clever"
  "${srcdir}/clever-tools-1.24.0_linux/clever" --zsh-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/zsh/site-functions/_clever"
}
