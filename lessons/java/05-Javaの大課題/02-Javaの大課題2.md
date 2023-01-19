# 何をするのか？

Javaの条件、繰り返し、配列を勉強するための問題です。

# 前提

- Javaのバージョンは17を使いましょう
- エディタはIntelliJを使いましょう

# 注意

問題によって実装するので問題がわからないと実装がうまくできないから問題をちゃんとわかるようにゆっくり読んでください。   
この問題では入力例として3つとそれぞれの出力例を記載されています。   
まずはその入力例の値のように入力して期待された出力例が出力するようにしましょう。   

# 準備

GitHubの自分のアカウントでリポジトリを作ってください。  

リポジトリの名前は「java-question-02」にしてください。  

IntelliJからProjectを作成しましょう。  

<img width="500" alt="スクリーンショット 2022-07-16 19 05 49" src="https://user-images.githubusercontent.com/62045457/179350352-6f6874cc-cb80-4f87-a527-44667322c4ed.png">

ディレクトリ構成は下記のようにしましょう。  

```bash
.
├── .gitignore
├── README.md
└── src
    └── Main.java
```
.gitignoreには下記を記載してください。  

```
HELP.md
.gradle
build/
!gradle/wrapper/gradle-wrapper.jar
!**/src/main/**/build/
!**/src/test/**/build/

### STS ###
.apt_generated
.classpath
.factorypath
.project
.settings
.springBeans
.sts4-cache
bin/
!**/src/main/**/bin/
!**/src/test/**/bin/

### IntelliJ IDEA ###
.idea
*.iws
*.iml
*.ipr
out/
!**/src/main/**/out/
!**/src/test/**/out/

### NetBeans ###
/nbproject/private/
/nbbuild/
/dist/
/nbdist/
/.nb-gradle/

### VS Code ###
.vscode/
```

README.mdには下記を記載してください。  

```
# このプロジェクトについて

Javaの条件、繰り返し、配列を勉強するためのリポジトリです。
```

`src/Main.java`には下記を記載してください。

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

}
```

ここまでできたら自分のリポジトリにプロジェクトをpushしましょう。  

----
# 問題

LeonとAnnaは期末テストの点数で勝負をすることにしました。しかし、LeonとAnnaでは普段の成績に差があり、まともな勝負になりません。   
そこで、期末テストの点数の各位の数を足した数の一の位(文字列の右から1つ目の値)で勝負することにし、大きい方が勝ちとしました。   
つまり、<strong>`85`点であれば`8 + 5 = 13`で、`13`の一の位(右から1つ目の値)の`3`となります。</strong>   
二人の期末テストの点数が入力されるので、どちらが勝ったか、あるいは引き分けたかを出力してください。

# 期待する出力

<strong>Leonが勝った場合は"Leon"、Annaが勝った場合は"Anna"、引き分けの場合は"Draw"と出力してください。</strong>

# 入力することについて

- Leonの期末テストの点数を表す整数`X`とAnnaの期末テストの点数を表す整数`Y`がこの順で入力されます。
- 入力は1行となります。
入力は以下のフォーマットで与えられます。
```java
X Y
```

# 課題１

キーボードから入力された文字列や数値を受け取ってプログラムの中で処理できるようにしましょう。   
入力は次のような形式になるようにしましょう。
```java
【Leonの点数とAnnaの点数をスペースを付けて入力してください】
45 56
```

出力は次のような形式になるようにしましょう。
```java
【入力値を確認する】
45 56
```

JavaのScannerについて参考リンク: [Scannerの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/java_big_questions/lessons/java/05-Java%E3%81%AE%E5%A4%A7%E8%AA%B2%E9%A1%8C/JavaScanner%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#scanner%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)

実装のサンプルはこちらです。   
コピペでもいいです。
```java
public class Main {

