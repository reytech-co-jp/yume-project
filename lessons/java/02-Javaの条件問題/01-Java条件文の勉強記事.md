# Java条件文について
条件分岐を利用することで条件に応じて処理を分けることができます。   
条件式は結果としてboolean型の値を返す式であればどのように記述してもいいのですが、関係演算子や論理演算子を組み合わせて指定する場合が多いです。

# Java条件文
- if
- switch

## if文の使い方

### if

`if`文は条件式を評価して結果に応じて異なる処理を行う場合に使われます。   
`if`文では条件式を評価して`true`だった場合は`{`から`}`のブロック内に記述された処理を上から順番に実行します。条件式が`false`の場合はブロック内の処理は何も行わずに`if`文の次の処理へ進みます。
```java
public class Main {

  public static void main(String[] args) {
    int i = 2;
    

    if(i > 1) {
      // 条件式が true のときに実行される処理
      System.out.println("i is greater than 1.");
    }
  }
}

```
output :
```java
i is greater than 1.
```

### if...else

条件式が`true`の場合と`false`の場合にそれぞれ異なる処理を行いたい場合は次の書式を使用します。   
`if...else`文では条件式を評価して`true`だった場合には`if`のあとの`{`から`}`のブロック内に記述された処理を上から順番に実行します。条件式が `false`の場合は`else`のあとの`{`から`}`のブロック内に記述された処理を上から順番に実行します。
```java
public class Main {

  public static void main(String[] args) {
    int i = 2;
    
    if(i > 3) {
      // 条件式が true のときに実行される処理
      System.out.println("i is greater than 3.");
    } else {
      // 条件式が false のときに実行される処理
      System.out.println("i is less than 3.");
    }
  }
  
}

```
output :
```java
i is less than 3.
```

### if...elseの三項演算子

`if...else`文は三項演算子を使用しで1行に省略することができます。

上記の`if...else`コードを「条件(三項)演算子」で記述すると次のようになります。

```java
public class Main {

  public static void main(String[] args) {
    int i = 2;
    String result = (i > 3) ? "i is greater than 3." : "i is less than 3.";
    System.out.println(result);
  }
  
}
```

output :
```java
i is less than 3.
```

### else if

`if`文は`else if`文を組み合わせることで複数の条件式を使ってより細かい分岐を行うことができます。

条件式を評価して`if`文の条件1が`true`だった場合には`if`のあとの`{`から`}`のブロック内に記述された処理を上から順番に実行します。条件1が `false`で`else if`文の条件2が`true`だった場合は`else if`文のあとの`{`から`}`のブロック内に記述された処理を上から順番に実行します。すべての条件が`false`だった場合は`else`のあとの`{`から`}`のブロック内に記述された処理を上から順番に実行します。

基本的な書き方は以下の通りです。

```java
public class Main {

  public static void main(String[] args) {
    int age = 21;
    if(age < 18) {
      // 条件式1が true のときに実行される処理
      System.out.println("【未成年です】");
    } else if(age < 60) {
      // 条件式1が false で条件式2が true のときに実行される処理
      System.out.println("【大人です】");
    } else {
      // すべての条件式が false のときに実行される処理
      System.out.println("【高齢者です】");
    }
  }
  
}

```
output :
```java
【大人です】
```

### ネストしたif

if文の条件の中で、さらに条件を追加したい場合if文のブロック内に別のif文を記述することができます。

以下のコードで外側のif文が達成してネストしたif文内の条件式が成立せずに、内側のelseブロック内のメッセージが出力されることを確認します。

```java
public class Main {

  public static void main(String[] args) {
    int a = 202;
    if (a >= 0) {
      System.out.print("変数aは正数で");
      if (a <= 100) {
        System.out.println("100以下です。");
      } else {
        System.out.println("100より大きいです。");
      }
    } else {
      System.out.println("変数aは負数です");
    }

  }
  
}
```

output :

```java
変数aは正数で100より大きいです。
```

## switch文の使い方

### defaultラベルを利用しない

switch文は式を評価した値を、複数の値の候補と比較して一致したラベルへ処理を移すことができます。   
switch文では最初に式を評価します。そして`case`の後に記述されたラベルの値と一致したものがあった場合に、そのラベルの位置へ処理を移します。
```java
public class Main {

  public static void main(String[] args) {
    int num = 2;

    switch(num) {
      case 1:
        System.out.println("Aクラス");
        break;
      case 2:
        System.out.println("Bクラス");
        break;
      case 3:
        System.out.println("Cクラス");
      }
  }
  
}

```
switch文で変数`num`の値を評価し、値が1、または2、または3だった場合に、そのラベルの位置へ処理を移動します。今回の場合は変数が2なので、ラベル2の位置へ移動したあと`「Bクラス」`と画面に出力し、そのあとの`break;`文でswitch文を終了します。   
output :
```java
Bクラス
```

### defaultラベルを利用する

switch文で`default`ラベルを使用すると、式を評価した値がいずれのラベルとも一致しない場合のラベルとして使用することができます。
```java
public class Main {

  public static void main(String[] args) {
    int num = 7;

    switch(num) {
      case 1:
        System.out.println("Aクラス");
        break;
      case 2:
        System.out.println("Bクラス");
        break;
      case 3:
        System.out.println("Cクラス");
      default:
        System.out.println("－－－－");
      }
  }
  
}

```
変数`num`の値を評価し、 1か2か3であった場合はそれぞれ対応するラベルの位置へ処理が移りますが、それ以外の場合は `default`ラベルの位置へ処理が移ります。   
output :
```java
－－－－
```
