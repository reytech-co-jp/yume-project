# if-elseの課題

Javaの条件についてまず`if-else`の課題をやってみましょう。  

# if-else文の使い方

`if-else`文の使い方についてはこちらのリンクを参考にしてください。  
`if-else`文の使い方の参考リンク: [if-else文の勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/02-Java%E3%81%AE%E6%9D%A1%E4%BB%B6%E5%95%8F%E9%A1%8C/.Java%E6%9D%A1%E4%BB%B6%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#ifelse)

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のようにint型の`num1`変数を宣言してください。  

```java
public class Main {

  public static void main(String[] args) {
    int num1 = -6;
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

# 課題2の準備

`Main.java`に下記のようにint型の変数`num2`という変数を宣言してください。  

```java
public class Main {

  public static void main(String[] args) {
    int num1 = -6;
    int num2 = 2;
  }

}
```

# 課題2

`if-else`文を使用して変数`num1`が`num2`より大きい場合は`【変数num1が変数num2より大きいです。】`と表示、`num2`が`num1`より大きい場合は`【変数num2が変数num1より大きいです。】`と表示するコードを記載してください。

出力は以下の通りになります。

出力：

```java
【変数num2が変数num1より大きいです。】
```

# 課題3の準備

`Main.java`に下記のようにint型の変数`length`, `width`という変数を宣言してください。  

```java
public class Main {

  public static void main(String[] args) {
    int length = 16;
    int width = 16;
  }

}
```


# 課題3

`if-else`を使用して変数`length`と変更`width`が等しい場合は、`【形は四角です。】`と表示、等しくない場合は`【形は長方形です。】`と表示するコードを記載してください。

出力は以下の通りになります。

出力：

```java
【形は四角です。】
```

# 課題4の準備

`Main.java`に下記のようにint型の`mark`変数を宣言してください。

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

# 課題5の準備

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

# 課題6の準備

`Main.java`に下記のように次の変数`date`という`Date`型変数とint形`hour`という変数を宣言してください。  
`Date`型のフォーマットは、日付をわかりやすく表示するために用意されています。  
`Date`型についの詳細を知りたい方はこちらのリンクを参考にしてください。  
`Date`型のフォーマットの使い方の参考リンク: [Date型の使い方](https://docs.oracle.com/javase/jp/8/docs/api/java/util/Date.html)

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

今の時間は12未満である場合は、`【午前{hour}時間です。】`と表示、今の時間は12未満ではない場合は、`【午後{hour}時間です。】`と表示するコードを追加してください！  

今は午前11時間なら出力は以下の通りになります。  

出力：

```java
【午後11時間です。】
```
