# Javaのコンストラクタについて

# 概要

- メンバ変数
- コンストラクタ

# メンバ変数

コンストラクタを説明する前にメンバ変数について少し解説していきます。

## メンバ変数とは

メンバ変数とはクラス定義をしている`{`と`}`の中に記述され、そしてメソッドの外に記述されている変数のことです。メンバ変数とはクラス定義の中で下記の部分です。

```java
public class Car { 
    String model;   //メンバ変数

    //メンバメソッド
    void setModel(String newModel) {
        this.model = newModel;
    }

    //メンバメソッド
    void displayModel() {
        System.out.println("車のモデルは" + model + "です。");    
    }

}
```
変数`model`の定義されている部分を含んでいる一番近くの`{`と`}`はクラス定義の`{`と`}`ですので、この変数はクラス内であれば自由に使うことが出来ます。このような変数をメンバ変数と言います。   
このクラスからオブジェクトを作成した時にメンバ変数は作成され、オブジェクトが破棄されるまで変数に格納されている値は保存されています。   
メンバ変数はオブジェクトの性質や状態などを保存しておく時に利用します。

## メンバ変数に値を格納する方法

今回はメンバ変数の値をメンバメソッドを使って代入します。   
メンバメソッドとはクラスの中で定義されているメソッドのことで、そのクラスの中で何かの動作をするためのものです。   
メンバメソッドが定義されているクラスの外からオブジェクトを介して呼び出す場合には「オブジェクト名.メンバメソッド名(引数)」の形式で呼び出します。   
上記の`Car`クラスには`setModel`と`displayModel`というメンバメソッドがあります。   
setModelメソッド内で、メンバ変数に値を格納しています。   
メンバ変数に格納したい値を下記のようにmainメソッドから値を渡します。

```java
public class Main {

    public static void main(String[] args) {
        Car car = new Car();
        car.setModel("Toyota");

    }

}

```

作成されたオブジェクトを使ってクラスの中に定義されたメソッドを呼び出してメンバ変数に値を格納しました。

# コンストラクタ

## コンストラクタとは

クラスからオブジェクトを作成した際に、無条件で実行されるメソッドのことで、メンバ変数の初期化などの主に行います。   
通常のメソッドの戻り値の型指定が無いものと考えて下さい。またメソッド名はクラス名と同じ名前にします。   

## デフォルトコンストラクタ

引数無しで中身が空のコンストラクタが作成されます。中身が空ですので何もしません。

```java
public class Car { 
    String model;   //メンバ変数

    //デフォルドコンストラクタ
    Car() {
    }

    void setModel(String newModel) {
        this.model = newModel;
    }


    void displayModel() {
        System.out.println("車のモデルは" + model + "です。");    
    }

}
```

***or***

```java
public class Car { 
    String model;   //メンバ変数

    void setModel(String newModel) {
        this.model = newModel;
    }


    void displayModel() {
        System.out.println("車のモデルは" + model + "です。");    
    }

}
```

***上記のようにコンストラクタを1つも定義していない場合、自動的にデフォルトコンストラクタと呼ばれるコンストラクタが作成されます。***   

デフォルトコンストラクタがあるクラスそれともコンストラクタを1つも定義していないクラスのオブジェクトは下記のように作成します。

```java
public class Main {

    public static void main(String[] args) {
        Car car = new Car();
    }

}

```

## 引数があるコンストラクタ

コンストラクタにはメソッドと同じように引数を指定することが出来ます。   
引数があるコンストラクタについて実際の使い方としては下記のようになります。

```java
public class Car { 
    String model;   //メンバ変数

    //引数があるコンストラクタ
    Car(String model) {
        this.model = model;
    }

    void displayModel() {
        System.out.println("車のモデルは" + model + "です。");    
    }

}

```

引数がある場合のコンストラクタを使用する場合、そのクラスからオブジェクトを作成する際に下記のように記述します。

```java
public class Main {

    public static void main(String[] args) {
        Car car1 = new Car("Toyota");
        car1.displayModel();

        Car car2 = new Car("Honda");
        car2.displayModel();
    }

}

```

出力は下記のようになります。

```java
車のモデルはToyotaです。
車のモデルはHondaです。
```

オブジェクト毎に異なる値をオブジェクト作成時に設定したい設置場所はコンストラクタの引数に指定してコンストラクタの中で設定します。

## 引数が異なるコンストラクタ

引数の数や型が異なるものであれば、1つのクラスの中に複数のコンストラクタを記述できます。   
下記の例をみて下さい。

```java
public class Car { 
    String model;   //メンバ変数

    //デフォルドコンストラクタ
    Car() {
    }

    //引数があるコンストラクタ
    Car(String model) {
        this.model = model;
    }

    void setModel(String newModel) {
        this.model = newModel;
    }

    void displayModel() {
        System.out.println("車のモデルは" + model + "です。");    
    }

}

```

引数が異なるコンストラクタのオブジェクトを作成する際に下記のように記述します。

```java
public class Main {

    public static void main(String[] args) {
        Car car1 = new Car("Toyota");
        car1.displayModel();

        Car car2 = new Car();
        car2.setModel("Mercedes");
        car2.displayModel();
    }

}

```

引数が異なるコンストラクタのオブジェクトは上記のように作成することが異なります。   
出力は下記のようになります。

```java
車のモデルはToyotaです。
車のモデルはMercedesです。
```

# まとめ

Javaのコンストラクタについては以上となります。次はコンストラクタについての課題をやってみましょう。

