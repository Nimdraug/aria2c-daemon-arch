# Maintainer: Yunhui Fu <yhfudev@gmail.com>

pkgname=aria2c-daemon
pkgver=0.1
pkgrel=1
pkgdesc='Daemonize aria2c'
license=('GPL3')
arch=(any)
depends=('aria2')
conflicts=('aria2-daemon-svn')
replaces=('aria2-daemon-svn')
makedepends=('git')
url='https://github.com/yhfudev/aria2c-daemon-arch.git'
install=$pkgname.install
source=( aria2c-env.conf aria2c.conf aria2cd.service )
md5sums=('ed34ec0a71bf7c9e4174a6ffffa6decc'
         '8766000feac4339b314e262474b550c8'
         'e758c3ed67d1e6851198e77c28d3cef1')

_giturl='https://github.com/yhfudev/aria2c-daemon-arch.git'
_gitdir='aria2c-daemon-git'

build() {
	msg 'Cloning GIT repository...'
	cd "${srcdir}"
	cd ${srcdir}
	if [ -d ${_gitdir}/.git ]; then
		(cd ${_gitdir} && git pull origin)
	else
		(git clone ${_giturl} ${_gitdir})
	fi
	msg 'GIT repository downloaded...'
}

package() {
	install -D -m644 "${srcdir}/${_gitdir}/aria2c-env.conf" "${pkgdir}/etc/conf.d/aria2c-env.conf"
	install -D -m600 "${srcdir}/${_gitdir}/aria2c.conf"     "${pkgdir}/etc/conf.d/aria2c.conf"
	install -D -m755 "${srcdir}/${_gitdir}/aria2cd.service" "${pkgdir}/etc/systemd/system/aria2cd.service"
}

