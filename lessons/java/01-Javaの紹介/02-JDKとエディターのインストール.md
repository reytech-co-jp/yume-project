# 概要
JDKとエディタのインストールについてのガイドです。

# 目次

- JDKインストール
- エディタインストール
- エディタの設定

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
JDKをインストールときはバージョン11をインストールしてください。   
Windowの場合は環境設定もする必要がありますから、注意してやってみてください。
- Linuxにインストール
  - https://opensource.com/article/19/11/install-java-linux
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

## エディタの設定

インストールが終わったら、エディタに以下のものを設定しましょう。
- コードが自動でフォーマットされることと自動でimportの整理（optimize imports）をする
- ワイルドカードimportを禁止する
- ファイルの最終行に改行を入れる

### コードが自動でフォーマットされることと自動でimportの整理（optimize imports）をする

https://www.jetbrains.com/help/idea/reformat-and-rearrange-code.html#reformat-on-save

https://www.jetbrains.com/help/idea/creating-and-optimizing-imports.html#optimize-on-save

<img width="400" alt="スクリーンショット 2022-10-08 10 57 24" src="https://user-images.githubusercontent.com/62045457/194682346-ff16fbe3-af9a-4ed1-aefd-9e41134967ec.png">

<img width="400" alt="スクリーンショット 2022-10-08 10 58 13" src="https://user-images.githubusercontent.com/62045457/194682363-5baf507e-e6ba-454a-975b-69ab950047b2.png">

### ワイルドカードimportを禁止する

https://www.jetbrains.com/help/idea/creating-and-optimizing-imports.html#disable-wildcard-imports
https://www.jetbrains.com/help/idea/creating-and-optimizing-imports.html#disable-wildcards-for-class

### ファイルの最終行に改行を入れる

https://stackoverflow.com/questions/16761227/how-to-make-intellij-idea-insert-a-new-line-at-every-end-of-file
<img width="400" alt="スクリーンショット 2022-10-08 11 00 25" src="https://user-images.githubusercontent.com/62045457/194682440-2e0a01aa-a102-4e1c-b8ae-202251e38cb0.png">

# お願い

何か問題があれば、Slackの宿題手伝いチャネルに質問お願いします。
質問する時に、自分がやっとこと、エラーの内容、質問したいことを相手がわかりやすくように書いて質問しましょうね。
<img width="500" src="https://user-images.githubusercontent.com/100908505/208692131-c6596046-8943-41f9-bf0f-27e102b6ffd9.png">

***※これでJDKとエディタのインストールは完了となります。***