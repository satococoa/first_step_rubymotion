# RubyMotion とは
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
### Hello, world
### デバッグの仕方
#### `rake debug=1` (GDB)

## 主要なライブラリ
### BubbleWrap
### Teacup
### Pixate
### CocoaPods
### Bundler と組み合わせる

## 情報の調べ方
- [Developer Center](http://www.rubymotion.com/developer-center/)
- [Google Groups](http://groups.google.com/group/rubymotion)
- [Motion Meetup](http://meetup.rubymotion.com)
- [Stack Overflow](http://stackoverflow.com)
- [RubyMotion API Reference](http://www.rubymotion.com/developer-- ter/api/)
- [RubyMotion JP](http://rubymotion.jp)
  - IRC チャンネル
  - RubyMotion もくもく会


# WebAPI と連携したアプリケーションを作る: チュートリアル
## CRUD のアプリをつくってみる
### Read
### Create
### Update
### Delete

## 端末にデータを保存する
### NSUserDefault
### Serialize
### Core Data
### NanoStore

## よりよい設計のために知っておきたいこと
### Notification
### KVO
### GCD
### NSOperationQueue


# メモ
## iOS アプリ開発でおさえておきたいもの
- Apple の公式ドキュメント
- [エキスパートObjective-Cプログラミング ― iOS/OS Xのメモリ管理とマルチスレッド](http://tatsu-zine.com/books/objc)
- [iOS開発におけるパターンによるオートマティズム](http://hmdt.jp/hmdtbooks/pg329.html)


