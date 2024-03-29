# Java配列について
# 配列

配列を使用することで同じデータ型の複数の値をまとめて一つの変数として保管や管理することができます。  
配列は繰り返し処理と組み合わせることで、順番に並べられていて特定の値をを取り出して処理することもできます。  
Javaの配列では配列と多次元配列という2つの種類があります。

# 多次元配列

配列の要素には数値や文字列の値だけでなく別の配列を格納することができます。
配列の要素に別の配列が格納されている配列を2次元配列、さらに配列の要素に別の2次元配列が格納されている配列を3次元配列などと呼びます。

# 配列の使い方

## 配列の宣言

配列を利用するためまず配列を宣言します。  
配列を利用するときにデータ型と配列名を指定して宣言を行います。  
配列の宣言は以下のように記述します。  

書き方：

```java
型名[] 配列変数名;
```
or
```java
型名 配列変数名[];
```

例えば`String`型の値を扱う配列であれば次のように宣言します。

例：

```java
String[] fruits;
```
or
```java
String fruits[];
```

## 配列の作成

配列の要素数という一つ一つの値を保管する場所の数を指定する場合は、以下のように記述します。  

書き方：

```java
型名[] 配列変数名 = new 型名[要素数];
```
or
```java
型名 配列変数名[] = new 型名[要素数];
```

例えば配列`fruit`は4つの`String`型の値を扱う配列であれば次のように宣言します。

例：

```java
String[] fruits = new String[4];
```
or
```java
String fruits[] = new String[4];
```

## 配列の各要素への値の代入

配列の要素へ値を代入するときにインデックスという配列の何番目かを表す数値を使用して代入します。  

インデックスは0から始まります。  

配列の要素へ値を代入するには次のように記述します。  

書き方：

```java
String[] fruits = new String[4];
fruits[0] = "バナナ";
fruits[1] = "リンゴ";
fruits[2] = "ブドウ";
fruits[3] = "イチゴ";
```

配列で宣言と同時に値を代入して初期化することもできます。  
宣言と同時に初期化するには、次のように記述します。

書き方：

```java
String[] fruits = {"ブドウ", "リンゴ", "バナナ","イチゴ"};
```

## 配列の出力

配列ではインデックスを指定して要素を取得することができます。  

書き方は次のように記述します。  

書き方：

```java
String fruits[] = {"ブドウ", "リンゴ", "バナナ","イチゴ"};
System.out.println("【0インデックスで格納する果物を表示する】");
System.out.println(fruits[0]);
```
出力：

```java
【0インデックスで格納する果物を表示する】
ブドウ
```

 配列`fruits`の各データを表示するときに繰り返し文`for`や`for-each`を使用して特定のデータを出力することができます。

`for`を使用して出力すると書き方は次のように記述します。

書き方：

```java
String fruits[] = {"ブドウ", "リンゴ", "バナナ","イチゴ"};
System.out.println("【各果物を表示する】");
for (int i = 0; i < fruits.length; i++) {
   System.out.println(fruits[i]);
  }
```

`for-each`を使用して出力すると書き方は次のように記述します。

```java
String fruits[] = {"ブドウ", "リンゴ", "バナナ","イチゴ"};
System.out.println("【各果物を表示する】");
for (String fruit: fruits) {
  System.out.println(fruit);
}
```

出力：

```java
【各果物を表示する】
ブドウ
リンゴ
バナナ
イチゴ
```

上記のコードで使う`length`メソッドは要素数を取得したいときに使います。  
上記のコードでの配列`fruits`の要素数は4です。  

こちらで使う繰り返し処理はこちらのサイトを参考にしてください。  
繰り返し処理`for`の参考リンク：[for文の勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/loop_statment_questions/lessons/java/03-Java%E3%81%AE%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E5%95%8F%E9%A1%8C/Java%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9)  

繰り返し処理`for-each`の参考リンク：[for-each文の勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/loop_statment_questions/lessons/java/03-Java%E3%81%AE%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E5%95%8F%E9%A1%8C/Java%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#for-each%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9)

# 多次元配列の使い方

この記事では2次元の配列の使い方について解決していきます。

## 多次元配列の宣言

2次元の配列を使うためには、その準備として配列を宣言する必要があります。  
2次元配列の書式は次の通りです。  

書き方：

```java
データ型[][] 配列変数名;
```
or
```java
データ型 配列変数名[][];
```
or
```java
データ型[] 配列変数名[];
```
例えば "int 型の値を要素に格納する配列"を要素に格納する配列であれば次のように宣言します。

例：
```java
int[][] mark;
```
or
```java
int mark[][];
```
or
```java
int[] mark[];
```
## 多次元配列の作成

2次元の配列を作成するときに次の書式が利用できます。

書き方：

```java
データ型[要素数1][要素数2] 配列変数名 = new データ型[要素数1][要素数2];
```
`要素数1`は別の配列を要素の値として格納する外側の配列の要素数であり、`要素数2`は配列に格納される内側の配列の要素数です。  

例えばint 型の4つの値を要素に格納する配列を要素に格納する外側の配列で要素数が2の内側の配列を作成する書き方は次のように記述します。  

```java
int[][] mark = new int[2][4];
```
## 多次元配列の各要素への値の代入

多次元配列を作成が終わっているのでそれぞれの要素に対して int 型の値を代入してみましょう。
書式は次の通りになります。

書き方：

```java
int[][] mark = new int[2][4];

num[0][0] = 97;
num[0][1] = 98;
num[0][2] = 95;
num[0][3] = 100;

num[1][0] = 74;
num[1][1] = 72;
num[1][2] = 30;
num[1][3] = 66;
```

多次元配列の宣言と同時に値を代入して初期化するには、次のように記述します。  

書き方：

```java
int mark[][] = {
    { 97, 98, 95, 100 },
    { 74, 72, 30, 66 },
};
```
## 多次元配列の出力

配列でインデックスを指定して要素を取得する書き方は次のように記述します。 

書き方：

```java
int mark[][] = = {
    { 97, 98, 95, 100 },
    { 74, 72, 30, 66 },
};
System.out.println("【(0,1)インデックスで格納するマークを表示する】");
System.out.println(num[0][1]);
```

出力：

```java
【(0,1)インデックスで格納するマークを表示する】
98
```
 繰り返し`for`文を使用して2次元配列`mark`の各データを取得する書き方は次のように記述します。 
 
 書き方：
 
 ```java
 int mark[][] = {
    { 97, 98, 95, 100 },
    { 74, 72, 30, 66 },
};
System.out.println("【2次元配列`mark`の各データを表示する】");
 for (int i = 0; i < mark.length; i++) {
      for (int j = 0; j < mark[i].length; j++) {
        System.out.println("mark[" + i + "][" + j + "] = " + mark[i][j]);
      }
 }
 ```
 
 出力：
 
 ```java
 【2次元配列`mark`の各データを表示する】
mark[0][0] = 97
mark[0][1] = 98
mark[0][2] = 95
mark[0][2] = 100
mark[1][0] = 74
mark[1][1] = 72
mark[1][2] = 30
mark[1][3] = 66
 ```
