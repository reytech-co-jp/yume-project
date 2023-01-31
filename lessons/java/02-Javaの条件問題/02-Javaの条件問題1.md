# 条件文の課題

Javaの条件文の課題をやってみましょう。

# if文の使い方

if文の使い方についてはこちらのリンクを参考にしてください。   
ifの使い方の参考リンク: [ifの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/if_statement_questions/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#if)

# お願い
こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。
 
# 準備

`Main.java`に下記のように`num1`と`num2`というint型である2つの変数を記述してください。   
num1変数に10、num2変数に5整数を代入してください。
```java
public class Main {

  public static void main(String[] args) {
    int num1 = 10;
    int num2 = 5;
  }

}
```
int型変数について知らない方はこちらのリンクを参考にして読んでみてください。   
参考リンク: https://www.javadrive.jp/start/var/index4.html

# 課題１

`num1`の値が`num2`の値より大きい場合は`num1の値がnum2の値より大きいです。`というメッセージを表示してください。   
出力は下記のようになります。
```java
num1の値がnum2の値より大きいです。
```
ここで使う比較演算子を知らない方はこちらのサイトを参考にしてください。   
比較演算子の参考リンク: https://www.javadrive.jp/start/ope/index11.html   

# 課題２

`num1`と`num2`の足し算は15以上の場合は`num1とnum2の足し算値は15以上です。`というメッセージを表示してください。   
出力は下記のようになります。
```java
num1とnum2の足し算値は15以上です。
```
ここで使う比較演算子を知らない方はこちらのサイトを参考にしてください。   
比較演算子の参考リンク: https://www.javadrive.jp/start/ope/index11.html   

以上、超える/より大きい、以下、未満についてはこちらのリンクを参考にして読んでみてください。   
https://foreignlang.ecc.co.jp/learn/l00064d/   

# 課題３

`num1`の値が15より大きい、それとも`num2`の値が10以下の場合は`num1`と`num2`の引き算を表示してください。     
出力は下記のようになります。
```java
num1とnum2の引き算: 5
```
こちらで使う`||`論理演算子はこちらのサイトを参考にしてください。   
論理演算子の参考リンク: https://www.javadrive.jp/start/ope/index12.html

# 課題４

`num1`の値が10以上で`num2`の値が6未満の場合だけ`num1`と`num2`の足し算を表示してください。   
出力は下記のようになります。
```java
num1とnum2の足し算: 15
```
こちらで使う`&&`論理演算子はこちらのサイトを参考にしてください。   
論理演算子の参考リンク: https://www.javadrive.jp/start/ope/index12.html  

# 課題５

`num1`と`num2`の足し算は10以上で`num1`の値は5より大きいとき、そして`num2`の値は10以下の場合は`Completed`というメッセージを表示してください。   
出力は下記のようになります。
```java
Completed
```

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
