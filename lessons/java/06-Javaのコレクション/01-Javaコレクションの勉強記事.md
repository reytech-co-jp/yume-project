# Javaコレクションについて

# コレクション
`Java`の`コレクション`は、複数の要素やオブジェクトを格納および管理するオブジェクトです。

`コレクション`は集められたデータに対して検索、並べ替え、挿入、操作、削除などの操作実行できます。

これから`コレクション`インターフェースを継承して作られている`List`と`コレクション`とよく似た機能を持つ`Map`も合わせて解説いたします。

# List
`Java`の`List`は格納されたデータを順序付けして管理します。
要素を挿入、更新、削除、および検索するためのインデックスベースのメソッドを使用することができます。重複した要素を持つこともできます。

次は`List`インターフェースを実装したクラスの一つ`ArrayList`について解説いたします。

## ArrayListの使い方
`ArrayList`は`List`インターフェースを実装したクラスの一つで、主にデータベースから取得したデータを格納し、処理する際に使われるクラスです。  

大量のデータや情報を管理し、プログラム内で素早く呼び出すのに適しています。配列と異なり、あとから`List`のサイズを変更して、新しい要素を追加、削除する作業ことができます。

以下の`ArrayList`に要素をセットし、その値を出力する例を見てみましょう。
```java
// List、ArrayListをimportする

import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {

        // ArrayList を使用してString型のListを作成する
        List<String> movies = new ArrayList<>();
        // Listに要素を追加する
        movies.add("コクリコ坂から");
        movies.add("君の名は");
        movies.add("崖の上のポニョ");
        System.out.println("【映画のリスト】");
        // for-each ループを使用して要素を繰り返します
        for (String movie : movies) {
            System.out.println(movie);
        }
    }
}
```
最初に`ArrayList` を使用して`List`を作成するため、`「List<データ型名> リスト名 = new ArrayList<データ型名>();」`の形で記述します。  
次に`movies`Listに要素を追加するには、`リスト名.add(要素)`メソッドを使用します。  
`movies`Listを出力するには`for-each`ループで繰り返して出力します。

出力は以下の通りになります。  

出力：
```java
【映画のリスト】
コクリコ坂から
君の名は
崖の上のポニョ
```

# Map

`Map`は、Javaで「キー」と対応する「値」をセットにして格納するデータ構造です。`配列`や`List`はインデックス番号で値を指定しますが、`Map`の場合は一意のキーで値を指定します。

次は`Map`インターフェースを実装したクラスの一つ`HashMap`について解説いたします。

## HashMap

`HashMap`は`Map`インターフェースを実装して一意であるキーと値の組み合わせで要素を管理します。重複するキーを挿入すると対応するキーの要素を置き換えます。また`HashMap`は順番を持ちません。

以下の`HashMap`に要素をセットし、そのキーと値を順に出力する例を見てみましょう。
```java
// Map、HashMapをインポートする

import java.util.HashMap;
import java.util.Map;

public class Main {

    public static void main(String[] args) {
        // char型のキーとString型の値の組み合わせのMapを作成する
        Map<Character, String> words = new HashMap<Character, String>();
        // Mapにキーと値を追加する
        words.put('A', "Apple");
        words.put('B', "Ball");
        words.put('C', "Cat");
        words.put('D', "Dog");
        words.put('E', "Egg");
        System.out.println("【アルファベットと単語を表示する】");
        // キーと値をforeachメソッドで繰り返す
        words.forEach((key, value) -> System.out.println(key + " for " + value));
        System.out.println("【アルファベットを表示する】");
        // keySetを使用してキーをfor-each文で繰り返す
        for (Character alphabet : words.keySet()) {
            System.out.println(alphabet);
        }
        System.out.println("【単語を表示する】");
        // valuesを使用して単語をfor-each文で繰り返す
        for (String word : words.values()) {
            System.out.println(word);
        }
    }
}

```
最初に`HashMap`クラスのインスタンスを作成するため、`HashMap<キーのデータ型,値のデータ型> 変数名 = new HashMap<>();`または`Map<キーのデータ型,値のデータ型> 変数名 = new HashMap<>();` という形で記載します。  
次に`words`Mapに新しいキーと値のペアを追加するには 、`マップ名.put(キー, 値)`メソッドを使用します。  
`words`Mapのキーと値それぞれを出力する時は繰り返し文`for-each`を使用します。  

`Map`のキーを全て取得するには、`Map`のキーを`Set`型で返す`keySet`メソッドを使用します。`Map`の値を全て取得するには、`Map`のキーを`Set`型で返す`values`メソッドを使用します。

出力：

```java
【アルファベットと単語を表示する】
A for Apple
B for Ball
C for Cat
D for Dog
E for Egg
【アルファベットを表示する】
A
B
C
D
E
【単語を表示する】
Apple
Ball
Cat
Dog
Egg
```

# まとめ

上記のようにJavaでは配列のように複数の要素を管理するのには`コレクション`を使用します。  
ご自身でソースコードを書いて試してみてください。
