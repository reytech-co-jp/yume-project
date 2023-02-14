# Javaメソッドについて

クラスの主要な要素の一つがメソッドです。メソッドはクラスが持つ機能を定義するためのものです。ここではメソッドを関数のように使用する方法を使ってメソッドの基本的な利用方法を解説します。   
メソッドにはインスタンスメソッドとクラスメソッドと呼ばれるものがあり、ここではクラスメソッドについて利用方法を確認していきます。

# Javaメソッド

- メソッドって何？
- メソッドの使い方
- どのような場合にメソッドが使われる？

## メソッドって何？

メソッドはクラスの中に記述します。プログラムが実行される時に最初に呼び出されるメソッドである`main`メソッドがクラスの中に既に記述されているはずですが、新しく定義するメソッドも***クラスの`{`から`}`の中に記述します。***   
メソッドの書式は次のようになります。   

例：

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

  //Javaメソッドの例
  private static void testMethod(String text) {

  }

}

```

### アクセス修飾子について

アクセス修飾子はメソッドだけではなくフィールドやクラスにも付けるもので、そのメソッドがどこからアクセス可能なのかを示すアクセス修飾子と呼ばれるものです。

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

  ⇒[アクセス修飾子]⇐ [戻り値のデータ型] [メソッド名](引数1, 引数2, ....) {

  }

}

```

アクセス修飾子はpublic、private、static、finalなどです。詳しくは以下のリンクを読んでみてください。   
アクセス修飾子について参考リンク：[アクセス修飾子について](http://msugai.fc2web.com/java/modify.html)

### 戻り値のデータ型について

メソッドから呼び出し元へ返す値を戻り値といいます。   
戻り値のデータ型はメソッドが呼び出された時に値を一つだけ呼び出し元に返すことができます。その返す値のデータ型を指定します。何も値を返さない場合は`void`型を指定することになっています。   

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

  [アクセス修飾子] ⇒[戻り値のデータ型]⇐ [メソッド名](引数1, 引数2, ....) {

  }

}

```

戻り値のデータ型はString型を戻す関数の場合は下記のようになります   

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

  //Javaメソッドの例
  private static String testMethod(String text) {
    return {文字列の値};
  }

}

```

### メソッドの名前について

定義するメソッドには名前をつける必要があります。メソッド名は変数名と同じく識別子を使います。

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

  [アクセス修飾子] [戻り値のデータ型] ⇒[メソッド名]⇐ (引数1, 引数2, ....) {

  }
  
}

```

どのような名前を付けるべきかは以下のリンクを参考にして読んでみてください。   
メソッドの名前つける方法につして参考リンク：[メソッドの名前つける方法](https://www.javadrive.jp/start/var/index3.html#section2)

### メソッドの引数について

メソッド側では渡されてきた値を格納するために変数をメソッド名の後の括弧の中に記述します。この変数のことを引数と呼びます。引数は渡されてくる値の数だけ記述する必要があり、渡されてきる値と同じデータ型を使って宣言されている必要があります。   
メソッドの呼び出し元からメソッドに対して値を渡したい場合に引数を利用します。戻り値は一つだけでしたが、引数は複数個指定することができます。その場合はカンマ(,)で区切って記述していきます。   
引数が必要無い場合は何も記述する必要はありません。

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

  [アクセス修飾子] [戻り値のデータ型] [メソッド名] ⇒(引数1, 引数2, ....)⇐ {

  }
  
}

```

## メソッドの使い方

メソッドを定義したらプログラムの中から呼び出すことができます。そして、メソッドが呼び出された時に実行する処理を`{`から`}`のブロックの間に記述します。   

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

  [アクセス修飾子] [戻り値のデータ型] [メソッド名] (引数1, 引数2, ....) ⇒{

  }⇐
  
}

```

メソッドの種類によって呼び出し方は異なります。ただどんなメソッドでも定義されているメソッド名を指定して呼び出します。   

### 引数がないメソッドの使い方

引数がないメソッドは下記のように呼び出します。

```java
public class Main {

  public static void main(String[] args) {
    sayHello();
  }
  
  private static void sayHello() {
    System.out.println("Hello World");
  }

}

```

出力は以下のようになります。

```java
Hello World
```

### 引数があるメソッドの使い方

メソッドを呼び出す時にメソッドに渡したい値を括弧の間に記述します。引き数があるメソッドは下記のように引数の値を渡して呼び出します。

```java
public class Main {

