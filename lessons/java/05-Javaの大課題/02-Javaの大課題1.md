# 何をするのか？

Javaの条件、繰り返し、配列、Scannerクラスを使用してじゃんけんゲームプログラムを処理します。  

# じゃんけんとは？

じゃんけんとは片手で石（グー）、紙（パー）、はさみ（チョキ）の形をまねて、どれかを互いに出しあって勝負をきめるゲームです。

グー＜パー、チョキ＜グー、パー＜チョキのような強さとなります。

# アプリケーションの仕様

- プレイヤーの名前をキーボードから入力してもらうこと
- グーなら「0」、チョキなら「１」、パーなら「2」で表現すること
- プレイヤーのじゃんけんの手は、キーボードから入力してもらうこと
- 「0」「1」「2」以外のデータが入力されたら再入力させること
- コンピュータ側のじゃんけんの手は、乱数で自動的に取得すること
- プレイヤーの判定結果(勝ち、負け、引き分け)を画面にプレイヤーの名前と共に表示すること
- プレイヤーがもう一度遊びたいか確認する時は、遊びたいなら「0」、辞めたいなら「1」をキーボードから入力してもらうこと
- 「0」「1」以外のデータが入力されたら再入力させること

# 前提

- Javaのバージョンは17を使いましょう
- エディタはIntelliJを使いましょう

# 準備

GitHubの自分のアカウントでリポジトリを作成してください。

リポジトリの名前は「rock-paper-scissors-project」にしてください。

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

`README.md`には下記を記載してください。

```java
# このプロジェクトについて

じゃんけんゲームのプログラムを管理します。
```

`src/Main.java`には下記を記載してください。

```java
public class Main {

  public static void main(String[] args) {
    System.out.println("Hello World");
  }

}
```
ソースコードを自動でフォーマットするために以下を設定しましょう。
Save ActionsというPluginをいれるとよいです。

<img width="400" alt="179350417-d076580b-9841-42f9-bac8-3a7ace7a08e9" src="https://user-images.githubusercontent.com/120652222/211270111-decd5bef-0b27-4c42-a7d5-7ae25c1e9f44.png">

<img width="400" alt="179350423-f3ca3c33-c3fa-4d3c-9b2c-18fcd86247ae" src="https://user-images.githubusercontent.com/120652222/211270145-13bca608-4a81-4277-88b3-dc8618a48905.png">

ここまでできたら自分のリポジトリにプロジェクトをpushしてください。

----

# 課題１

`feature/add-variables`ブランチを作成してください。

`Main.java`に下記のようにScannerクラスとRandomクラスを作成してください。次は`int`形配列`hands`、`int`形変数`playerMove`と`computerMove`と`replay`を作成してください。  

`String`形変数`playerName`を作成して`playerName`に入力した値を代入してください。

コードは以下のようになります。  

```java
import java.util.Scanner;
import java.util.Random;
public class Main {
	public static void main(String[] args) {
	Scanner scanner = new Scanner(System.in);
        Random rand = new Random();
        String[] hands = {"グー", "チョキ", "パー"};
        int playerMove;
	int computerMove;
        int retry;
        System.out.println("【じゃんけんゲームへようこそ！グーの場合は0、チョキの場合は1、パーの場合は2を選択してください。】");
        System.out.println("まずはご自身の名前を入力してください。");
        String playerName = scanner.nextLine();
        System.out.println("じゃ"+playerName+"さん今ゲームを始めます！");
	}
}
```

出力は以下の通りになります。

出力：

```java
【じゃんけんゲームへようこそ！グーの場合は0、チョキの場合は1、パーの場合は2を選択してください。】
まずはご自身の名前を入力してください。
日花里
じゃ日花里さん今ゲームを始めます！
```
ここまでの変更を日本語でコミットしてpushしてください。
feature/add-variables→mainにPull Requestを作成してください。

Pull Requestはレビューしやすいようにタイトルや説明をよく考えて書いてください。
Pull Requestを作成したらレビューを依頼してください。

レビューが完了したらPull Requestをマージしてください。
リモートの`feature/add-variables`ブランチは削除してください。

Pull Requestをマージしたら自動でリモートのブランチを削除する機能がありますので設定をONにするといいです。   
参考： <https://docs.github.com/ja/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-the-automatic-deletion-of-branches>

