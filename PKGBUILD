# Submitter: Colin Duquesnoy <colin.duquesnoy@gmail.com>
# Maintainer: Colin Duquesnoy <colin.duquesnoy@gmail.com>
pkgbase=python-pyqode.python
pkgname=('python-pyqode.python')
pkgver=2.6.2
_pkgver=2.6.2
pkgrel=0
arch=('any')
url="https://github.com/pyQode/pyqode.python"
license=('MIT')
depends=('python')
makedepends=('python-setuptools')
source=("https://github.com/pyQode/pyqode.python/archive/${_pkgver}.tar.gz")
md5sums=('5a61b6bcb84d77a8d6644a0690b5017a')

build() {
   cd "$srcdir/pyqode.python-${_pkgver}"
}

package_python-pyqode.python() {
    pkgdesc="Add python support to pyQode"
    depends=('python'
	     'python-pyqode.qt'
	     'python-pyqode.core'
	     'python-jedi'
	     'pep8'
             'python-docutils')
    cd "$srcdir/pyqode.python-${_pkgver}"
    python3 setup.py install --root="$pkgdir/" --optimize=1

    install -D -m644 "$srcdir/pyqode.python-${_pkgver}/LICENSE" $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
