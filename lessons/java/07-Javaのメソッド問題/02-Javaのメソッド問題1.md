# メソッドの課題

Javaのメソッドの課題をやってみましょう。

# メソッドについて

メソッドについてはこちらのリンクを参考にしてください。   
メソッドの参考リンク: [メソッドについて勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/07-Java%E3%81%AE%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E5%95%8F%E9%A1%8C/01-Java%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md)

# 準備

まずはキーボードから入力された文字列や数値を受け取ってプログラムの中で処理できるようにしましょう。
入力された値を`num`という整数型に代入してください。   
次のようになります。

```java
import java.util.Scanner;

public class Main {

  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("整数を入力してください");
    int num = scanner.nextInt();

    System.out.println("【numの値の二乗値を計算する】");
    //課題1の実装したメソッドを呼び出す

  }

}
```

# 課題１

`num`の値の二乗値を計算してその値を戻すメソッドを作成ましょう。   
そのメソッドをmainから呼び出して戻った値を`square`という整数型に代入して表示してください。   
入力した値は4の場合出力は下記のようになります。
```java
【numの値の二乗値を計算する】
numの値の二乗値: 16
```

# 課題２の準備

課題２の形式は下記のようになります。
```java
import java.util.Scanner;

public class Main {

  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("整数を入力してください");
    int num = scanner.nextInt();

    System.out.println("【numの値の二乗値を計算する】");
    //課題1の実装したメソッドを呼び出す

    System.out.println("【numの値の三乗値を計算する】");
    //課題2の実装したメソッドを呼び出す

  }

}
```

# 課題２

`num`の値の三乗値を計算してその値を戻すメソッドを作成しましょう。   
そのメソッドをmainから呼び出して戻った値を`cube`という整数型に代入して表示してください。   
入力した値は4の場合出力は下記のようになります。
```java
【numの値の三乗値を計算する】
numの値の三乗値: 64
```

# 課題３の準備 

課題３の形式は下記のようになります。   
```java
import java.util.Scanner;

public class Main {

  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("整数を入力してください");
    int num = scanner.nextInt();

    System.out.println("【numの値の二乗値を計算する】");
    //課題1の実装したメソッドを呼び出す

    System.out.println("【numの値の三乗値を計算する】");
    //課題2の実装したメソッドを呼び出す

    System.out.println("【numの値の階乗値を計算する】");
    //課題3の実装したメソッドを呼び出す

  }

}
```

# 課題３

`num`の値の階乗値を計算してその値を戻すメソッドを作成ましょう。   
そのメソッドをmainから呼び出して戻った値を`factorial`という整数型に代入して表示してください。   
入力した値は5の場合出力は下記のようになります。

```java
【numの値の階乗値を計算する】
num!は 120 です。
```

階乗値について参考リンク: [階乗値について](https://www.mathsisfun.com/numbers/factorial.html)

# 課題４の準備

課題４の形式は下記のようになります。 
```java
import java.util.Scanner;

public class Main {

  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    System.out.println("整数を入力してください");
    int num = scanner.nextInt();

    System.out.println("【numの値の二乗値を計算する】");
    //課題1の実装したメソッドを呼び出す

    System.out.println("【numの値の三乗値を計算する】");
    //課題2の実装したメソッドを呼び出す

    System.out.println("【numの値の階乗値を計算する】");
    //課題3の実装したメソッドを呼び出す

    System.out.println("【numの値が素数かどうか確認する】");
    //課題4の実装したメソッドを呼び出す

  }

}
```

# 課題４

`num`の値が素数かどうかを確認するboolean型を戻すメソッドを作成してください。   
そのメソッドをmainから呼び出して戻った値を`isPrime`というboolean型に代入して表示してください。   
`isPrime`の値がtrueの場合出力は下記のようになります。
```java
【numの値が素数かどうか確認する】
numは素数です。
```

`isPrime`の値がfalseの場合出力は下記のようになります。
```java
【numの値が素数かどうか確認する】
numは素数ではありません。
```

入力した値は5の場合出力は下記のようになります。
```java
【numの値が素数かどうか確認する】
numは素数です。
```

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
