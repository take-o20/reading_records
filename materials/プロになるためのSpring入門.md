# プロになるためのSpring入門


土岐 孝平. プロになるためのSpring入門ーーゼロからの開発力養成講座 Software Design plus (p. 258). (Function). Kindle Edition.

## きっかけ

Springについて知りたいと思ったから。

# 第1部 基本編
## 第1章 Springの概要

* 2003年ごろからOSSプロジェクトが始まった
* SpringとSpring Bootは別ものである

## 第2章 Webアプリケーションの全体像

* いい復習になった。
  * Controller
  * Service
  * Repository
  * Entity
  * View
  * Input

## 第3章 DIという考え方

* ハンズオンがわかりやすかった
  * VSCodeで実行しやすくて良かった。

## 第4章 DIコンテナの概要

* 依存注入用の入れもの
* 用語: p81
  * Bean
  * Bean定義
  * コンフィグレーション
  * Application Context
* Bean定義には３つの手段がある
  * ステレオタイプアノテーション
  * @Beanメソッド
  * <bean>タグ

## 第5章 ステレオタイプアノテーション

* よく見かける
* インジェクションの方法には3種類ある
  * コンストラクタインジェクション
  * Setterインジェクション
  * フィールドインジェクション
* 同じ型のBeanが複数存在した場合のインジェクションの挙動→コンパイルエラーとなる
  * こういった説明があるのはいいなと思った。気になっていた箇所であった。


## 6章　プロファイルを用いたコンフィグレーションの切り替え

* Beanを切り替えることができる

## 7章 JavaConfigと@Beanメソッド

* @Configurationを付与したもの。同じパッケージ内なら自動でコンポーネントスキャンができる。あるConfigクラスから別のConfigクラスをインポートできる。
* @Bean: Beanを作る
  * ステレオタイプアノテーションができない外部ライブラリなどの場合に使える。
  * デメリットは管理が面倒であること
* ハンズオンのオプション問題にあるように全てBeanメソッドで定義すると、プログラムが肥大化するなと思った。コンストラクタの引数にあるリポジトリなども全てBeanメソッドで定義しなければならないから。

## 8章 Spring JDBCを使用したデータベースアクセス

* JDBCとは？
  * Java Database Connectivity(JDBC)
* Spring JDBCとは？
  * JDBCをラップしたもの。ソースコードがシンプルになる。
* p141: Spring JDBCの利用が効果的なケース
* ハンズオンでよく理解できた。7章の箇所もよく理解できた。
  * Bean定義の引数に他のDI対象を定義すればいい
    ```java
    @Bean
    public ABC abc(){return new ABCImple()}
    public CDE cde(ABC abc){return new CDEImple(abc)}
    ```

## 9章 宣言的トランザクション

## 10章 Spring Bootによる生産性の向上

## 11章 Spring MVC + Thymeleaf

## 12章 RESTful Webサービスの作成


## 13章 更新系のREST APIの作成

## 14章 Spring Securityを用いた認証と認可


# 第2部 詳細編
## 15章 シングルトンとスレッドセーフ


## 32章 Selenideを用いたE2Eテスト