JavaのScannerについての参考リンク: [Scannerの使い方](https://github.com/reytech-co-jp/yume-project/blob/feature/java_big_questions/lessons/java/05-Java%E3%81%AE%E5%A4%A7%E8%AA%B2%E9%A1%8C/JavaScanner%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#scanner%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)

JavaのRandomについての参考リンク: [Randomクラスの勉強記事](https://java-code.jp/288)

# 課題2
自分のリポジトリに`feature/play-janken`という名前のブランチを作成してください。

プレイヤーの名前をキーボードから入力できるコードを記載してください。そしてコンピューター側の手をランダムに選び、選んだ値を`computerMove`に代入し、 選択もの「(0)グー、(1)チョキ、(2)パー 」を表示してプレイヤーからこの3つから選ぶ入力を`playerMove`に代入するコードを記載てください。0、1、2以外の数字が選ばれたらもう一度再入力させます。  

コンピューターがランダムに選んだ結果とユーザーが入力した結果を表示してください。

出力：

```java
【じゃんけんゲームへようこそ！グーの場合は0、チョキの場合は1、パーの場合は2を選択してください。】
まずはご自身の名前を入力してください。
日花里
じゃ日花里さん今ゲームを始めます！
じゃんけんゲーム！
(0)グー (1)チョキ (2)パー から選択してください：1
日花里：チョキ
コンピューター：グー
```
ここまでできたら変更をコミットしてpushしてください。  
そして、Pull Requestを作成してレビューを依頼してください。  
レビューが完了したらPull Requestをマージして`feature/play-janken`ブランチは削除してください。

# 課題3

`feature/display-result`ブランチを作成してください。

次にじゃんけんの勝敗結果を判定するコードを追加してください。  

- ゲームに勝つ場合は【コングラチュレーション`playerName`さんの勝ちです！】と表示、
- ゲームに負けた場合は【ゲームオーバー`playerName`さんの負けです！】と表示、
- ゲームを引き分けた場合は【引き分けです！】と表示するコードを記載してください。

ヒント：じゃんけんの勝敗を判定するとき`int`resultに`playerMove`を`computerMove`で減算して答えに3を足して正の数にスライドさせ、その数を3で割ったあまりを代入すること！

計算式は、`(playerMove - ComputerMove + 3) % 3` ということになります。

- `result`が 0 の時は、引き分け
- `result`が 1 の時は、プレイヤーの負け
- `result`が 2 の時は、プレイヤーの勝ち

＊上記のヒントと違う考え方で開発しても大丈夫です！

出力は以下の通りになります。

出力：

```java
【じゃんけんゲームへようこそ！グーの場合は0、チョキの場合は1、パーの場合は2を選択してください。】
まずはご自身の名前を入力してください。
日花里
じゃ日花里さん今ゲームを始めます！
じゃんけんゲーム！
(0)グー (1)チョキ (2)パー から選択してください：1
日花里：チョキ
コンピューター：グー
ゲームオーバー日花里さんの負けです！
```
ここまでできたら変更をコミットしてpushしてPull Requestを作成してレビューを依頼してください。  
レビューが完了したらPull Requestをマージして`feature/display-result`ブランチは削除してください。

# 課題4

新しいブランチ`feature/play-again`という名前で作成してください。

こちらの処理は少なくとも1回は行い、プレイヤーが遊びたい限りじゃんけんゲームの処理を行い、遊びたくない場合は処理を停止しますから繰り返し文`do-while`を使用して`do-while`ブロックの内でじゃんけん処理（課題2から課題3）のコードを移してください。`do-while`の条件は変数`retry`が0であれば処理を続けるコードを記載してください。

`do-while`ブロック中で次にもう一度遊びたいか確認するコードを追加してください。　

一度遊びたいか質問して遊びたい場合は0、ゲームを止めたい場合は1を選択するコードを記載してください。

プレイヤーから入力した値( 0 or 1 )を変数`retry`に代入してください。0、1以外の数字が入力されたらこの処理を繰り返します。

出力は以下の通りになります。

出力：

```java
【じゃんけんゲームへようこそ！グーの場合は0、チョキの場合は1、パーの場合は2を選択してください。】
まずはご自身の名前を入力してください。
日花里
じゃ日花里さん今ゲームを始めます！
じゃんけんゲーム！
(0)グー (1)チョキ (2)パー から選択してください：1
日花里：チョキ
コンピューター：グー
ゲームオーバー日花里さんの負けです！
もう一度遊びたいですか？(0)はい (1)いいえ ：1

...Program finished with exit code 0
```
ここまでできたら変更をコミット、pushし、Pull Requestを作成し、レビューを依頼してください。
レビューが完了したらPull Requestをマージして`feature/play-again`ブランチは削除してください。

# 宿題

※完了したら自分のリポジトリにプールリクエストを作成してSlackにレビューを出してください。
