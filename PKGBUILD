# Maintainer: Charles Bos <charlesbos1 AT gmail>
# Contributor: Xiao-Long Chen <chenxiaolong@cxl.epac.to>

pkgname=sphinx-voxforge-en
_actual_ver=0.1.1
_extra_ver=~daily20130301
_source_date=20130301
pkgver=${_actual_ver}.${_source_date}
pkgrel=2
pkgdesc="English Sphinx models built from the Voxforge audio corpus"
arch=('any')
url="http://www.voxforge.org/"
license=('GPL')
groups=('unity')
source=("https://launchpad.net/ubuntu/+archive/primary/+files/sphinx-voxforge-en_${_actual_ver}${_extra_ver}.orig.tar.gz")
sha512sums=('247fec16789a98d8bd60ee30b4df49059729ae0ceb444c07cfd0a0d6c0a91bc47dc8ac2bb8d672aa12dfa92cc78fc1ae67c22200ab48dbd0ea6514b888f07147')

package() {
  cd "${srcdir}/${pkgname}"

  install -dm755 \
    "${pkgdir}/usr/share/sphinx-voxforge-en/hmm/voxforge_en_sphinx.cd_cont_3000/"
  install -m644 model_parameters/voxforge_en_sphinx.cd_cont_3000/* \
    "${pkgdir}/usr/share/sphinx-voxforge-en/hmm/voxforge_en_sphinx.cd_cont_3000/"

  install -dm755 \
    "${pkgdir}/usr/share/sphinx-voxforge-en/lm/voxforge_en_sphinx.cd_cont_3000/"
  install -m644 etc/voxforge_en_sphinx.lm.DMP \
                etc/voxforge_en_sphinx.dic \
    "${pkgdir}/usr/share/sphinx-voxforge-en/lm/voxforge_en_sphinx.cd_cont_3000/"
}
