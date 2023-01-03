# Scannerクラスについて

Scannerクラスはユーザからの入力を取得するためのクラスです。　　
キーボードから入力された文字列や数値やファイルなどを受け取り処理するのに`Scanner`クラスを使用します。

# Scannerクラスの使い方

Scannerクラスを使用できるため、まずインポート文として「`java.util.Scanner`」と、記述する必要があります。 

```java
import java.util.Scanner;
```
Scannerクラスは下記のようにインスタンスを生成してから利用します。
引数には標準入力を指定する場合は、標準入力ストリームを表す定義済みオブジェクト「System.in」を渡します。　

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
  //標準入力を取得
  Scanner scan = new Scanner(System.in);
  //ユーザに名前入力を促す
  System.out.println("【ご自身の名前をご入力ください。】");
  }
}
```
# nextメソッドについて

Scanner クラスの next メソッドは入力値を読み取る際に使うメソッドです。

以下のコードではキーボードでエンターキーが押されるまでに入力した文字列を変数`name`に格納します。

入力値を読み取る際に使うメソッドは複数あります。
文字列を空白まで読み取るためには以下のように， Scanner の next()メソッドを使います。  

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
  //標準入力を取得
  Scanner scan = new Scanner(System.in);
  //ユーザに名前入力を促す
  System.out.println("【ご自身の名前をご入力ください。】");
  //文字列を空白まで読み込んで格納する
  String name = scan.next();
  //名前を出力
  System.out.println("はじめまして，" + name + "さん。");
  }
}
```
出力：

```java
【ご自身の名前をご入力ください。】
木村　佳子
はじめまして、木村さん。
```

文字列を改行まで読み取るためには以下のように， Scanner の nextLine()メソッドを使います。

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
  //標準入力を取得
  Scanner scan = new Scanner(System.in);
  //ユーザに名前入力を促す
  System.out.println("【ご自身の名前をご入力ください。】");
  //文字列を改行まで読み込んで格納する
  String name = scan.nextLine();
  //名前を出力
  System.out.println("はじめまして，" + name + "さん。");
  }
}
```
出力：

```java
【ご自身の名前をご入力ください。】
木村　佳子
はじめまして、木村　佳子さん。
```

整数を読み取るためには以下のように Scanner の nextInt()メソッドを使います。
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
  //標準入力を取得
  Scanner scan = new Scanner(System.in);
  //ユーザに年齢入力を促す
  System.out.println("【ご自身の年齢をご入力ください。】");
  //整数を読み込んで格納する
  int age = scan.nextInt();
  //年齢を出力
  System.out.println("年齢は" + age + "でございます。");
  }
}
```

出力：

```java
【ご自身の年齢をご入力ください。】
21
年齢は21でございます。
```

浮動小数点数を読み取るためには Scanner の nextDouble()メソッドを使います。

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
  //標準入力を取得
  Scanner scan = new Scanner(System.in);
  //ユーザに身長入力を促す
  System.out.println("【ご自身の身長をご入力ください。】");
  //浮動小数点数を読み込んで格納する
  int height = scan.nextDouble();
  //身長を出力
  System.out.println("身長は" + height + "cmでございます。");
  }
}
```

出力：

```java
【ご自身の身長をご入力ください。】
168.34
身長は168.34cmでございます。
```
# まとめ

上記のようにJavaでは指定した型の値を読み込むのにScannerクラスを使用します。
ご自身でソースコードを書いて試してみてください。
