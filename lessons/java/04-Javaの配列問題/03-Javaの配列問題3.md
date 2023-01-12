# 配列の課題

Javaの配列の課題をやってみましょう。

# 配列について

配列についてはこちらのリンクを参考にしてください。   
配列の参考リンク: [配列について勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/array_statement_questions/lessons/java/04-Java%E3%81%AE%E9%85%8D%E5%88%97%E5%95%8F%E9%A1%8C/Java%E9%85%8D%E5%88%97%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#java%E9%85%8D%E5%88%97%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のように`text`というString型の変数を記述してください。   
```java
public class Main {

  public static void main(String[] args) {
      String text = "This is array test";
  }

}
```

# 課題１

`textArray`というString型の配列を記載してください。   
`text`にある文字列を<strong>空白</strong>部分で分割して`textArray`に入力してください。
```java
public class Main {

  public static void main(String[] args) {
      String text = "This is array test";
      String[] textArray = ....
  }

}
```
文字列を分割するsplitメソッドの参考リンク: https://java-code.jp/799   

そして、`textArray`に格納した値を表示してください。   
出力は以下のようになります。
```java
【textArrayのデータ】
This
is
array
test
```

# 課題２

`textArray`に格納した値の中で`i`がない文字列だけを大文字にして表示してください。   
出力は以下のようになります。
```java
【'i'がない文字列】
ARRAY TEST
```
contains()のメソッドについて参考リンク: https://www.sejuku.net/blog/19257   
System.out.print()メソッドについて参考リンク: https://uxmilk.jp/48801   
文字列を大文字する方法: https://www.sejuku.net/blog/50886

# 課題３ 

`textArray`に格納した値の中で長さが４より大きい文字列だけを大文字して表示してください。   
出力は以下のようになります。
```java
【長さが４より大きい文字列】
ARRAY
```
大文字にする方法: https://www.sejuku.net/blog/50886

# 課題４

もし、`textArray`の長さは4以上の場合は`textArray`に格納した値を空白をつけて文字列のように表示してください。
```java
【textArrayの長さは4以上です】
{textArrayに格納した値を空白をつけて文字列のように表示する}
```
それ以外は以下のように表示してください。
```java
【textArrayの長さは4未満です】
```

出力は以下のようになります。
```java
【textArrayの長さは4以上です】
This is array test
```
文字列を連結する方法: https://www.sejuku.net/blog/19307

# 課題５+ α 

下記のように`vowels`というString型の配列を記載してください。
```java
public class Main {

  public static void main(String[] args) {
      String[] vowels = {"o", "a", "i", "u", "e"};
  }

}
```

# 課題５

`vowels`にある値を並べ替えてカンマをつけて表示してください。   
出力は以下のようになります。
```java
【vowelsを並べ替えて表示する】
a,e,i,o,u
```
配列を並べ替える方法: https://programmer-life.work/java/arrays-sort
String型の配列を指定した場合のjoinメソッドの使用方法: https://www.sejuku.net/blog/19307

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
