# GithubSimpleMDE
Githubのファイル編集ページでエディターとしてSimpleMDEが使えるためのユザースクリプトと、FirefoxのCSP制限をオバーライドするブラウザー拡張。

# インストールしたら何ができる？
SimpleMDEとは使いやすいマークダウンエディターです。
使い方とデモンストレーションは下記リンク先で見れます。
http://nextstepwebs.github.io/simplemde-markdown-editor/

その他には、画像ファイルをSimpleMDEフィールドにDrag and dropすることで直接AWS S3にアップロードすることことができます。

# インストールの手順
## Firefox
* about:config でxpinstall.signatures.requireをfalseにする。
* https://github.com/arith-alexander/GithubSimpleMDE/raw/master/githubCspOverride.xpi をクリックして拡張をインストールする。 Windowsの場合はクリックするだけでインストールポップアップがでますが、Macは拡張ファイルをセーブしてブラウザにDrag and Dropする必要があります。
* Greasemonkeyをインストールする　https://addons.mozilla.org/ru/firefox/addon/greasemonkey/
* https://github.com/arith-alexander/GithubSimpleMDE/raw/master/GithubSimpleMDE.user.js をｄｌしてテクストエディターで開く。
* var gsmde = new GithubSimpleMDE("AKIA....KFYA", "lhSxx.....2ExRk8p");　のところでAWS S3 Access Key IdとAWS S3 Secret Access Keyを設定する。
* セーブして、ブラウザにDrag and dropして、出たポップアップでおｋを押すことでユザースクリプトをインストールする。
* 目次自動生成拡張をインストール https://addons.mozilla.org/ja/firefox/addon/github-readme-toc/
* ブラウザを再起動する。

## Chrome
* CSP Testerをインストールする https://chrome.google.com/webstore/detail/csp-tester/ehmipebdmhlmikaopdfoinmcjhhfadlf
* ブラウザの右上にあるCSP Testerのアイコンをクリックして、次の設定値を入力する：
  * Url pattern:　[https://github.com/*](https://github.com/*)
  * Policy: style-src style-src assets-cdn.github.com maxcdn.bootstrapcdn.com 'self' 'unsafe-inline'
* Tampermonkeyをインストールする　https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=ru
* https://github.com/arith-alexander/GithubSimpleMDE/raw/master/GithubSimpleMDE.user.js をｄｌしてテクストエディターで開く。
* var gsmde = new GithubSimpleMDE("AKIA....KFYA", "lhSxx.....2ExRk8p");　のところでAWS S3 Access Key IdとAWS S3 Secret Access Keyを設定する。
* セーブして、ブラウザにDrag and dropして、出たポップアップでおｋを押すことでユザースクリプトをインストールする。
* 目次自動生成拡張をインストール https://chrome.google.com/webstore/detail/github-readme-table-of-co/hlkhpeomjgelmljaknhoboeohhgmmgcn
* ブラウザを再起動する。


# で？
ファイル編集画面を開いて

<img src="https://arismile-documents.s3.amazonaws.com/pen_1452653008.PNG" width="400">

エディターを切り替える

<img src="https://arismile-documents.s3.amazonaws.com/bar_1452653119.PNG" width="400">

フール画面二パネルリアルタイムモードのボタン

<img src="https://arismile-documents.s3.amazonaws.com/button_1452654197.PNG" width="400">

画像を張り付けるのに、ここにDrag and dropしてください

<img src="https://arismile-documents.s3.amazonaws.com/zone_1452654391.PNG" width="400">
