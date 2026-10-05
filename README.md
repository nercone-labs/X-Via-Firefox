# X via (Firefox)

[X via](https://github.com/naikaku1/X-Via)の非公式なFirefox移植版です。

macOS 27.0.1 上の Firefox Developer Edition (aurora, 158.0b4, aarch64) で動作確認済みです。

## インストール
X via (Firefox) は Cross-Platform Install (XPInstall, XPI) ファイルとして配布しています。
[リリースページ](https://github.com/nercone-labs/X-Via-Firefox/releases/)から入手できます。

### 署名について
Firefoxは標準で[AMO](https://addons.mozilla.org/)による署名のない拡張機能のインストールを制限しています。

X via (Firefox)の配布物にはAMOによる署名はありません。
そのため、X via (Firefox)をインストールするにはこの制限を解除する必要があります。

次の手順を実行することで、この制限を解除できます:
1. [about:config](about:config)を開きます
2. 確認画面が表示された場合「危険性を承知の上で続行」をクリックします
3. `xpinstall.signatures.required`を検索し、値をFalseに変更します

解除後、次の手順でXPIファイルをインストールします:
1. [about:addons](about:addons)を開きます
2. 歯車アイコンをクリックし「ファイルからアドオンをインストール...」をクリックします
3. ダウンロードしたXPIファイルを選択します

XPIファイルは、このリポジトリ上の次のファイルとディレクトリを含む.zipファイルを作成し、拡張子を.xpiに変更することで作成できます。
- LICENSE
- manifest.json
- content
- popup
