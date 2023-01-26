# 何をするのか？

Javaの条件、繰り返し、配列を勉強するための問題です。

# 前提

- Javaのバージョンは17を使いましょう
- エディタはIntelliJを使いましょう

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
    └── TriangleProgram.java
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

Javaの条件、繰り返しについてを勉強するためのリポジトリです。
```

`src/TriangleProgram.java`には下記を記載してください。

```java
public class TriangleProgram {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

}
```

ここまでできたら自分のリポジトリにプロジェクトをpushしましょう。  

----

# 課題１

キーボードから入力された文字列や数値を受け取ってプログラムの中で処理できるようにしましょう。   
入力は次のような形式になるようにしましょう。
```java
【三角形に印刷する行数を入力してください！】
5
```

出力は次のような形式になるようにしましょう。
```java
【入力値を確認する】
* * * * * 
```

JavaのScannerについて参考リンク: [Scannerの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/feature/java_big_questions/lessons/java/05-Java%E3%81%AE%E5%A4%A7%E8%AA%B2%E9%A1%8C/JavaScanner%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#scanner%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)

実装のサンプルはこちらです。   
コピペでもいいです。
```java
public class TriangleProgram {

  public static void main(String[] args) {
    Scanner scan = new Scanner(System.in);
    System.out.println("【三角形に印刷する行数を入力してください！】");
    int rows = scan.nextInt();
    //以下の分はただチェックするだけですから確認したあとに削除してください
    for (int i = 0; i < rows; i++) {
      System.out.print("* ");
    }

  }

}
```
***コメントとコメント以下の分はただチェックするだけですから確認したあとに削除してください。***   

# 問題

入力した値によっていろいろな三角形を表示しましょう。   
1. `rows`の値は0より大きい、そして4以下の場合は直角三角形を表示してください。
2. `rows`の値は4より大きい、そして7以下の場合は左三角形を表示してください。
3. `rows`の値は7より大きい、そして15未満の場合はピラミッド形を表示してください。
4. それ以外は`invalid`と表示してください。

# 例

問題を実装する前にこの例プログラムを参考にしてください。   
このプログラムは例だけですので実装しなくても大丈夫です。
```java
public class ExampleProgram {

  public static void main(String[] args) {
      int i, j, rows = 6;
      for (i = 0; i < rows; i++) { 
        for (j = rows - i; j > 0; j--) {
          System.out.print("* ");   
        }
          System.out.println();   
      }

  }

}
```
例プログラムの出力は以下のようになります。
```java
* * * * * * 
* * * * * 
* * * * 
* * * 
* * 
* 

```

# 課題２

入力した値が0より大きい、そして4以下の場合、直角三角形が表示されるように実装してください。   
出力は以下のようになります。
```java
* 
* * 
* * * 
* * * * 
```

# 課題３

もし入力した値は4より大きい、そして7以下の場合は下記のような三角形が表示されるようにしましょう。   
出力は以下のようになります。
```java
           * 
         * * 
       * * * 
     * * * * 
   * * * * * 
```

# 課題４

入力した値は7より大きい、そして15未満の場合はピラミッド形を表示しましょう。   
出力は以下のようになります。
```java
       * 
      * * 
     * * * 
    * * * * 
   * * * * * 
  * * * * * * 
 * * * * * * * 
* * * * * * * * 
```

# 課題５

入力した値は16、30、0など入力された場合は`Invalid`と表示してください。   
```java
Invalid
```

# どうなったら宿題が完了と言えるのか

- 入力した値は0より大きい、そして4以下の場合は直角三角形が表示されること
- 入力した値は4より大きい、そして7以下の場合は左に直角がある三角形が表示されること
- 入力した値は7より大きい、そして15未満の場合はピラミッド形が表示されること
- 入力した値は16、0など入力された場合は`invalid`が表示されること
- 自分のリポジトリに`feature/display-triangle`という名前でブランチができていること

# 宿題

実装が終わったら自分のリポジトリに`feature/display-triangle`という名前でブランチを作成してください。   
そして、コミットしてプッシュします。   
コミットについて参考リンク: [コミットメッセージの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/github/02-Git%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6GitHub%E3%81%AB%E3%82%BD%E3%83%BC%E3%82%B9%E3%82%B3%E3%83%BC%E3%83%89%E3%82%92push%E3%81%97%E3%81%A6%E3%81%BF%E3%82%88%E3%81%86.md#git-commit%E3%81%A8%E3%81%AF%E4%BD%95%E3%81%8B)   
※完了したら自分のリポジトリにPull Requestを作成してSlackにレビューを出してください。
