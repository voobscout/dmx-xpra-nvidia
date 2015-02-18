# Maintainer: Voobscout <voobscout+aur@gmail.com>
pkgname=dmx-xpra-nvidia
pkgver=1.0.0
pkgrel=1
pkgdesc="Configs and scripts to run Xdmx with Xephyr via Xpra on nvidia Xorg"
arch=('i686' 'x86_64')
license=('GPL2')
depends=('xorg-xdpyinfo'
         'xorg-xprop'
         'python2-opengl'
         'python2-gtkglext'
         'pyopengl-accelerate'
         'python2-dbus'
         'xpra-winswitch'
         'desktop-file-utils'
         'xorg-server'
         'xorg-xauth'
         'xorg-xbacklight'
         'xorg-xrdb'
        )
# TODO: actually check for my specific hardware and refuse to install pkg otherwise!
# 'nvidia-304xx'
# makedepends=('git' 'texinfo' 'autoconf' 'wget')
url="http://github.com/voobscout/dmx-xpra-nvidia"
provides=('dmx-xpra-nvidia')
source=('10-devices.conf'
        '10-layout.conf'
        '10-monitors.conf'
        '10-screens.conf'
        'xorg.service'
       )
sha256sums=('97e4b4df606ec74239c7c01948edf226b71883e1992873acac2f92e5848cc9d3'
            'ec9d0ef1d541b70a944abd66c7d2fb1ee725a17a56c32849463f3ebbb02c790d'
            '30e6dea8f0299ee32b3ebd01b222cd1ecc0f2820121308f521de1b821b2f35c9'
            'add213b07e775970e6deb4dd9bc244905a14a33541ca234983dcb8c737533466'
            '16b7c58a08f81beb9416e461aa7371f2e7fe44d42dfe7b0f6ca8e1d3eb94662b')
install=dmx-xpra-nvidia.install
options=(!strip)

build() {
  msg2 "There isn't anything to build actually..."
}

package() {
  msg "Installing xorg.conf.d components..."
  install -Dm 0644 ${srcdir}/10-devices.conf ${pkgdir}/etc/X11/xorg.conf.d/10-devices.conf
  install -Dm 0644 ${srcdir}/10-layout.conf ${pkgdir}/etc/X11/xorg.conf.d/10-layout.conf
  install -Dm 0644 ${srcdir}/10-monitors.conf ${pkgdir}/etc/X11/xorg.conf.d/10-monitors.conf
  install -Dm 0644 ${srcdir}/10-screens.conf ${pkgdir}/etc/X11/xorg.conf.d/10-screens.conf
  msg "Installing xorg systemd service"
  install -Dm 0644 ${srcdir}/xorg.service ${pkgdir}/usr/lib/systemd/system/xorg.service
 }
