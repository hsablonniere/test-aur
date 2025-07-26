# Maintainer: Clever Cloud <ci@clever-cloud.com>

pkgname=clever-tools-bin
pkgver=1.34.0
pkgrel=1
pkgdesc="Command Line Interface for Clever Cloud."
arch=('x86_64')
url="https://github.com/CleverCloud/clever-tools"
license=('Apache-2.0')

OPTIONS=(!strip)

source=("clever-tools-1.34.0_linux.tar.gz::https://clever-tools.clever-cloud.com/releases/1.34.0/clever-tools-1.34.0_linux.tar.gz")
sha256sums=('1677460f9027359e488551495084ef34a41fc0778d7a9eeda1f0c6b4b669e188')

package() {
  install -d "${pkgdir}/usr/bin"
  install -d "${pkgdir}/usr/share/bash-completion/completions"
  install -d "${pkgdir}/usr/share/zsh/site-functions"

  install "${srcdir}/clever-tools-1.34.0_linux/clever" "${pkgdir}/usr/bin/clever"

  "${srcdir}/clever-tools-1.34.0_linux/clever" --bash-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/bash-completion/completions/clever"
  "${srcdir}/clever-tools-1.34.0_linux/clever" --zsh-autocomplete-script /usr/bin/clever > "${pkgdir}/usr/share/zsh/site-functions/_clever"
}
