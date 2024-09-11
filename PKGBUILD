# Maintainer: Levente Polyak <anthraxx[at]archlinux[dot]org>
# Maintainer: T.J. Townsend <blakkheim@archlinux.org>
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Bartłomiej Piotrowski <bpiotrowski@archlinux.org>
# Contributor: Thorsten Töpper <atsutane-tu@freethoughts.de>
# Contributor: Thayer Williams <thayer@archlinux.org>
# Contributor: Jeff 'codemac' Mickey <jeff@archlinux.org>
# Contributor: Artur Leivar <arturleivarx@gmail.com>

pkgname=dmenu
pkgver=5.3
pkgrel=3
pkgdesc='Generic menu for X'
url='https://tools.suckless.org/dmenu/'
arch=('x86_64')
license=('MIT')
makedepends=('git')
depends=('sh' 'glibc' 'coreutils' 'libx11' 'libxinerama' 'libxft' 'freetype2' 'fontconfig' 'libfontconfig.so')
source=("git+https://git.suckless.org/dmenu#tag=${pkgver}"
        "https://raw.githubusercontent.com/arthurx07/dmenu/my_dmenu/patches/01-dmenu-barpadding-5.3.diff"
        "https://raw.githubusercontent.com/arthurx07/dmenu/my_dmenu/patches/02-dmenu-xresources-alt-5.0.diff"
        "https://raw.githubusercontent.com/arthurx07/dmenu/my_dmenu/patches/03-dmenu-fuzzymatch-5.3.diff"
        "https://raw.githubusercontent.com/arthurx07/dmenu/my_dmenu/patches/04-dmenu-password-5.3.diff"
        "https://raw.githubusercontent.com/arthurx07/dmenu/my_dmenu/patches/05-dmenu_run-terminal.diff"
        "https://raw.githubusercontent.com/arthurx07/dmenu/my_dmenu/patches/06-dmenu-vi_nav-20230907.diff"
        "https://raw.githubusercontent.com/arthurx07/dmenu/my_dmenu/patches/07-dmenu-lineheight-5.2.diff")
sha512sums=('781f4aab2bb32c39e79a2269b62fdb8cacdcebc162f73844e0ff86f8d084fd151eb63811e0f4de906ae5b3ca3a02f12c82fbf4d9f5f3e4a9b5d847de787aefd4'
            '81bc7d453aa28d88439dc7d1ebb290d0b8e9550572ec6850b84a666165366b9dfa02009da06d31763db20d317b62da804693d2ddb9f04644933ca5a0c42f7c40'
            '8194dd9403bf1bc3016b0884bd2a6afa251c570206e6e4f2deb9d3d40d4f5103fe354f9b24f468783345e65e84e9c5531f078fc242914d3e7b57a1fa9818fa3c'
            'db56d332449e71b3b1cf48ac75403fcc81a25a53a545a5c687995cdc36291056c2fa9bffff3335a19b4e8b973e565a3be295c215421f66c1cc3d074b50c02dbd'
            '0da5e03c1ad546015cf69c4a509a723aa9bb33c5b759b3d75ee759d2b06db4f1b65204922fb155b145f644618b4f72274b9da813e2be4fc4f3719dae45fe1a37'
            '63ab18a39901c8700e3b1de29553cbcb8203d322d5b9a618c60577dcd4329e0e4a13704388305494e3bd103d5415dfa5dcbe997d8fd6ffdb7578c0bec0af0d36'
            '026d91b061eb6e386b92a12545d5b9e6abec2fb37ced257b9c7e1f0d649e616be18029a2f5eff1a1bf50a1dcbd770467dc8c7c57337c7be01a7936c0a6091195'
            '9049547831956b32f8e753889ce33f203f1a53c62bfaa24332570d3e515bab20430094218000cb198f65af16d1a4913cadf5be7bb33724b6ff5f5ceec81cd429')
b2sums=('6da7112a8975c152038f7694f1a658674f92c2d5a9340f97e8b64430a2fce612c87effd361078b66ce77510d6bb6478c47ea3b1d6ee0adfafa1e8c0d62f1adb5'
        '9eeef5fb0c27a753266a8a3471847928649a2a18a811df1983e5d9458942e268ab4e64ab400e3f903625ed1c837d531e06e3d0930dc349a3423e89f98034dec1'
        '7b0a3261baefdfad2df82cba4821d31cb4dd1bded4ce4f444a1f4da119335d8993a74092342ef20e227b8da2438d2a86c649fb996ef3f1b18dcdd20bafb6cfd7'
        'a7124c17237b2ab1f8f54e98196af1c674a66a3d901a55a7c5030603028bb621c517036eef29b765c0b1b0b6cdc32011531b7621aed6e863c11981d8bbbcdde3'
        'ef8f2593b8698bae415fb683c8b21bb96ca9be8d1f852d6106799638545ec16f82487fe4965dbf9655aaf6d81c1fcf7092792c12a40497691329b4f2b0d7a2a4'
        '2544b460ff6f9c8f957a623a73d73db0f1f18feca8708c2ee95699fb99ac799ef8abe8dea870d0d3d6c2f02455e1d65545042a70e7329800c21f848a59b32455'
        '9fec13f7c0abefd2c0f8c482bff13d76eae3c0bd2fd4aa39b8a994df6eb0e53469b79e5d7310dd1f13c5a83c3518c33fc5bf8d16778df23a83bcde615b8e9aa4'
        'ef0043821029c57d2f9d5571679859ae11c82ea98d7962fcdafe4b474e7dd6cc71e7251a79e3db7509e4f001d3808a0cb4f2ff74abf0c1c856c7f60edce8123c')

prepare() {
  cd ${pkgname}
  patch -Np1 -i ../01-dmenu-barpadding-5.3.diff
  patch -Np1 -i ../02-dmenu-xresources-alt-5.0.diff
  patch -Np1 -i ../03-dmenu-fuzzymatch-5.3.diff
  patch -Np1 -i ../04-dmenu-password-5.3.diff
  patch -Np1 -i ../05-dmenu_run-terminal.diff
  patch -Np1 -i ../06-dmenu-vi_nav-20230907.diff
  patch -Np1 -i ../07-dmenu-lineheight-5.2.diff

  echo "CPPFLAGS+=${CPPFLAGS}" >> config.mk
  echo "CFLAGS+=${CFLAGS}" >> config.mk
  echo "LDFLAGS+=${LDFLAGS}" >> config.mk
}

build() {
  cd ${pkgname}
  make \
	  X11INC=/usr/include/X11 \
	  X11LIB=/usr/lib/X11 \
	  FREETYPEINC=/usr/include/freetype2
}

package() {
  cd ${pkgname}
  make PREFIX=/usr DESTDIR="${pkgdir}" install
  install -Dm 644 LICENSE -t "${pkgdir}/usr/share/licenses/${pkgname}"
}

# vim: ts=2 sw=2 et:
