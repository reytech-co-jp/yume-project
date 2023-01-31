# 配列の課題

Javaの配列の課題をやってみましょう。

# 配列について

配列についてはこちらのリンクを参考にしてください。   
配列の参考リンク: [配列について勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/array_statement_questions/lessons/java/04-Java%E3%81%AE%E9%85%8D%E5%88%97%E5%95%8F%E9%A1%8C/Java%E9%85%8D%E5%88%97%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#java%E9%85%8D%E5%88%97%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。
 
# 準備

`Main.java`に下記のように`numArray`というint型の配列を記述してください。   
`numArray`の値は以下のようになります。
```java
public class Main {

  public static void main(String[] args) {
    int[] numArray = {12, 31, 7, 9, 28, 10};
  }

}
```

# 課題１

`numArray`の長さは10以上の場合は以下のようにメッセージを表示してください。
```java
numArrayの長さは10以上です。
numArrayの長さ: {numArrayの長さ}
```
10未満の場合は以下のようにメッセージを表示してください。   
```java
numArrayの長さは10未満です。
numArrayの長さ: {numArrayの長さ}
```
出力は下記のようになります。
```java
numArrayの長さは10未満です。
numArrayの長さ: 6
```
配列の長さを取得するメソッドの参考リンク: https://www.javadrive.jp/start/array/index6.html

# 課題２

10未満の場合は`numArray`の最初の値と最後の値の足し算を表示してください。   
出力は下記のようになります。
```java
numArrayの長さは10未満です。
numArrayの長さ: 6
最初と最後の値の合計: 22
```
配列の各要素の値がどのように代入されているか以下の画像を参考してください。   
<img width="500" src="https://user-images.githubusercontent.com/100908505/210033403-59ad078e-5140-4412-9dae-f2fff45d81f6.png">

# 課題３ + α 

下記のように`sum`というint型の変数を記述してください。   
```java
public class Main {

  public static void main(String[] args) {
    int[] numArray = {12, 31, 7, 9, 28, 10};
    int sum = 0;
  }

}
```

# 課題３

`numArray`にある値を全部加算して`sum`に入力してください。
出力は以下のようになります。
```java
numArrayにある値の合計値: 97
```
配列のデータを取得する方法の参考リンク: [配列のデータを取得する方法](https://github.com/reytech-co-jp/yume-project/blob/feature/array_statement_questions/lessons/java/04-Java%E3%81%AE%E9%85%8D%E5%88%97%E5%95%8F%E9%A1%8C/Java%E9%85%8D%E5%88%97%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#%E9%85%8D%E5%88%97%E3%81%AE%E5%87%BA%E5%8A%9B)

# 課題４+ α 

下記のように`nameArray`と`copyNameArray`という2つのString型の配列を記述してください。   
<strong>`copyNameArray`の値は`nameArray`にある値をコーピします。</strong>
```java
public class Main {

  public static void main(String[] args) {
    String[] nameArray = {"John", "William", "Bob", "Stark"};
    String[] copyNameArray = ....
  }

}
```
コピーする方法は以下のリンクを参考にして自分が好きな方法でやってみてください。   
参考リンク: https://workteria.forward-soft.co.jp/blog/detail/10213

# 課題４

もし`copyNameArray`の値は`nameArray`と等しい場合は以下のように表示してください。
```java
【copyNameArrayとnameArrayは等しいです。】
copyNameArray【0】の値: John
nameArray【0】の値: John
```
それ以外は以下のように表示してください。
```java
【copyNameArrayとnameArrayは同じではありません。】
```
2つの配列が等しいかどうか調べるときに使うメソッドは以下のリンクを参考にしてください。   
https://www.geeksforgeeks.org/java-util-arrays-equals-java-examples/

# 課題５

`copyNameArray`にある各値を表示してください。
出力は以下のようになります。
```java
【copyNameArrayのデータ】
copyNameArray【0】のデータ: John
copyNameArray【1】のデータ: William
copyNameArray【2】のデータ: Bob
copyNameArray【3】のデータ: Stark
```
配列にあるデータを取得する方法の参考リンク: [配列のデータを取得する方法](https://github.com/reytech-co-jp/yume-project/blob/feature/array_statement_questions/lessons/java/04-Java%E3%81%AE%E9%85%8D%E5%88%97%E5%95%8F%E9%A1%8C/Java%E9%85%8D%E5%88%97%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#%E9%85%8D%E5%88%97%E3%81%AE%E5%87%BA%E5%8A%9B)

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
