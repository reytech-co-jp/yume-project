# 条件文の課題

Javaの条件文の課題をやってみましょう。

# if文の使い方

if文の使い方についてはこちらのリンクを参考にしてください。   
ifの使い方の参考リンク: [ifの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/if_statement_questions/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#if)

# お願い
こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のように`greeting`というString型変数を記述してください。
```java
public class Main {

  public static void main(String[] args) {
    String greeting = "Hello World";
  }

}
```
Stringについて知らない方はこちらのリンクを参考にして読んでみてください。   
参考リンク: https://www.javadrive.jp/start/num/index3.html
 
# 課題１   

`greeting`にある文字の長さは10以上とき`greetingの長さは10以上です。`というメッセージを表示してください。   
出力は下記のようになります。
```java
greetingの長さは10以上です。
```
ここで使う(String.length)Stringクラスのメソッドを知らない方はこちらのサイトを参考にしてください。   
参考リンク: https://www.javadrive.jp/start/string/index6.html

# 課題２

`greeting`にある文字の長さは10以上で20未満のときは`greeting`にある文字を大文字に変更して、その文字の長さを表示してください。   
出力の文書は下記のようになります。
```java
greeting : HELLO WORLD
greetingの長さは11です。
```
大文字(UPPER CASE)について参考リンク: https://www.javadrive.jp/start/string/index14.html   
printfの参考リンク: https://www.baeldung.com/java-printstream-printf#syntax

# 課題３

`greeting`にある文字にスペースがある場合は`greetingの値にスペースがあります！`というメッセージ表示してください。   
出力は下記のようになります。
```java
greetingの値にスペースがあります！
```
ここで使う(String.contains)Stringクラスのメソッドを知らない方はこちらのサイトを参考にしてください。   
参考リンク: https://www.w3schools.com/java/ref_string_contains.asp  

# 課題４の準備

下記のように`greeting2`というもう一つのString型変数を記述してください。
```java
public class Main {

  public static void main(String[] args) {
    String greeting = "Hello World";
    String greeting2 = "hello world";
  }

}
```

# 課題４

もし`greeting`と`greeting2`の値が同じで長さも等しいときは`"greetingとgreeting2が同じです。"`というメッセージを表示してください。   
出力は下記のようになります。
```java
greetingとgreeting2が同じです。
```
こちらで使う`&&`論理演算子はこちらのサイトを参考にしてください。   
論理演算子の参考リンク: https://www.javadrive.jp/start/ope/index12.html   

# 課題５の準備 

`worldIndex`というint型変数を記述してください。   
下記のように`worldIndex`の値は`greeting`から`World`のインデックスを取得して記載してください。
```java
public class Main {

  public static void main(String[] args) {
    String greeting = "Hello World";
    int worldIndex = _______; //こちらWorldのインデックスを取得して記載する
  }

}
```
greetingからWorldのインデックスを取得する方法: https://www.tohoho-web.com/java/string.htm#indexOf

# 課題５

もし`worldIndex`の値が5以上のときは`greeting`から`World`の文字を取得して表示してください。   
出力は下記のようになります。
```java
World
```
greetingからWorldの文字を取得する方法: https://www.javadrive.jp/start/string/index7.html   

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
