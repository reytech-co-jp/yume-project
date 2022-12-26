# do-whileの課題

Javaの繰り返し処理について次のdo-whileの課題をやってみましょう。

# do-while文の使い方

do-while文の使い方についてはこちらのリンクを参考にしてください。  

do-while文の使い方の参考リンク:https://github.com/reytech-co-jp/yume-project/blob/feature/loop_statment_questions/lessons/java/03-Java%E3%81%AE%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E5%95%8F%E9%A1%8C/Java%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#dowhile%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に`String`形変数`string`、`int`形変数`i`と`count`を宣言して`string`に"Learning java is fun"、`i`と`count`に0を代入してください。
```java
public class Main {

  public static void main(String[] args) {
    String string = "learning java is fun";  
    int i = 0;
    int count = 0;
    int whiteSpaceCount = 0;
  }

}
```

# 課題1

この課題では、`"learning java is fun"`文字列に含まれる空白を数える`do-while`コードを記載してください。

出力：

```java
【"learning java is fun"文字列の空白の数を表示する】

文字列の空白の数：3空白
```
ここで使う(String.length)Stringクラスのメソッドを知らない方はこちらのサイトを参考にしてください。  
参考リンク: <https://www.w3schools.com/java/ref_string_length.asp>  

String.charAt()について参考リンク: <https://www.w3schools.com/jsref/jsref_charat.asp>

# 課題2

この課題では、`"learning java is fun"`文字列に含まれる文字数を数える`do-while`コードを記載してください。  
文字数を数える時に空白を数えないように開発してほしいです。　　

出力：

```java
【"learning java is fun"文字列の文字数を表示する】

文字列の文字数：17文字
```

# 課題3

"Learning Java is fun"文字列内の単語数を数える`do-while`コードを追加してください。

出力：

```java
【"learning java is fun"文字列の単語数を表示する】

文字列の単語数：4語
```

# 課題4

"Learning Java is fun"文字列内の各単語を表示する`do-while`コードを追加してください。

出力：

```java
【"learning java is fun"文字列の各単語を表示する】

Learning
Java
is
Fun
```
String.split()について参考リンク: <https://www.w3schools.com/jsref/jsref_split.asp>

# 課題5
"Learning Java is fun"文字列の各単語を大文字にする`do-while`コードを追加してください。

出力：

```java
【"learning java is fun"文字列の各単語を大文字にする】
Learning Java Is Fun
```
大文字(UPPER CASE)について参考リンク: <https://www.w3schools.com/java/ref_string_touppercase.asp>  
String.substring()について参考リンク: <https://www.w3schools.com/jsref/jsref_substring.asp>

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
