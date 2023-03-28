# 引数を持つメソッドの課題

Javaの引数を持つメソッドの課題をやってみましょう。

# 引数を持つメソッドについて

引数を持つメソッドについてはこちらのリンクを参考にしてください。  
引数を持つメソッドの参考リンク: [引数を持つメソッドについて勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/07-Java%E3%81%AE%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E5%95%8F%E9%A1%8C/01-Java%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md)

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に下記のように`int`型の`passedSubjects`と`faliedSubjects`という変数を記載してください。

次に`HashMap`を使用して`String`型のキーと`Integer`型の値を持つ`tanakaMarks`という`Tanaka`さんの各科目のマークをマップする`Map`を作成してください。`Map`に以下のようにキーと値のセットを追加します。

```java
import java.util.HashMap;
import java.util.Map;

public class Main {

    public static void main(String[] args) {
        int passedSubjects = 0;
        int failedSubjects = 0;
        Map<String, Integer> tanakaMarks = new HashMap<>();
        tanakaMarks.put("国語", 50);
        tanakaMarks.put("英語", 39);
        tanakaMarks.put("数学", 80);
        tanakaMarks.put("理科", 70);
        tanakaMarks.put("化学", 33);
        tanakaMarks.put("物理", 77);
        tanakaMarks.put("歴史", 79);
        System.out.println("【Tanakaさんの成績を表示する】");
        for (Map.Entry<String, Integer> entry : tanakaMarks.entrySet()) {
            System.out.println(entry.getKey() + " - " + entry.getValue());
        }
    }
}

```

出力：

```java
【Tanakaさんの成績を表示する】
物理 - 77
歴史 - 79
理科 - 70
国語 - 50
数学 - 80
化学 - 33
英語 - 39
```

`Map`と`HashMap`の参考リンク：[MapとHashMapの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/06-Java%E3%81%AE%E3%82%B3%E3%83%AC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3/01-Java%E3%82%B3%E3%83%AC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#map)

`Map`を繰り返す方法の参考リンク：[Mapを繰り返す方法の参考リンク](https://flytech.work/blog/7360/#For-EachMapentrySet)

# 課題1

`課題1`では科目のマークによって合格か不合か確認する`hasPassed`というメソッドを作成してください。

`hasPassed`メソッドでは`int`型の変数を渡します。メソッド内で渡された引数が40以上である場合は`true`を返し、40未満の場合は`false`を返すコードを追加してください。

# 課題2

`課題2`では合格した科目の数と不合格した項目の数を表示します。  

まずは`main`メソッド内で`tanakaMarks`Mapを自分が好きな繰り返し文で繰り返してループ内で`hasPassed`というメソッドを呼び出して各科目が合格か不合格か確認します。`hasPassed`メソッドで`tanakaMarks`Mapからの各値を渡します。

合格なら`passedSubjects`を1ずつ足し、不合格なら`failedSubjects`を1ずつ足します。

出力は以下のようになります。

```java
【Tanakaさんの合格した科目の数と不合格した項目の数を表示する】
合格 - 5, 不合格 - 2
```

# 課題3

`課題3`では不合格した科目とその科目のマークをマップして返す
`returnFailedSubjects`メソッドを追加してください。`returnFailedSubjects`メソッドで`String`型のキーと`Integer`型の値を持つ`Map`型の変数を渡します。  

まずはメソッド内で`failedSubjectMap`という`Map`を宣言してください。そして`hasPassed`メソッドで確認して不合格した科目を`failedSubjectMap`に追加してください。次に`failedSubjectMap`を返してください。

次に`main`メソッドで`failedSubjectMap`メソッドを呼び出してこのメソッドで`tanakaMarks`Mapを渡し、以下のように出力してください。

出力は以下の通りになります。

出力：

```java
【Tanakaさんの不合格した項目を表示する】
化学 - 33
英語 - 39
```

# 課題4

`課題4`ではTanakaさんのすべてのマークの合計を返す`calculateSum`というメソッドを作成してください。`calculateSum`メソッドで`String`型のキーと`Integer`型の値持つ`Map`型の変数を渡します。

メソッド内では渡した`Map`を繰り返し文で繰り返して`Map`に含まれるすべてのマーク(キー)を合計してください。合計したら`int`型の結果を返してください。

次に`main`メソッドで`calculateSum`メソッドを呼び出してこのメソッドで`tanakaMarks`Mapを渡します。

出力は以下の通りになります。

出力：

```java
【Tanakaさんのすべてのマークの合計を表示する。】
合計 - 428
```

# 課題5

`課題5`ではTanakaさんのすべてのテスト結果の平均点を計算する`calculateAverage`というメソッドを作成してください。`calculateAverage`メソッドで`String`型のキーと`Integer`型の値持つ`Map`型の変数を渡します。

`calculateAverage`メソッドでは平均点を計算するためすべてのマークの合計を`Map`のサイズで割りますから`calculateSum`メソッドを呼び出してください。

`Map`のサイズを取得するには`マップ名.size()`メソッドを使用してください。

`マップ名.size()`の参考リンク：[マップ名.size()の使い方](https://www.javadrive.jp/start/collection/index3.html#section5)

`calculateAverage`メソッドで合計の結果を`Map`のサイズで割って`int`型の結果を返してください。

次に`main`メソッドで`calculateAverage`メソッドを呼び出してこのメソッドで`tanakaMarks`Mapを渡します。

出力は以下の通りになります。

```java
【Tanakaさんの平均点を表示する】
平均点 - 61
```

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