  public static void main(String[] args) {
    Scanner scan = new Scanner(System.in);
    System.out.println("【Leonの点数とAnnaの点数をスペースを付けて入力してください】");
    String inputString = scan.nextLine();
    //以下の分はただチェックするだけですから確認したあとに削除してください
    System.out.println("【入力値を確認する】");
    System.out.println(inputString);
  }

}
```
***【入力値を確認する】分はただチェックするだけですから確認したあとに削除してください。***   
そして、`scan.nextLine()`の文も`scan.nextInt()`とか自分が好きな方法でやってみてください。   

# 課題２

まずは入力された文字列を分岐して条件をつけましょう。   

## 条件

- X(Leonの点数)とY(Annaの点数)の値については以下のようになります。
  - 0 ≦ X ≦ 100
  - 0 ≦ Y ≦ 100

文字列を分割するsplitメソッドの参考リンク: https://java-code.jp/799   
String型からint型に変換することについて参考リンク: https://www.javadrive.jp/start/string/index12.html

# 課題３

こちら問題3は***期待する出力***が出せるように問題を解決するコードを実装しましょう。実装がうまくいくため問題、それとも問題のまとめを理解するようにしておきましょう。   

## 問題のまとめ

- <strong>※LeonとAnnaのそれぞれの点数は`10`点より小さい場合は`0`となります。</strong>   
- <strong>※LeonとAnnaのそれぞれの点数は`100`点の場合は最初の位の`1`となります。</strong>   
- <strong>足した数は`10`未満</strong>であればその足した値をそのまま取ります。
  - <strong>例えば、`34`点であれば`3 + 4 = 7`で、`7`となります。</strong>   
- <strong>足した数は`10`以上</strong>の場合は問題で説明された通り一の位(右から1つ目の値)をとります。
  - <strong>例えば、`85`点であれば`8 + 5 = 13`で、`13`の一の位(右から1つ目の値)の`3`となります。</strong>    

下記の入力例を利用して自分のコードが出力例と同じく出力を出せるようにしましょう。入力例は3つありますので、その3つを試してみてください。   

## 入力例と出力例

### 入力例: 1

`75 81`という文字列を入力しましょう。   
入力は以下のようになります。  
```java
【Leonの点数とAnnaの点数をスペースを付けて入力してください】
75 81
```
Leonの点数は`75`から`7`と`5`の足し算は`12`ですが問題の通りだと一位の値(右から1つ目の値)`2`を取ります。それからAnnaの点数は`81`から`8`と`1`の足し算は`9`です。
ですからAnnaの点数が大きいので勝った人はAnnaとなります。
出力は以下のようになります。
```java
【勝った人】
Anna
```

### 入力例: 2

`100 91`という文字列を入力しましょう。   
入力は以下のようになります。
```java
【Leonの点数とAnnaの点数をスペースを付けて入力してください】
100 91
```
出力は以下のようになります。
```java
【勝った人】
Leon
```

### 入力例: 3

`69 87`という文字列を入力しましょう。   
入力は以下のようになります。
```java
【Leonの点数とAnnaの点数をスペースを付けて入力してください】
69 87
```
出力は以下のようになります。
```java
【勝った人】
Draw
```

JavaのcharAtメソッドについて参考リンク: https://java-code.jp/185   

実装が終わったら自分のリポジトリに`feature/mark-check-function`という名前でブランチを作成してください。   
そして、コミットしてプッシュします。   
コミットについて参考リンク: [コミットメッセージの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/github/02-Git%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6GitHub%E3%81%AB%E3%82%BD%E3%83%BC%E3%82%B9%E3%82%B3%E3%83%BC%E3%83%89%E3%82%92push%E3%81%97%E3%81%A6%E3%81%BF%E3%82%88%E3%81%86.md#git-commit%E3%81%A8%E3%81%AF%E4%BD%95%E3%81%8B)

# どうなったら宿題が完了と言えるのか

- 全部の入力例とその出力例が当てること
- 自分のリポジトリに`feature/mark-check-function`という名前でブランチができていること

# 宿題

※完了したら自分のリポジトリにPull Requestを作成してSlackにレビューを出してください。
