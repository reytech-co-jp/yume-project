# 概要
JDKとエディタのインストールについてのガイドです。

# 目次

- JDKインストール
- エディタインストール

## JDKインストール

### バージョンチェック

まずは自分のパソコンにJDKがインストールされているかどうかを確認しましょう。ターミナル(コマンドプロンプト)にこのコマンドを入力してチェックしてください。   
```bash
$ javac -version
```
以下のようにバージョンが表示されなかった方は次のステップをやってみましょう。
```bash
$ javac -version
'javac' is not recognized as an internal or external command.
opreable program or batch file.
```
もし以下のようにバージョンが表示された方はエディタのインストールをお願いします。      
```bash
$ javac -version
javac 11.0.2
```

### インストール方法

JDKのインストールはOSによって違うから自分のOSによるリンクをクリックし、参考にしてやってみてください。   
JDKをインストールときは最新のバージョンをインストールしてください。   
Windowの場合は環境設定もする必要がありますから、注意してやってみてください。
- Macにインストール
  - https://phoenixnap.com/kb/install-java-macos
- Windowにインストール
  - https://devwithus.com/install-java-windows-10/

インストールが終わったら、うまくインストールされたのかを先ほど紹介した方法で確認してみましょう。
以下のようにバージョンが表示されればOKです。
```bash
$ javac -version
javac 11.0.2
```

## エディタインストール

エディタはEclipseとかVS Codeとか自分が好きなエディタを使っても大丈夫です。   
この夢プロジェクトではIntellijを使っていきます。
IntellijのインストールもOSによって少し違うのでこちらのサイトを参考にしつつ自分でやってみてください。   
参考リンク： https://www.jetbrains.com/help/idea/installation-guide.html

# お願い

何か問題があれば、Slackの宿題手伝いチャネルに質問お願いします。   
質問する時に、自分がやっとこと、エラーの内容、質問したいことを相手がわかりやすくように書いて質問しましょうね。   
<img width="500" src="https://user-images.githubusercontent.com/100908505/208692131-c6596046-8943-41f9-bf0f-27e102b6ffd9.png">

***※これでJDKとエディタのインストールは完了となります。***