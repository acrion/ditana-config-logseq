# Maintainer: Stefan Zipproth <s.zipproth@ditana.org>

pkgname=ditana-config-logseq
pkgver=1.13.2
pkgrel=5
pkgdesc="Logseq configuration with gpt3-openai plugin using local koboldcpp instance"
arch=(any)
license=('AGPL-3.0-or-later AND MIT')
depends=(
    logseq-desktop-bin
)
makedepends=(npm git)
source=(
    'logseq-plugin-gpt3-openai.json'
)
sha256sums=(
    'SKIP'
)

package() {
    cd /tmp
    rm -rf logseq-plugin-gpt3-openai
    git clone --branch "v$pkgver" --depth 1 https://github.com/briansunter/logseq-plugin-gpt3-openai.git
    cd logseq-plugin-gpt3-openai

    npm install
    npm run build

    PLUGIN_DIR="$pkgdir/etc/skel/.logseq/plugins/logseq-plugin-gpt3-openai"

    mkdir -p "$PLUGIN_DIR"

    # Install LICENSE and package.json
    install -Dm644 LICENSE "$PLUGIN_DIR/LICENSE"
    install -Dm644 package.json "$PLUGIN_DIR/package.json"

    # Copy dist directory
    cp -r dist "$PLUGIN_DIR/dist"

    # Create plugins.edn configuration
    mkdir -p "$pkgdir/etc/skel/.logseq/config"
    echo "{:logseq-plugin-gpt3-openai {:version \"$pkgver\", :repo \"briansunter/logseq-plugin-gpt3-openai\", :effect true, :theme false}}" > "$pkgdir/etc/skel/.logseq/config/plugins.edn"

    install -Dm644 "$srcdir/logseq-plugin-gpt3-openai.json" "$pkgdir/etc/skel/.logseq/settings/logseq-plugin-gpt3-openai.json"
}
