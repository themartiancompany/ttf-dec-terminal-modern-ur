# SPDX-License-Identifier: AGPL-3.0

#    ----------------------------------------------------------------------
#    Copyright © 2024, 2025  Pellegrino Prevete
#
#    All rights reserved
#    ----------------------------------------------------------------------
#
#    This program is free software: you can redistribute it and/or modify
#    it under the terms of the GNU Affero General Public License as published by
#    the Free Software Foundation, either version 3 of the License, or
#    (at your option) any later version.
#
#    This program is distributed in the hope that it will be useful,
#    but WITHOUT ANY WARRANTY; without even the implied warranty of
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#    GNU Affero General Public License for more details.
#
#    You should have received a copy of the GNU Affero General Public License
#    along with this program.  If not, see <https://www.gnu.org/licenses/>.

# Maintainer:
#   Truocolo
#     <truocolo@aol.com>
#     <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
# Maintainer:
#   Pellegrino Prevete (dvorak)
#     <pellegrinoprevete@gmail.com>
#     <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>

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

