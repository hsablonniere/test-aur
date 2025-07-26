# Maintainer: Clever Cloud <ci@clever-cloud.com>

pkgname=clever-tools-bin
pkgver=1.31.0
pkgrel=1
pkgdesc="Command Line Interface for Clever Cloud."
arch=('x86_64')
url="https://github.com/CleverCloud/clever-tools"
license=('Apache-2.0')

OPTIONS=(!strip)

source=("clever-tools-1.31.0_linux.tar.gz::https://clever-tools.clever-cloud.com/releases/1.31.0/clever-tools-1.31.0_linux.tar.gz")
sha256sums=('99f7a5b00e50ea0016f78dcd2e2a312a560ac7b5547472a0cfff73051f8755e9')

package() {
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/bash-completion/completions"
  install -d "${pkgdir}/usr/share/zsh/site-functions"

  install "${srcdir}/clever-tools-1.31.0_linux/clever" "${pkgdir}/usr/bin/clever"

  "${srcdir}/clever-tools-1.31.0_linux/clever" --bash-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/bash-completion/completions/clever"
  "${srcdir}/clever-tools-1.31.0_linux/clever" --zsh-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/zsh/site-functions/_clever"
}
