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

_evmfs_available="$( \
  command \
    -v \
    "evmfs" || \
    true)"
if [[ ! -v "_evmfs" ]]; then
  if [[ "${_evmfs_available}" != "" ]]; then
    _evmfs="true"
  elif [[ "${_evmfs_available}" == "" ]]; then
    _evmfs="false"
  fi
fi
_os="$( \
  uname \
    -o)"
_font_family=dec-terminal
_variant=modern
_pkg="${_font_family}-${_variant}"
_font="${_font_family}-${_variant}"
pkgname="ttf-${_font}"
pkgver=1.0
pkgrel=1
_pkgdesc=(
  "Font based on the one of the"
  "Digital Electronics Corp's
  VT220 video terminal."
)
pkgdesc="${_pkgdesc[*]}"
arch=(
  'any'
)
url="http://www.vtxemu.com/vtx/fnt/_decterm-demo.html"
license=(
  'custom'
)
_http="https://www.wfonts.com"
_license=(
  "${_http}/tos"
)
provides=(
  "ttf-${_font_family}=${pkgver}"
)
_sum="ebdcc3edf60748e4cb319dfb59943b4fa9967f7615f9a038fc3c066a3bc30cbc"
_sig_sum="8b3f187033c0c5e7ade4f5bbc7cf925c572ca59c0e9259006ecfbed01c438323"
# Dvorak
_sig_ns="0x87003Bd6C074C713783df04f36517451fF34CBEf"
# The kid
_evmfs_ns="0x926acb6aA4790ff678848A9F1C59E578B148C786"
_chain_id="100"
_fs="0x69470b18f8b8b5f92b48f6199dcb147b4be96571"
_evmfs_dir="evmfs://${_chain_id}/${_fs}/${_evmfs_ns}"
_evmfs_sig_dir="evmfs://${_chain_id}/${_fs}/${_evmfs_sig_ns}"
_evmfs_uri="${_evmfs_dir}/${_sum}"
_evmfs_sig_uri="${_evmfs_sig_dir}/${_sig_sum}"
_tarname="${_font}"
source=()
sha256sums=()
if [[ "${_evmfs}" == "true" ]]; then
  _uri="${_evmfs_uri}"
elif [[ "${_evmfs}" == "false" ]]; then
  _uri="${_http}/download/data/2015/05/12/${_font}/${_font}.zip"
  source+=(
    "${_sig_uri}"
  )
  sha256sums+=(
    "${_sig_sum}"
  )
fi
_src="${_tarname}.zip::${_uri}"
source+=(
  "${_src}"
)
sha256sums+=(
  "${_sum}"
)
validpgpkeys=(
  # Truocolo
  #   <truocolo@aol.com>
  '97E989E6CF1D2C7F7A41FF9F95684DBE23D6A3E9'
  #   <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
  'F690CBC17BD1F53557290AF51FC17D540D0ADEED'
  # Pellegrino Prevete (dvorak)
  #   <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>
  '12D8E3D7888F741E89F86EE0FEC8567A644F1D16'
)

package() {
  cd \
    "${srcdir}"
  install \
    -dm755 \
    "${pkgdir}/usr/share/fonts/TTF"
  install \
    -m644 \
    *".ttf" \
    "${pkgdir}/usr/share/fonts/TTF"
}
