# if-elseの課題

Javaの条件についてまず`if-else`の課題をやってみましょう。  

# if-else文の使い方

`if-else`文の使い方についてはこちらのリンクを参考にしてください。  
`if-else`文の使い方の参考リンク: [if-else文の勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#ifelse)

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のようにint形の`num1`変数を宣言してください。  

```java
public class Main {

  public static void main(String[] args) {
    int num = 6;
  }

}
```

# 課題1

変数`num1`は数値は0より小さいなら`【数値は負の整です！】`と表示、変数`num1`は数値は0以上であるなら`【数値は正の整です！】`と表示するコードを開発してください。  

出力は以下の通りになります。  

出力：

```java
【数値は負の整です！】
```

# 課題2+ α

`Main.java`に下記のようにint形の変数`num2`, `num3`, `smallest`と`largest`という変数を宣言してください。  

```java
public class Main {

  public static void main(String[] args) {
    int num1 = 6;
    int num2 = 2;
    int num3 = 4;
    int smallest;
    int largest;
  }

}
```

# 課題2

`if-else`文を使用してこちらの3つの変数中で最小値を見つけて`smallest`変数に最小値を代入してください。

出力は以下の通りになります。

出力：

```java
【6,2,4の中で最小値は2です。】
```

# 課題3

`if-else`文を使用してこちらの3つの変数中で最大値を見つけて`largest`変数に最大値を代入してください。

出力は以下の通りになります。

出力：

```java
【6,2,4の中で最大値は6です。】
```

# 課題4+ α

`Main.java`に下記のようにint形の`mark`変数を宣言してください。

```java
public class Main {

  public static void main(String[] args) {
    int mark = 100;
  }

}
```

# 課題4

マークは80以上の場合は、`【合格おめでとうございます！】`と表示、マークは80未満である場合は`【申し訳ございませんが不合格です！】`と表示するコードを追加してください。この処理を開発する時は、`if..else`の三項演算子を使用してください。

`if..else`の三項演算子について分からない場合はこちらのサイトを参考にしてください。  
`if..else`の三項演算子の参考リンク：[if..elseの三項演算子の勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/if_else_statement_questions/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#ifelse%E3%81%AE%E4%B8%89%E9%A0%85%E6%BC%94%E7%AE%97%E5%AD%90)

出力は以下の通りになります。

出力：

```java
【合格おめでとうございます！】
```

# 課題5+ α

`Main.java`に下記のように`email`,`password`という`String`型である2つの変数を宣言してください。

`email`変数に”user@gmail.com”、`password`変数に”12345”を代入してください。

```java
public class Main {

  public static void main(String[] args) {
    String username = "user@gmail.com";
    String password = "12345";
  }

}
```

# 課題5

`email`がadmin@gmail.comと`password`が12345である場合、`【ログインが成功しました！】`というメッセージを表示してください。  
`email`がadmin@gmail.comと`password`が12345ではない場合は、`【メールアドレスまたはパスワードが正しくありません！】`と表示するコードを追加してください。  

出力は次の通りになります。  

出力：

```java
【メールアドレスまたはパスワードが正しくありません。】
```

# 課題6+ α

`Main.java`に下記のように次の変数`date`という`Date`型変数とint形`hour`という変数を宣言してください。  
`Date`型のフォーマットは、日付をわかりやすく表示するために用意されています。  
`Date`形についの詳細を知りたい方はこちらのリンクを参考にしてください。  
`Date`型のフォーマットの使い方の参考リンク: [Date形の使い方](https://www.sejuku.net/blog/21098)

```java
import java.util.Date;
public class Main {

  public static void main(String[] args) {
    Date date = new Date();
    int hour = date.getHours();
  }

}
```

# 課題6

今の時間は1時から12時の間にある場合は、`【おはようございます！今は_時間です。】`と表示、  
今の時間は12時から16時の間にある場合は、`【こんにちは！今は_時間です。】`と表示、  
今の時間は16時から21時の間にある場合は、`【こんばんは！今は_時間です。】`と表示、  
今の時間は21時以降である場合は、`【おやすみなさい！今は_時間です。】`と表示するコードを追加してください！  

課題6を開発するため条件文`else..if`を使用しますのでこれについて分からない場合はこちらのサイトを参考にしてください。
`else..if`文の参考リンク：[`else..if`文の勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/if_else_statement_questions/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#elseif)

今は6時間なら出力は以下の通りになります。  

```java
【おはようございます！今は6時間です。】
```
