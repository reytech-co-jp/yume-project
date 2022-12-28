# 条件文の課題

Javaの条件文の課題をやってみましょう。

# switch文の使い方

switch文の使い方についてはこちらのリンクを参考にしてください。   
switchの使い方の参考リンク: https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#switch%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のように`day`というint型変数を記述してください。
```java
public class Main {

  public static void main(String[] args) {
    int day = 7;
  }

}
```
 
# 課題１   

`day`にある値によって曜日を表示してください。   
出力は下記のようになります。
```java
曜日 : 日曜日
```
もし、`day`に`1`を記載した場合は`月曜日`、`day`に`2`を記載した場合は`火曜日`という風に`day`にある値によって曜日を表示するように実装しましょう。

# 課題２ + α

下記のように`word`というString型変数を記述してください。
```java
public class Main {

  public static void main(String[] args) {
    String word = "apple";
  }

}
```

# 課題２

`word`にある文字列はvowelなら`Vowel`と表示し、vowelではない場合は`Consonant`かというメッセージを表示してください。   
vowel文字は`a,e,i,o,u`から始めます。   
今の`word`にある文字列なら出力の文書は下記のようになります。
```java
Vowel
```
Stringメソッドの参考リンク: https://java-code.jp/185   

# 課題３

`word`にある文字列を自分が好きなvowelではない文字列に変更してください。例えば、"pineapple"、"stawberry"。。。   
出力は下記のようになります。
```java
Consonant
```
defaultの参考リンク: https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#default%E3%83%A9%E3%83%99%E3%83%AB%E3%82%92%E5%88%A9%E7%94%A8%E3%81%99%E3%82%8B 

# 課題４ + α

下記のように`levelString`と`level`という二つの変数を記載してください。
```java
public class Main {

  public static void main(String[] args) {
    String levelString = "Expert";
    int level = 0;
  }

}
```

# 課題４

`levelString`によって`level`の値を記載するように実装しましょう。
1. `levelString`の文字は`Expert`の場合
   - `level`に`3`を記載します。
2. `levelString`の文字は`Intermediate`の場合
   - `level`に`2`を記載します。
3. `levelString`の文字は`Beginner`の場合
   - `level`に`1`を記載します。
4. それ以外の場合は
   - `level`に`0`を記載します。

出力は下記のようになります。
```java
Your Level is : {level}
```

# 宿題

***※この宿題はSlackに提出しなくても大丈夫です。***
