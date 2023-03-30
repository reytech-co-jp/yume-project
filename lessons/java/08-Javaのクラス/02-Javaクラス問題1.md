# クラスの課題

Javaのクラスの課題をやってみましょう。

# クラスについて

クラスについてはこちらのリンクを参考にしてください。   
クラスの参考リンク: [クラスについて勉強記事](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/java/08-Javaのクラス/01-Javaクラスの勉強記事.md)

# お願い

こちらの課題は課題ごとに新しいプロジェクトを作成しないでいろいろ試してみてください。

# 準備

`src`フォルダーの下に`Employee`というファイルの名前で社員の情報を管理するクラスを作成してください。

Employeeクラスには、`String`型の変数`firstName`と`lastName`、`int`型の変数`salary`、`配列`型の変数`skill`の4つのフィールドを持ちます。

```java
public class Employee {
    private String firstName;
    private String lastName;
    private int salary;
    private String[] skills;

}
```

# 課題1

`Employee`クラスには、全てのフィールドを引数にとるコンストラクタを作成するコードを記載してください。

# 課題2

`課題2`には`Employee`クラスで各フィールドの値を取得する`getter`メソッドと、設定する`setter`メソッドを記載してください。

`getter`メソッドは、クラスのフィールドの値を取得するために使用されます。一般的に、`getter`メソッドは「get」から始まり、そのフィールドの名前を続けた形で命名されます。たとえば、フィールド名が「firstName」であれば、`getter`メソッドは「getFirstName()」となりますが、フィールドの値を返すだけで、何らかの処理を行いません。

`setter`メソッドは、クラスのフィールドの値を設定するために使用されます。一般的に、`setter`メソッドは「set」から始まり、そのフィールドの名前を続けた形で命名されます。たとえば、フィールドが「firstName」であれば、`setter`メソッドは「setFirstName(String firstName)」となります。引数として新しい値を受け取り、その値をフィールドに設定します。

`getter`メソッドと、`setter`メソッドについての参考リンク：[getterメソッドと、setterメソッドの使い方](https://kiserukun.hatenablog.com/entry/2021/07/03/120000)

# 課題3

`Employee`クラスで社員の`firstName`と`lastName`を結合して`String`型の結果を返す`getFullName`メソッドを記載してください。

次に社員の年俸を計算する`getAnnualSalary`というメソッドを記載してください。年俸とは1年間の労働に対して支払われる給与のことです。年俸を計算するためには、社員の月の給与に12(1年間)をかけることで得られます。

# 課題4

`Main.java`にEmployeeのインスタンスをリストに格納しますので`ArrayList`を使用して`employeeList`というリストを作成してください。
`employeeList`に以下の社員のデータを使用して3つの`Employee`インスタンスを生成し、リストに追加してください。

社員のデータ
```
1.
FirstName - John 
LastName - Smith
Salary - 800000円
Skills - ["Java", "Python", "PHP"]

2.
FirstName -  Katherine 
LastName -  White
Salary - 750000円
Skills - ["HTML", "CSS", "JavaScript", "Tailwind CSS"]

3.
FirstName -  Jessica  
LastName -  Garcia
Salary - 940000円
Skills - ["React", "Django", "Flutter", "PHP"]
```

# 課題5

繰り返し文を使用してリストから各インスタンスを取り出し、getFullName、getSalary、getSkills、getAnnualSalaryメソッドを呼び出して、各社員データを以下のように出力しています。

出力は以下のようになります。

```java
【社員のデータを表示する】
名前：John Smith, 年俸：960000円, スキル：[Java, Python, PHP]
名前：Katherine White, 年俸：750000円, スキル：[HTML, CSS, JavaScript, Tailwind CSS]
名前：Jessica Garcia, 年俸：940000円, スキル：[React, Django, Flutter, PHP]
```

# 宿題

※この宿題はSlackに提出しなくても大丈夫です。
