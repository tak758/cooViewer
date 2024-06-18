#+OPTIONS: "\n:t"
#+OPTIONS: ^:t
* 自分用 cooViewer

本家 [[https://github.com/coo-ona/cooViewer][coo-ona/cooViewer]] の [[https://github.com/coo-ona/cooViewer/forks?include=active&page=1&period=&sort_by=stargazer_counts][Fork]] や [[https://github.com/coo-ona/cooViewer/pulls][Pull requests]] から、自分が欲しいと思った機能をマージしたリポジトリ。

** マージ元

  - [[https://github.com/plife18/cooViewer/tree/custom][plife18/cooViewer:custom]] ブランチ
    - Monterey, arm64 + x86_64 対応
    - XADMaster, UniversalDetector の submodule 化 (RAR5 アーカイブが扱える)
    - Rounded-Rectangle アイコン (Big Sur 以降の丸角アイコン)
    - フルスクリーン時に上部に余白が残るのを修正
  - [[https://github.com/u39ueda/cooViewer/tree/fix/pagebar_minus_index_exception][u39ueda:fix/pagebar_minus_index_exception]]
    - ページバーで例外が出るのを修正
  - [[https://github.com/u39ueda/cooViewer/tree/feature/image_dpi][u39ueda:feature/image_dpi]]
    - 画像のDPIを無視する設定を追加

** その他の修正

  - Mac OS X 10.13 (High Sierra) 以上が必要
  - 単ページ・見開きのデフォルト値が無視されることがあるのを修正

** テスト環境

  - iMac 27 Late 2012
  - macOS 14.4.1 Sonoma (with OpenCore Lecacy Patcher)
  - Xcode 15.3

** ビルド方法

ローカルでビルドする場合。
#+begin_src sh
git clone --recursive https://github.com/tak758/cooViewer.git
cd cooViewer
xcodebuild -configuration Deployment
open build/Deployment/cooViewer.app
#+end_src
リモート(GitHub Actions)でもビルドが可能です。

** バイナリ

https://github.com/tak758/cooViewer/releases/latest

- x86_64 + arm64 のユニバーサルバイナリ
- Mac OS X 10.13 (High Sierra) 以上が必要

[[https://github.com/tak758/cooViewer/actions][GitHub Actions]] でビルドしたものです。\\
Xcode 14.3.1 を使用し =-sdk macosx13.3= が指定してあります。

署名はしてないのでGatekeeperがアプリ実行を拒否します。
