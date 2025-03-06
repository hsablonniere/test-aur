# Maintainer: Clever Cloud CI <ci@clever-cloud.com>

pkgname=clever-tools-bin
pkgver=3.12.0
pkgrel=1
pkgdesc="Command Line Interface for Clever Cloud."
arch=('x86_64')
url="https://github.com/CleverCloud/clever-tools"
license=('Apache-2.0')

OPTIONS=(!strip)

source=("clever-tools-3.12.0_linux.tar.gz::https://clever-tools.clever-cloud.com/releases/3.12.0/clever-tools-3.12.0_linux.tar.gz")
sha256sums=('3c1c2c8bd1c4fee114a09cbab349d3d1196a15f625934a37385abf35d7288979')

package() {
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/bash-completion/completions"
  install -d "${pkgdir}/usr/share/zsh/site-functions"

  install "${srcdir}/clever-tools-3.12.0_linux/clever" "${pkgdir}/usr/bin/clever"

  "${srcdir}/clever-tools-3.12.0_linux/clever" --bash-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/bash-completion/completions/clever"
  "${srcdir}/clever-tools-3.12.0_linux/clever" --zsh-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/zsh/site-functions/_clever"
}
