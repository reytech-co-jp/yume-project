# Java配列について

配列を使用することで同じデータ型の複数の値をまとめて一つの変数として保管や管理することができます。  
配列は繰り返し処理と組み合わせることで、順番に並べられていて特定の値をを取り出して処理することもできます。  

# 配列の使い方

## 配列の宣言

配列を利用するためまず配列を宣言します。  
配列を利用するときにデータ型と配列名を指定して宣言を行います。  
配列の宣言は以下のように記述します。  

書き方：

```java
型名[] 配列変数名;
```

例えば`String`型の値を扱う配列であれば次のように宣言します。

例：

```java
String[] fruits;
```

## 配列の作成

配列の要素数という一つ一つの値を保管する場所の数を指定する場合は、以下のように記述します。  

書き方：

```java
型名 配列変数名[] = new 型名[要素数];
```

例えば配列`fruit`は4つの`String`型の値を扱う配列であれば次のように宣言します。

例：

```java
String[] fruits = new String[4];
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
String fruits[] = {"ブドウ", "リンゴ", "バナナ","イチゴ"};
```

## 配列の出力

 配列`fruits`の各データを表示するときに繰り返し文`for`や`for-each`を使用して特定のデータを出力することができます。

`for`を使用して出力すると書き方は次のように記述します。

書き方：

```java
String fruits[] = {"ブドウ", "リンゴ", "バナナ","イチゴ"};
System.out.print("【各果物を表示する】");
for (int i = 0; i < fruits.length; i++) {
   System.out.print(fruits[i] + ", ");
  }
```

`for-each`を使用して出力すると書き方は次のように記述します。

```java
String fruits[] = {"ブドウ", "リンゴ", "バナナ","イチゴ"};
System.out.print("【各果物を表示する】");
for (String fruit: fruits) {
  System.out.print(fruits[i] + ", ");
}
```

出力：

```java
【各果物を表示する】
ブドウ, リンゴ, バナナ, イチゴ
```

上記のコードで使う`length`メソッドは要素数を取得したいときに使います。  
上記のコードでの配列`fruits`の要素数は4です。  

こちらで使う繰り返し処理はこちらのサイトを参考にしてください。
繰り返し処理`for`の参考リンク：<https://github.com/reytech-co-jp/yume-project/blob/feature/loop_statment_questions/lessons/java/03-Java%E3%81%AE%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E5%95%8F%E9%A1%8C/Java%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9>  

繰り返し処理`for-each`の参考リンク：<https://github.com/reytech-co-jp/yume-project/blob/feature/loop_statment_questions/lessons/java/03-Java%E3%81%AE%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E5%95%8F%E9%A1%8C/Java%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#for-each%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9>


