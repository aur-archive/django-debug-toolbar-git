# Contributor:  apkawa <apkawa@gmail.com>
pkgname=django-debug-toolbar-git
pkgver=20111027
pkgrel=1
pkgdesc="A configurable set of panels that display various debug information about the current"
arch=('i686' 'x86_64')
url="http://rob.cogit8.org/blog/2008/Sep/19/introducing-django-debug-toolbar/"
license=('GPL')
depends=('python2' 'django')
makedepends=('git')
source=( )
md5sums=( )
_gitname="django-debug-toolbar"
_gitroot="git://github.com/django-debug-toolbar/django-debug-toolbar.git"

build() {
      cd ${srcdir}
      msg "Connecting to $_gitroot GIT server...."

      if [ -d ${srcdir}/$_gitname ] ; then
      cd $_gitname && git pull origin
      msg "The local files are updated."
      else
      git clone $_gitroot && cd $_gitname
      fi

      msg "GIT checkout done or server timeout"

    python2 setup.py install --root=${pkgdir} && \
    install -D -m0644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}

