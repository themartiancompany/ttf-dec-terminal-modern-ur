# SPDX-License-Identifier: AGPL-3.0
#
# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Pellegrino Prevete (tallero) <pellegrinoprevete@gmail.com>
_pkgname=dec-terminal-modern
pkgname=ttf-$_pkgname
pkgver=1.0
pkgrel=1
_pkgdesc=(
  "Font based on the one of the"
  "Digital Electronics Corp's VT220 video terminal."
)
pkgdesc="${_pkgdesc[*]}"
arch=(any)
url="http://www.vtxemu.com/vtx/fnt/_decterm-demo.html"
license=(
  'custom'
)
_license=(
  "https://www.wfonts.com/tos"
)
source=(
  "https://www.wfonts.com/download/data/2015/05/12/${_pkgname}/${_pkgname}.zip"
)
md5sums=(
  '13a70789fe00d6b0b4cfed39309575c4'
)

package() {
  cd \
    "$srcdir"
  install \
    -dm755 \
    "${pkgdir}/usr/share/fonts/TTF"
  install \
    -m644 \
    *".ttf" \
    "${pkgdir}/usr/share/fonts/TTF"
}

