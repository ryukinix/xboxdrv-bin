# Maintainer: Manoel Vilela <manoel_vilela@engineer.com>
pkgname=xboxdrv-bin
_pkgname=xboxdrv
pkgver=0.8.8
pkgrel=4
pkgdesc="A precompiled Xbox360 joystick emulator with Playstation2 gamepad
config"
arch=('x86_64')
url="http://pingus.seul.org/~grumbel/xboxdrv"
license=('GPL')
depends=('libx11' 'dbus-glib' 'libusb')
provides=('xboxdrv')
conflicts=('xboxdrv')
replaces=('xboxdrv')
backup=('etc/default/xboxdrv')
source=("https://www.dropbox.com/s/b9m78qyjyhatglx/xboxdrv.${pkgver}"
        "xboxdrv.default"
        "xboxdrv.openrc"
        "xboxdrv.1"
        "61-twin-joystick.rules"
        "uniq-num")
md5sums=('2865c2821450790d52984c90b1668d80'
         '5d6688ef948bf4ed6df0e6444e519fc4'
         '9ef3163573e99e64f3d2525795511693'
         '2d471a2aa0f81edecc9136a96e767d08'
         '2dd784ec4ae87a98803c2a806d58af9c'
         '05cd32b6de4f3612516bc0fc6879bd11')


package() {
  install -Dm 755 "${srcdir}/${_pkgname}.${pkgver}" "${pkgdir}/usr/bin/${_pkgname}"
  install -Dm 755 "${srcdir}/${_pkgname}.openrc" "${pkgdir}/etc/init.d/${_pkgname}d"
  install -Dm 644 "${srcdir}/${_pkgname}.default" "${pkgdir}/etc/default/${_pkgname}"
  install -Dm 644 "${srcdir}/xboxdrv.1" "${pkgdir}/usr/share/man/man1/xboxdrv.1"
  install -Dm 755 "${srcdir}/uniq-num" "${pkgdir}/usr/bin/uniq-num"
  install -Dm 655 "${srcdir}/61-twin-joystick.rules" -t "${pkgdir}/usr/lib/udev/rules.d/"
}
