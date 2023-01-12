# whileの課題
Javaの繰り返し処理について次のwhileの課題をやってみましょう。

# while文の使い方
while文の使い方についてはこちらのリンクを参考にしてください。  
while文の使い方の参考リンク: [while文の勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/loop_statment_questions/lessons/java/03-Java%E3%81%AE%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E5%95%8F%E9%A1%8C/Java%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%96%87%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#while%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9)

# 準備

`Main.java`に`int`形変数`i`を宣言して`num`に100を代入してください。

```java
public class Main {

  public static void main(String[] args) {
    int i = 100;
  }

}
```

# 課題1
100から10までの数値を10づつ引いて表示するコードを追加してください。  

出力は下記のようになります。

出力：

```java
【100から10までの数字を10づつ減算して降順で表示する】
100
90
80
70
60
50
40
30
20
10
```

# 課題2
100から10までの数字を10づつ加算して表示するときに`i`は40である場合、処理を中断してください。  

出力は下記のようになります。

出力：

```java
【100から10までの数字を10づつ減算してiは40である場合、処理を中断してで表示する】
100
90
80
70
60
50
```
こちらのコードを作成するためbreak文を使用してください。  
break文の参考リンク：[break文の使い方](https://www.javadrive.jp/start/for/index9.html)

# 課題3
10から100までの数字を10づつ加算して合計を計算するコードを追加してください。  

出力は下記のようになります。

出力：
```java
【10から100までの数字10づつ加算して合計を表示する】
10+20+30+40+50+60+70+90+100 = 550
```

# 課題4+ α
`Main.java`に`int`形の変数`count`と`long`形の変数`digit`を宣言して`count`に0、`digit`に542981を代入してください。  

```java
public class Main {

  public static void main(String[] args) {
    int count = 0;
    long digit = 542981;
  }

}
```

# 課題4

`while`文を使用して指定された整数の桁数を数えるコードを記載してください。  

出力は下記のようになります。

出力：

```java
【整数542981の総桁数を表示する】
542981の総桁数：6
```

# 課題5

`while`文を使用して指定された整数の桁`542981`の合計を表示するコードを記載してください。  

出力は下記のようになります。  

出力：

```java
【整数542981の合計を表示する】
542981の合計：29
```

# 課題6+ α

`Main.java`に2つの変数`num`と`limit`を宣言して`num`に97、`limit`に122を代入してください。
```java
public class Main {

  public static void main(String[] args) {
    int num = 97;
    int limit = 122;
  }

}
```
# 課題6
aからzまでのアルファベットを昇順に表示するプログラムを追加してください。  

出力は下記のようになります。  

出力：

```java
【aからzまでの数字を昇順で表示する】
a
b
c
d
e
f
g
h
i
j
k
l
m
n
o
p
q
r
s
t
u
v
w
x
y
z
```
こちらのコードを作成するためASCII 文字を使います。  
ASCII 文字について知らない方はこちらのリンクを参考にして読んでみてください。  
ASCII文字の参考リンク: [ASCII文字の使い方](https://java-reference.com/java_info_ascii.html)
# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
