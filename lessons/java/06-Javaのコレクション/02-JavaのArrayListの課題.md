# ArrayListの課題

JavaのArrayListについて次の課題をやってみましょう。

# ArrayListの使い方

ArrayListの使い方についてはこちらのリンクを参考にしてください。

ArrayListの使い方の参考リンク: [ArrayListの勉強記事]()

# お願い

こちらの課題は新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のように`numList`という整数型のArrayListを宣言してください。   
 
```java
import java.util.ArrayList;
import java.util.List;

public class Main {

  public static void main(String[] args) {
    List<Integer> numList = new ArrayList<>();

  }
   
}
```

# 課題1

繰り返しを使って`numList`にデータを代入します。繰り返しでは初期化式を1からスタートし、5回目に終わるようにしてください。つまり`for (int i = 1; i <= 5; i++)`となります。   
繰り返し以内には初期化式の値によって`numList`にデータを代入してください。   
- 初期化式の1回目は初期化式の値、例えば`i`の値を20とかけてください。
- 初期化式の2回目は初期化式の値を15と足してください。
- 初期化式の3回目は初期化式の値を10と足してください。
- 初期化式の4回目は初期化式の値を50と足してください。
- 初期化式の5回目は初期化式の値を2と引いてください。

繰り返し以内はifやswitchなど自分が好きな方法で実装してください。   
そして、`numList`に代入した値を表示してください。   
  
出力は次のようになります。  

出力：

```java
【numListに代入された値】
[20, 17, 13, 54, 3]
```

# 課題2

`numList`の最初の値と最後の値をかけてその値を`numList`のインデックス2に代入して`numList`に代入した値を表示してください。   

出力は以下のようになります。     
出力：

```java
【かけ算を代入した後のnumListの値】
[20, 17, 60, 13, 54, 3]
```

インデックスに追加する方法の参考リンク： [インデックスに追加する方法](https://codechacha.com/ja/java-collections-arraylist-add/#2-1%E3%80%82-arraylistaddint-index%E3%80%81e-e%E3%81%AE%E4%BE%8B)

# 課題3の準備 

`Main.java`に`birthdays`という整数型のArrayListと`currentYear`とう整数型変数を宣言してください。   
LocalDateTimeクラスのnow()メソッドを使用し、getYear()メソッドを使って今の年を取得して`currentYear`に代入します。   

```java
import java.util.ArrayList;
import java.util.List;
import java.time.LocalDateTime;

public class Main {

  public static void main(String[] args) {
    List<Integer> birthdays = new ArrayList<>();
    int currentYear = LocalDateTime.now().getYear();

  }
   
}
```

そして、`birthdays`に`1998`、`1999`、`2000`、`2050`という要素を追加してください。   
現在の年を取得する方法について参考リンク: [日付の情報を単位別に取得する](https://flytech.work/blog/11832/)

# 課題3

`birthdays`にある各値を計算して年齢を表示してください。だたし、今の年より大きい年の場合は`Invalid`と表示するようにしてください。   
そして、繰り返しの初期化式の値によって出力してください。   
- 初期化式の値は0の場合は`Aさんは{birthdays}歳です。`
- 初期化式の値は1の場合は`Bさんは{birthdays}歳です。`
- 初期化式の値は2の場合は`Cさんは{birthdays}歳です。`
- 初期化式の値は3の場合は`Dさんは{birthdays}歳です。`

初期化式の値によって出力する場合はifやswitchなど自分が好きな方法で実装してください。   

出力は以下のようになります。   
出力：

```java
【年齢を計算して表示】
Aさんは 25歳です。
Bさんは 24歳です。
Cさんは 23歳です。
Invalid
```

# 課題4

`birthdays`にある値の中で現在の年より大きい年を削除して`birthdays`を表示してください。   

出力は以下の通りになります。   
出力：

```java
【現在の年より大きい年を削除した後のbirthdaysの値】
[1998, 1999, 2000]
```

ArrayListのデータを削除する方法について参考リンク：[インデックス番号で削除](https://nagablog.info/java-beginner-array-operation/#i-8)

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
