# 条件文の課題

Javaの条件文の課題をやってみましょう。

# else..if文の使い方

else..if文の使い方についてはこちらのリンクを参考にしてください。   
else..ifの使い方の参考リンク: [else..ifについての勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/if_else_statement_questions/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#elseif)

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のように`num`というint型変数を記述してください。
```java
public class Main {

  public static void main(String[] args) {
      int num = -10;
  }

}
```
 
# 課題１   

`num`にある値によってメッセージを表示するようにしましょう。
- `num`の値が0より大きい場合は`numの値は正数です。`というメッセージを表示してください。
- `num`の値が0より小さい場合は`numの値は負の数です。`というメッセージを表示してください。
- それ以外は`numの値はゼロです。`というメッセージを表示してください。

出力は下記のようになります。
```java
numの値は負の数です。
```

# 課題２+ α

下記のように`a`と`b`というint型変数を記述してください。
`division`には`a`割る`b`の値を代入しましょう。
```java
public class Main {

  public static void main(String[] args) {
      int a = 80;
      int b = 6;
      int division = ...;
  }

}
```

整数と整数の値を割る方法について参考リンク: https://www.javadrive.jp/start/ope/index1.html

# 課題２

`division`にある値によってメッセージを表示するようにしましょう。
- `division`の値が5より大きい、そして10より小さい場合は`divisionの値は5から10以内です。`というメッセージを表示してください。
- `division`の値が5より小さい場合は`divisionの値は5より小さいです。`というメッセージを表示してください。
- それ以外は`divisionの値は10以上です。`というメッセージを表示してください。

出力は以下のようになります。
```java
divisionの値は10以上です。
divisionの値: 13
```

# 課題３+ α

下記のように`modulus`には`a`と`b`の割った余り値を代入しましょう。
```java
public class Main {

  public static void main(String[] args) {
      int a = 80;
      int b = 6;
      int modulus = ...;
  }

}
```

整数と整数の値を割った余り方法について参考リンク: https://www.javadrive.jp/start/ope/index1.html


# 課題３

`modulus`にある値によってメッセージを表示するようにしましょう。
- `modulus`の値が0以上で、そして5より小さい場合は`modulusの値は0から5以内です。`というメッセージを表示してください。
- `modulus`の値が6以上で、そして10より小さい場合は`modulusの値は6から10以内です。`というメッセージを表示してください。
- それ以外は`modulusの値は10以上です。`というメッセージを表示してください。

出力は以下のようになります。
```java
modulusの値は0から5以内です。
modulusの値: 2
``` 

# 課題４+ α

下記のように`mark`というint型変数を記述してください。
```java
public class Main {

  public static void main(String[] args) {
    int mark = 65;
  }

}
```

# 課題４

`mark`にある値によってメッセージを表示するようにしましょう。
- `mark`にある値は50より小さい場合は`不合格`というメッセージを表示してください。
- `mark`にある値は50以上で、60より小さい場合は`Dグレード`というメッセージを表示してください。
- `mark`にある値は60以上で、70より小さい場合は`Cグレード`というメッセージを表示してください。
- `mark`にある値は70以上で、80より小さい場合は`Bグレード`というメッセージを表示してください。
- `mark`にある値は80以上で、90より小さい場合は`Aグレード`というメッセージを表示してください。
- `mark`にある値は90以上で、100より小さい場合は`A+グレード`というメッセージを表示してください。
- それ以外は`無効`というメッセージを表示してください。

出力は以下のようになります。
```java
Cグレード
```  

# 課題５

課題5として課題4に実装したコードをテストするため`mark`に値を変更して試してみてください。


# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