  public static void main(String[] args) {
    sayHello("Hello World");
  }
  
  private static void sayHello(String text) {
    System.out.println(text);
  }

}

```

出力は以下のようになります。

```java
Hello World
```

複数の値を渡す場合はカンマ(,)で区切り続けて記述します。    
複数の引き数があるメソッドは下記のように引数の値を渡して呼び出します。

```java
public class Main {

  public static void main(String[] args) {
    sayHello("John", "Snow");
  }

  private static void sayHello(String firstName, String lastName) {
    System.out.println("Hello " + firstName + lastName);
  }

}

```

出力は以下のようになります。

```java
Hello John Snow
```

### 戻り値のデータがあるメソッドの使い方

戻り値としてreturn文の後に指定する値のデータ型はメソッド名の前に記述したデータ型である必要があります。   
戻り値のデータ型はメソッドが呼び出された時に値を一つだけ呼び出し元に返すことができます。その返す値のデータ型を指定します。   
戻り値のデータ型はメソッドは下記のように呼び出します。

```java
public class Main {

  public static void main(String[] args) {
    String say = sayHello();
    System.out.println(say);
  }

  private static String sayHello() {
    String say = "Hello World";
    return say;
  }

}

```

***or***

```java
public class Main {

  public static void main(String[] args) {
    System.out.println(sayHello());
  }

  private static String sayHello() {
    return "Hello World";
  }

}

```  

出力は以下のようになります。

```java
Hello World
```

return文が実行された時点でメソッドを終了し呼び出し元へ処理が帰ります。return文はメソッド内の任意の位置に記述できますが、return文が実行されるとそれ以降にメソッド内に書かれた処理は実行されませんので注意して下さい。   
次に例を見てください。

```java
public class Main {

  public static void main(String[] args) {
    int mark1 = 40;
    int mark2 = 80;
    String result1 = check(mark1);
    System.out.println(result1);

    String result2 = check(mark2);
    System.out.print(result2);
  }

  private static String check(int marks) {

    if (marks < 50) {
      return "Fail";
    } else {
      return "Pass";
    }

  }

}

```

出力は以下のようになります。

```java
Fail
Pass
```

メソッド内で条件分岐を行い、戻り値で返す値を二通り記述しています。このようにreturn文はメソッド内で複数記述しても構いません。ただ、いずれかのreturn文が実行されるとその時点でメソッドを終了するのでreturn文が実行されるのは一つだけです。

## どのような場合にメソッドが使われる？

メソッドは複数の処理をまとめたものです。同じような処理を行う複数の文が、プログラムの中で離れたところに記述されていた場合はメソッドを使うと便利です。   
次の例プログラムをみてください。

```java
public class Main {

  public static void main(String[] args) {
    int myanmarHour = 11;

    if (myanmarHour <= 12) {
      System.out.println("ミャンマーでは午前です");
    } else {
      System.out.println("ミャンマーでは午後です");
    }

    int japanHour = 13;

    if (japanHour <= 12) {
      System.out.println("日本では午前です");
    } else {
      System.out.println("日本では午後です");
    }

  }

}

```

if文が2回使われていますが条件式の中で使われている変数以外は同じです。上記では2回だけですがこれが3回も4回も同じような処理が記述されていくと無駄に長いプログラムとなってしまいます。   
メソッドは複数の処理をまとめたものです。プログラムの中からメソッドを呼び出すと、そのメソッドで記述された処理が実行されます。先ほどの例をメソッドを使って書き直すと次のようになります。

```java
public class Main {

  public static void main(String[] args) {
    int myanmarHour = 11;
    int japanHour = 13;

    check("ミャンマー", myanmarHour);
    check("日本", japanHour);

  }

  public static void getPeriod(String country, int hour) {

    if (hour <= 12) {
      System.out.println(country + "では午前です");
    } else {
      System.out.println(country + "では午後です");
    }

  }

}

```

「check」という名前のメソッドを一つ用意しました。このメソッドにはif文を使った画面出力の処理が記述されています。プログラム本体からは必要な時にこのメソッドを呼び出すと、メソッド内に記述された一連の処理が実行されることになります。   
このようにメソッドを使うことで何度も実行される一連の処理をひとまとめにしておき、必要に応じて呼び出して実行させることができるようになります。 

# まとめ

Javaのメソッドの勉強はこれで以上となります。次はメソッドを使って課題をやってみましょう。
