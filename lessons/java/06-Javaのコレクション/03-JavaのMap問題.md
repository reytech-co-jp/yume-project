# Mapの課題

Javaの`Map`について次の課題をやってみましょう。

# Mapの使い方

`Map`の使い方についてはこちらのリンクを参考にしてください。

`Map`の使い方の参考リンク: [Mapの勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/06-Java%E3%81%AE%E3%82%B3%E3%83%AC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3/01-Java%E3%82%B3%E3%83%AC%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%AE%E5%8B%89%E5%BC%B7%E8%A8%98%E4%BA%8B.md#map)

# お願い

こちらの課題は新しいプロジェクトを作成しないで一つの`Main.java`にいろいろ試してみてください。

# 準備

`Main.java`に学生のIDと名前をセットに格納するため、下記のように`studentMap`というキーと値に文字列を格納する`HashMap`を宣言してください。`studentMap`を`for-each`メソッドを使用して以下のように記載して出力してください。

```java
import java.util.HashMap;
import java.util.Map;

public class Main {

    public static void main(String[] args) {
        Map<String, String> studentMap = new HashMap<>();
        studentMap.put("A03", "Minato");
        studentMap.put("A05", "Erika");
        studentMap.put("A01", "Hikari");
        studentMap.put("A04", "Akari");
        studentMap.put("A02", "Yukina");
        System.out.println("【学生の名前をID付きで表示する】");
        studentMap.forEach((key, value) -> System.out.println(key + " - " + value));
    }
}

```

出力：

```java
【学生の名前をID付きで表示する】
A01 - Hikari
A02 - Yukina
A03 - Minato
A04 - Akari
A05 - Erika
```

# 課題1

`課題1`では生徒数を数えるコードを追加してください。
ここではマップに追加されているキーと値のペアの数を返すため`マップ名.size()`メソッドを使用します。

`マップ名.size()`の参考リンク：[マップ名.size()の使い方](https://www.javadrive.jp/start/collection/index3.html#section5)

出力は次のようになります。

出力：

```java
クラスAでは学生の数が５人です。
```

# 課題2

`課題2`ではID`A01`の学生がいるかどうか確認してこの学生がいるならクラスから除ぐコードを記載してください。削除する時は削除する要素を取得して`学生「学生名」を正常に削除されました`という形でメッセージを表示します。  
次に削除した後の`studentMap`マップを`for-each`文を使用して表示してください。

指定したキーが存在するか確認するには`マップ名.containsKey(キー)`、キーを指定して対応する要素を削除するには`マップ名.remove(キー)`を使用します。

`マップ名.containsKey(キー)`の参考リンク：[マップ名.containsKey(キー)の使い方](https://www.javadrive.jp/start/collection/index3.html#section9)  
`マップ名.remove(キー)`の参考リンク：[マップ名.remove(キー)の使い方](https://www.javadrive.jp/start/collection/index3.html#section8)

出力は次のようになります。

出力：

```java
学生Hikariさんを正常に削除されました！
【削除後に学生の名前をID付きで表示する】
A02 - Yukina
A03 - Minato
A04 - Akari
A05 - Erika
```

# 課題3

`課題3`では`Erika`という名前の学生がいるかどうかを確認して学生がいるならこの学生を取得して`「学生名」という名前の学生が存在します！`という形で表示し、いない場合は`「学生名」という名前の学生が存在しません！`という形でメッセージを表示してください。

指定した値が存在するか確認するには`マップ名.containsValue(値)`、キーkeyに対応する値を取得するには`マップ名.get(キー)`を使用します。

`マップ名.containsValue(値)`の参考リンク：[マップ名.containsValue(値)の使い方](https://www.javadrive.jp/start/collection/index3.html#section9)  
`マップ名.get(キー)`の参考リンク：[マップ名.get(キー)の使い方](<https://www.javadrive.jp/start/collection/index3.html#section6>)

出力は次のようになります。

出力：

```java
Erikaという名前の学生が存在します！
```

# 課題4

`課題4`では学生のデータを値で並べ替えます。HashMapクラスは要素の順番を保障しないから格納された順番を保持している`Map`インターフェースを実装したクラスの一つ`LinkedHashMap`クラスを使用します。

まずは`sortedStudentMap`という名前でキーと値に文字列を格納する空の挿入順序の`LinkedHashMap`を作成してください。書き方は以下のように記述します。

```java
 LinkedHashMap<String, String> sortedStudentMap = new LinkedHashMap<>();
```

`LinkedHashMap`の参考リンク：[LinkedHashMapの使い方](https://washboard.blog/105/)

次に`studentList`という名前で`ArrayList`を使用して`List`を作成してください。`studentList`に`studentMap`からの値を繰り返し文を使用して挿入してください。挿入したら`studentList`をソートするため、`Collections`クラスのsortメソッドを使用します。書き方は以下のように記述します。

```java
Collections.sort(リスト名);
```

`Collections.sort(リスト名)`の参考リンク：[Collections.sort(リスト名)の使い方](https://itsakura.com/java-arraylist-sort)

ソートが出来たら自分が好きな繰り返し文を使用して以下のように出力してください。

出力：

```java
【ソートした学生のリストを表示する】
Akari
Erika
Minato
Yukina
```

# 課題5

`課題5`ではソートされた`studenetList`と`studentMap`を使用して`sortedStudentMap`にソートされたリストのすべてのマップエントリに対して、キーと値のペアを挿入します。

次に`sortedStudentMap`を自分が好きな繰り返し文を使用して以下のように出力してください。

出力：

```java
【値でソートした学生のマップを表示する】
A04 - Akari
A05 - Erika
A03 - Minato
A02 - Yukina
```

ここでは繰り返し文`for`や`for-each`文や`for-eachメソッド`や`ネストされたfor文法`など自分が好きな方法で実装してみてください。

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
