# RubyMotion とは
## RubyMotion の簡単な紹介
- 2012 年 5 月にリリースされ、今まで数多くの RubyMotion で作られたアプリが出てきたこと。
- 自分の好きなツールを使えるということ。
- 国内外でジワジワと盛り上がりを見せていること。

## 仕組み
Objective-C で実装された Ruby を使い、LLVM により Objective-C ランタイム上で動作するバイナリになる

## ライセンス体系
- サポート、アップデートは年間更新 (ソフトウェア自体は使い続けられる)

## 他の主要なフレームワークとの違い
### PhoneGap
- Ruby vs HTML5
- WebView をラップするのではなく、完全にネイティブになる

### Titanium
- Ruby vs JavaScript
- ObjC のコードが吐かれるのではなく、LLVM を使用して Objective-C ランタイム上で動作するバイナリになる

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
- 単純なアラート
- ボタンをタップしたらアラート
- コンソールから動的にボタンのタイトルを書き換える

### デバッグの仕方
#### `rake debug=1` (GDB)
- bt, break, pro, pri くらい？

## 主要なライブラリ
### [Bundler](http://gembundler.com) と組み合わせる
### [BubbleWrap](http://bubblewrap.io)
### [Teacup](https://github.com/rubymotion/teacup)
### [Pixate](http://www.pixate.com)
### [CocoaPods](http://cocoapods.org)

## 情報の調べ方
- [Developer Center](http://www.rubymotion.com/developer-center/)
- [Google Groups](http://groups.google.com/group/rubymotion)
- [Motion Meetup](http://meetup.rubymotion.com)
- [Stack Overflow](http://stackoverflow.com)
- [RubyMotion API Reference](http://www.rubymotion.com/developer-- ter/api/)
- [RubyMotion JP](http://rubymotion.jp)
  - IRC チャンネル
  - RubyMotion もくもく会

# チュートリアル
Rails 製の Web API と連携したアプリケーションを実際に作ってみる。

## CRUD のアプリをつくってみる
AFMotion を使う。

### Read (一覧)
### Create (作成)
### Update (更新)
### Delete (削除)

## 端末にデータを保存する
色々紹介はするが、チュートリアルでは motion-nanostore OR Serialize を使いたい。  
ここでは一番基本的な Serialize でいいか。

### NSUserDefault (`App::Persistent`)
### Serialize (`NSCoding protocol`)
### Core Data
### [NanoStoreInMotion](https://github.com/siuying/NanoStoreInMotion)

## よりよい設計のために知っておきたいこと
### NSNotification (`App.notification_center`)
### KVO (`BW::KVO`)
### GCD (`Dispatch`)
### NSOperationQueue

何か端末ならではの機能も使いたい気がする。
- 位置情報、カメラ etc.

# メモ
## iOS アプリ開発でおさえておきたいもの
- Apple の公式ドキュメント (特に View Controller Programming, View Programming)
- [エキスパートObjective-Cプログラミング ― iOS/OS Xのメモリ管理とマルチスレッド](http://tatsu-zine.com/books/objc)
- [iOS開発におけるパターンによるオートマティズム](http://hmdt.jp/hmdtbooks/pg329.html)


