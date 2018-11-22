# Maintainer: Jace Bennest <jacebennest87 at gmail dot com>
# Contributor: skydrome <skydrome at i2pmail dot org>
# Contributor: Adrian Wheeldon <arandomowl at gmail dot com>
# Contributor: StevensNJD4 <github dot com slash StevensNJD4>

pkgname=lazyman
pkgver=2.4.0.20181101
pkgrel=1
pkgdesc="A simple program that lets you stream every NHL and MLB game"
arch=('any')
url="https://github.com/StevensNJD4/LazyMan"
license=('GPL2')
depends=('java-runtime>=8' 'streamlink') 
optdepends=('vlc: requires a video player - choose one' 'mpv: requires a video player - choose one')
backup=('usr/share/java/lazyman/config.properties')

source=("https://github.com/StevensNJD4/LazyMan/releases/download/${pkgver}/Mac_Linux.zip"
	"config.properties"
	"${pkgname}.sh"
	"${pkgname}.desktop"
	"${pkgname}.png"
	"${pkgname}.svg")

package() {
    cd "$srcdir"

    install -dm755 "${pkgdir}/usr/bin"
    install -dm755 "${pkgdir}/usr/share/applications"
    install -dm755 "${pkgdir}"/usr/share/icons
    install -dm755 "${pkgdir}/usr/share/icons/Numix-Circle/16/apps"
    install -dm755 "${pkgdir}/usr/share/icons/Numix-Circle/22/apps"
    install -dm755 "${pkgdir}/usr/share/icons/Numix-Circle/24/apps"
    install -dm755 "${pkgdir}/usr/share/icons/Numix-Circle/48/apps"
    install -dm777 "${pkgdir}/usr/share/java/${pkgname}"
    install -dm777 "${pkgdir}/usr/share/java/${pkgname}/mitm"

    install -Dm755 "${pkgname}".sh      "${pkgdir}/usr/bin/${pkgname}"
    install -Dm644 "${pkgname}".desktop "${pkgdir}/usr/share/applications/${pkgname}.desktop"
    install -Dm644 "${pkgname}".png     "${pkgdir}/usr/share/icons/${pkgname}.png"
    install -Dm644 "${pkgname}".svg     "${pkgdir}/usr/share/icons/Numix-Circle/16/apps/${pkgname}.svg"
    install -Dm644 "${pkgname}".svg     "${pkgdir}/usr/share/icons/Numix-Circle/22/apps/${pkgname}.svg"
    install -Dm644 "${pkgname}".svg     "${pkgdir}/usr/share/icons/Numix-Circle/24/apps/${pkgname}.svg"
    install -Dm644 "${pkgname}".svg     "${pkgdir}/usr/share/icons/Numix-Circle/48/apps/${pkgname}.svg"
    install -Dm777 config.properties    "${pkgdir}/usr/share/java/${pkgname}/config.properties"
    install -Dm644 LazyMan.jar          "${pkgdir}/usr/share/java/${pkgname}/LazyMan.jar"
    install -Dm655 mitm/linux/mitmdump  "${pkgdir}/usr/share/java/${pkgname}/mitm/linux/mitmdump"
    install -Dm644 mitm/proxy.py        "${pkgdir}/usr/share/java/${pkgname}/mitm/proxy.py"
}

md5sums=('e9af636a4fccfcd6e81a74f69247eaf0'
         'd41d8cd98f00b204e9800998ecf8427e'
         'b387dc6c2bdf54718d6d2e48f9f37e3d'
         'cc5998a228727420cbf7d07fc5318920'
         '41aebb968e8b6856d1b73cabd6a8c5d2'
         '838805914545f8ece3df2115b638252f')
