# クラスの課題

Javaのクラスの課題をやってみましょう。

# クラスの使い方

Javaのクラスの使い方についてはこちらのリンクを参考にしてください。   
Javaのクラスの使い方の参考リンク: [Javaのクラスの使い方]()

# 準備

`src/Main.java`には下記を記載してください。

```java
public class main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

}
```

# 課題１

次のような`BankAccount.java`ファイルを作ってください。

```java
import java.util.List;

public class BankAccount {

    private String accountNumber;
    private int balance;
    private List<String> transactionHistory;

}
```

# 課題２

`BankAccount`クラスには`accountNumber`と`balance`フィールドを引数として受けるコンストラクタを作成してください。   
`BankAccount`クラスは次のようになります。

```java
import java.util.List;
import java.util.ArrayList;

public class BankAccount {

    private String accountNumber;
    private int balance;
    private List<String> transactionHistory;

    public BankAccount(String accountNumber, int balance) {
        this.accountNumber = accountNumber;
        this.balance = balance;
        this.transactionHistory = new ArrayList<>();
    }

}
```

# 課題３

`accountNumber`、`balance`、`transactionHistory`フィールドのgetterメソッドを作成してください。今回はgetterだけで大丈夫です。   
getter&setterを作成する方法について参考リンク：[getter&setterを作成する方法](https://www.jetbrains.com/help/idea/generating-code.html#generate-getters-setters)

# 課題４

そして、`BankAccount`クラスに`withdraw`という整数型を引数として受ける何も返さないメソッドを作成してください。引数の名前は`amount`と宣言してください。   
`withdraw`メソッド内はもし`balance`の値は`amount`より小さい場合は`残高不足です`というメッセージを表示するようにしてください。   
それ以外は今の`balance`から`amount`を引いて`balance`に代入してください。   
`transaction`という文字列型を宣言し、その値として`"[" + LocalDate.now() + "] 出金 " + amount + "円";`を記載してください。   
`LocalDate.now()`を使うと`import java.time.LocalDate;`をインポートする必要があります。   
そして、`transaction`文字列を`transactionHistory`に追加してください。

# 課題５

`Main.java`に`bankAccounts`という名前で文字列型の`ArrayList`を宣言して以下のデータを代入してください。   
***`bankAccounts`に代入するデータ***   
```
1. 
  accountNumber - "2023001"
  balance - 300000

2. 
  accountNumber - "2023002"
  balance - 100000
```

# 課題６

キーボードから入力された文字列や数値を受け取ってプログラムの中で処理できるようにしましょう。   
キーボードから二つの値を入力させます。   
一つは`accountNumber`という文字列型ともう一つは`withdrawAmount`という整数型を入力できるようにしてください。   

出力は下記のようになります。   

出力例：

```java
銀行口座を入力してください： 2023001
引き出す金額を入力してください： 150000
```

# 課題７
  
ループを使って`bankAccounts`リストにあるデータからの`accountNumber`と入力された`accountNumber`と等しい`BankAccount`オブジェクトの`withdraw`メソッドを利用します。   
`withdraw`メソッドを呼び出すときは入力された`withdrawAmount`を引数として渡して呼び出してください。   
そのオブジェクトの`transactionHistory`を呼び出して返った値を`history`という文字列型のListを宣言して代入してください。   
そして、`history`にある値をループを使って表示するようにしてください。   

# テストしたデータ

アカウントには`2023001`、金額には`150000`を入力された場合の出力は下記のようになります。   
出力：

```java
[こちらはこのプログラムを実行するデートになります] 出金 150000円
```

アカウントには`2023002`、金額には`200000`を入力された場合の出力は下記のようになります。   
出力：

```java
残高不足です
```

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
