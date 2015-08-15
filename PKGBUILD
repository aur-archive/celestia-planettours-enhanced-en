# Maintainer: JasonPollitt <snostormjp+arch@gmail.com>
# Contributor: ConnorBehan  <connor.behan@gmail.com>
pkgname=celestia-planettours-enhanced-en
pkgver=3.0
pkgrel=3
pkgdesc="Tours of the eight major planets plus Pluto in Celestia"
arch=(i686 x86_64)
url="http://www.celestiamotherlode.net/catalog/scripts.php"
license=('GPL','cc-by-nc-sa-3.0')
depends=('celestia')
makedepends=('unzip')
source=(http://www.celestiamotherlode.net/creators/bhegwood/mercurytour.zip \
http://www.celestiamotherlode.net/creators/seeks/venustour-nix.zip \
http://www.celestiamotherlode.net/creators/bhegwood/EarthTourFiles.zip \
http://www.celestiamotherlode.net/creators/bhegwood/MarsTourFiles.zip \
http://www.celestiamotherlode.net/creators/bhegwood/JupiterTourFiles.zip \
http://www.celestiamotherlode.net/creators/bhegwood/SaturnTourFiles.zip \
http://www.celestiamotherlode.net/creators/bhegwood/UranusTourFiles.zip \
http://www.celestiamotherlode.net/creators/bhegwood/NeptuneTourFiles.zip \
http://www.celestiamotherlode.net/creators/bhegwood/PlutoTourFiles.zip \
http://www.celestiamotherlode.net/creators/marco_klunder/SunAndPlanetsSizeComparison_EN_2011.zip)

md5sums=('76e53795f08d49d5eb8f76543e60fa85' \
'7e8f0700093f6c5bf4359cc4b6ebde75' \
'552b95ac0b4acf4120f7147112710056' \
'21659f4c1e1186db6a522af7fdcc2bfa' \
'c30025ca6ec964359380c4f6536a5d07' \
'132ca9c6d3e02942c39febec578b9e7c' \
'24404cc538a53b988856d3dd6a25fa84' \
'3a9c1abf731f317c70f4887858546cb6' \
'274b69053a9ded5f10303bfcf59a25b3' \
'307ffa60d4509133461d1c49b7a8d44c')

build() {
  mkdir ${startdir}/pkg/usr/
  mkdir ${startdir}/pkg/usr/share
  mkdir ${startdir}/pkg/usr/share/celestia
  mkdir ${startdir}/pkg/usr/share/celestia/extras
  mkdir ${startdir}/pkg/usr/share/celestia/scripts
  mkdir ${startdir}/pkg/usr/share/celestia/data
  cd ${startdir}/src
  mkdir ${startdir}/src/scripts
  mv extras/Tours/*.cel ./scripts/
  mv  "Program Files"/Celestia/extras/* ./extras
  cp -R "Program Files"/Celestia/textures/* ./textures
  cp -R textures/* ${startdir}/pkg/usr/share/celestia/textures
  cp -R scripts ${startdir}/pkg/usr/share/celestia
  cp -R extras/* ${startdir}/pkg/usr/share/celestia/extras
  cp -R models ${startdir}/pkg/usr/share/celestia
  cp *.ssc ${startdir}/pkg/usr/share/celestia/extras/
  cp -R "Program Files"/Celestia/*.cel ${startdir}/pkg/usr/share/celestia/scripts/
  cp *.cel ${startdir}/pkg/usr/share/celestia/scripts/
  cp *.celx ${startdir}/pkg/usr/share/celestia/scripts/
}

