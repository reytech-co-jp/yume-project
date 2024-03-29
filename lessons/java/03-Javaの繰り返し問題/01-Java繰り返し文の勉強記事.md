# Java繰り返し文について
繰り返し処理は、指定した回数や条件を満たしている間は同じ処理を何回もやることができます。  
Java では 繰り返し処理を行うため、for 文、 while 文、 do while 文、拡張 for 文が用意されています。

# Java繰り返し文
- for
- while
- do-while
- for-each

## 繰り返し文の使い方
### for

`for`文は決められた回数だけ処理を繰り返す時に使用されます。  
書式は次の次のサンプル通り書きます。  
`for`文を使うため3つの引数が必要です。 

- 初期化式 (for 文が実行されるときに最初に1度だけ実行される式)
- 条件式 (forブロック内の処理を繰り返し行う条件)
- 変化式 (ループ処理が終わるたびに実行され、継続条件式で使用している変数の値を増加させる式)

```java
for (int i = 0; i < 5; i++) {
   // 繰り返しの中で実行される処理
  System.out.println("Number " + i);
}

```
出力：
```
Number 0
Number 1
Number 2
Number 3
Number 4
```
上記の例では、「i」に0を代入し、条件「i < 5」が成立している場合はそのまま繰り返し処理を実行します。  
そして、「i」に1ずつ加算し、条件式が成立しなくなるまで繰り返しを行います。

#### ネストしたforループ

for文のブロック内に別のfor文を記述することができます。  

```java
for (int i = 1; i < 5; i++) {
  for (int j = 1; j < 5; j++) {
    System.out.println("i = " + i + ", j = " + j);
  }
}
```

出力：
```java
i = 1, j = 1
i = 1, j = 2
i = 1, j = 3
i = 2, j = 1
i = 2, j = 2
i = 2, j = 3
i = 3, j = 1
i = 3, j = 2
i = 3, j = 3

```
### while文の使い方

`while` 文は回数を決めずに条件が`true`の場合に処理が繰り返されます。  
条件が `true` だった場合にはwhileブロック内に記載された処理を上から順番に実行し、`false` だった場合には繰り返し処理を終了します。  
最初の条件式が `false` となった場合には繰り返し処理が一回も行われません。

```java
public class Main {
 
    public static void main(String[] args) {
        int i = 1;
        while (i < 4) {
            System.out.println(i + "回目の処理です");
            i++;
        }
    }
}
```

出力：
```java
1回目の処理です

2回目の処理です

3回目の処理です
```
上記の例では「i」が4未満であれば処理を繰り返します。  
1回ごとの処理で「i」に1ずつ加算する処理を行っていますので、4回処理を繰り返すと条件を満たさなくなって処理が終了します。

### do-while文の使い方

`do-while` 文ではブロック内の処理を1度は上から順番に実行したあと、条件が`true`だった場合には繰り返し処理を行い、`false` だった場合には繰り返し処理を終了し ます。  
`do-while`文はfor文や`while`文と異なり必ず一回は繰り返し処理を行います。  

```java
public class Main {
 
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println(i + "回目の処理です");
            i++;
        } while (i < 4);
    }
}
```

出力：
```java
1回目の処理です

2回目の処理です

3回目の処理です
```
上記の例ではまず1回はブロック内の処理を行います。  
1回ごとの処理で「i」に1ずつ加算する処理を行っていますので、4回処理を繰り返すと条件を満たさなくなって処理が終了します。

### for-each文の使い方
for-each 文は他の繰り返しを行う文とは異なり条件式がありません。
配列やコレクションの全要素に対して、順番に処理を行います。

```java
String fruits[] = {"ブドウ", "リンゴ", "バナナ","イチゴ"};

for (String fruit: fruits) {
  System.out.println(fruit);
}
```
出力：
```java
ブドウ

リンゴ

バナナ

イチゴ
```
結果的に繰り返し処理を 4 回行い、それぞれ ブドウ、リンゴ、バナナとイチゴ を画面に出力します。
