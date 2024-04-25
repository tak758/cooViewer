# 自分用 cooViewer

本家 [coo-ona/cooViewer](https://github.com/coo-ona/cooViewer) の [Fork](https://github.com/coo-ona/cooViewer/forks?include=active&page=1&period=&sort_by=stargazer_counts) や [Pull requests](https://github.com/coo-ona/cooViewer/pulls) から、自分が欲しいと思った機能をマージしたリポジトリ。


## マージ元

-   [plife18/cooViewer:custom](https://github.com/plife18/cooViewer/tree/custom) ブランチ
    -   Monterey, arm64 + x86\_64 対応
    -   XADMaster, UniversalDetector の submodule 化 (RAR5 アーカイブが扱える)
    -   Rounded-Rectangle アイコン (Big Sur 以降の丸角アイコン)
    -   フルスクリーン時に上部に余白が残るのを修正
-   [u39ueda:fix/pagebar\_minus\_index\_exception](https://github.com/u39ueda/cooViewer/tree/fix/pagebar_minus_index_exception)
    -   ページバーで例外が出るのを修正
-   [u39ueda:feature/image\_dpi](https://github.com/u39ueda/cooViewer/tree/feature/image_dpi)
    -   画像のDPIを無視する設定を追加


## その他の修正

-   Mac OS X 10.13 (High Sierra) 以上が必要
-   単ページ・見開きのデフォルト値が無視されることがあるのを修正


## テスト環境

-   iMac 27 Late 2012
-   macOS 14.4.1 Sonoma (with OpenCore Lecacy Patcher)
-   Xcode 15.3


## ビルド方法

```sh
git clone --recursive https://github.com/tak758/cooViewer.git
cd cooViewer
xcodebuild -configuration Deployment
open build/Deployment/cooViewer.app
```
