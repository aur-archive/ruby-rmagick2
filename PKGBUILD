# Contributor: Alexsandr Pavlov <kidoz at mail dot ru>
pkgname=ruby-rmagick2
_gemname=rmagick
pkgver=2.13.1
pkgrel=2
pkgdesc="Interface between the Ruby programming language and the ImageMagick"
arch=(any)
url="http://rmagick.rubyforge.org"
license=(MIT)
depends=('ruby' 'imagemagick' 'rubygems')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('f528a83789c5abbe540b6227c08b2f5a')
 
build() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem
}

