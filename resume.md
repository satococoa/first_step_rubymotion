# 構成
- 第1章: RubyMotion 自体や学び方などの説明
- 第2章: 実際に手を動かしてアプリをつくる

# はじめに
## 対象読者
- iOS アプリの開発をしてみたい Rubyist
- Objective-C の経験は不問。

## 目的
- RubyMotion の購入を検討している人の背中を押す。
- RubyMotion を買ったけれどもあまり活用できていない人のモチベーションを上げる。
- RubyMotion でアプリをつくりたい人のための高速道路を整備する。

# RubyMotion とは
## RubyMotion の簡単な紹介
- 2012 年 5 月にリリースされ、今まで数多くの RubyMotion で作られたアプリが出てきたこと。
- 自分の好きなツールを使えるということ。
- 国内外でジワジワと盛り上がりを見せていること。

## ライセンス体系
- サポート、アップデートは年間更新 (ソフトウェア自体は使い続けられる)
- 更新料は新規ライセンスの約半額

## 仕組み
Objective-C で実装された Ruby を使い、LLVM により Objective-C ランタイム上で動作するバイナリになる。

この仕組みのおかげで Objective-C で作られたライブラリも RubyMotion ではそのまま扱えるし、Objective-C で定義されたクラスに特異メソッドを定義するなんてことも可能。

## RubyMotion の魅力
- Cocoa Touch フレームワークを直接扱うことになるので、Objective-C の知識は必ずしも必須ではないが、Cocoa Touch の知識は必要となる。
- Objective-C と Cocoa Touch を同時に学ぶことよりは、慣れ親しんだ Ruby を使いながら Cocoa Touch を使えるのでスムーズに学ぶことが出来る。
- その知識は RubyMotion 独自の知識ではないので、将来的に Objective-C をやることになってもそのまま役に立つ。
- 直接バイナリになるので、パフォーマンスの低下を心配しなくてよい。

## 他の主要なフレームワークとの違い
### PhoneGap
- Ruby vs HTML5
- WebView をラップするのではなく、完全にネイティブになる

### Titanium
- Ruby vs JavaScript
- ObjC のコードが吐かれるのではなく、LLVM を使用して Objective-C ランタイム上で動作するバイナリになる

### Xamarin
- Ruby vs C#
- (TODO: 調査)


## 開発の手順
### 購入〜インストールの流れ
さらっと購入ページ、メール、ダウンロード、インストールという手順をたどることを書くだけ。

### 開発ツール
- Sublime Text 2
- Emacs
- Vim
- RubyMine
- Xcode (StoryBoard, モデルエディタ)
- Terminal

### Hello, world
- 単純なアラート ->  sample: HelloWorld
- ボタンをタップしたらアラート -> sample: HelloWorld2
- コンソールから動的にボタンのタイトルを書き換える

### テストについて
- Bacon (Unit, Functional)
- Carabash

### デバッグの仕方
#### `rake debug=1` (GDB)
- bt, break, pro, pri くらい？

## 主要なライブラリ
### [Bundler](http://gembundler.com) と組み合わせる
### [CocoaPods](http://cocoapods.org)
### [motion-testflight](https://github.com/HipByte/motion-testflight)
### [BubbleWrap](http://bubblewrap.io)

## 情報の調べ方
- [Developer Center](http://www.rubymotion.com/developer-center/)
- [Google Groups](http://groups.google.com/group/rubymotion)
- [Motion Meetup](http://meetup.rubymotion.com)
- [Stack Overflow](http://stackoverflow.com) Objective-C の項目も参考になるよ、と。
- [RubyMotion API Reference](http://www.rubymotion.com/developer-- ter/api/)
- [RubyMotion JP](http://rubymotion.jp)
  - IRC チャンネル
  - RubyMotion もくもく会

## iOS アプリ開発でおさえておきたいもの
- Apple の公式ドキュメント (特に View Controller Programming, View Programming)
  - 日本語訳がある: https://developer.apple.com/jp/devcenter/ios/library/japanese.html
- [エキスパートObjective-Cプログラミング ― iOS/OS Xのメモリ管理とマルチスレッド](http://tatsu-zine.com/books/objc)
- [iOS開発におけるパターンによるオートマティズム](http://hmdt.jp/hmdtbooks/pg329.html)


# チュートリアル
Rails 製の Web API と連携したアプリケーションを実際に作ってみる。

アプリ案
- RSS リーダー
- メモアプリ
- 行きたい場所メモとか


本格的にアプリをつくる際には必須なので、以下についてもサンプルに入れたい
- NSNotification (`App.notification_center`)
- KVO (`BW::KVO`)
- GCD (`Dispatch`)
- NSOperationQueue

## CRUD のアプリをつくってみる
AFMotion を使う。

### Read (一覧)
### Create (作成)
### Update (更新)
### Delete (削除)

## 端末にデータを保存する
色々紹介はするが、チュートリアルでは motion-nanostore OR Serialize を使いたい。  
ここでは一番基本的な Serialize でいいか。

- 何を保存するか。
  - RSS リーダーならお気に入りをローカルに持たせてもいいかも。
    - 保存する属性: id, title, url, bookmarked_at
  - 既読情報？いつどこで既読にしたかを管理してみる？
  - Map に出したら意味はわからないけれど面白いかも

### NSUserDefault (`App::Persistent`)
### Serialize (`NSCoding protocol`)
### Core Data
### [NanoStoreInMotion](https://github.com/siuying/NanoStoreInMotion)
