# IAM・認証

## Amazon Cognito
* 顧客ID・アクセス管理サービスを提供する
    * ウェブアプリケーションやモバイルアプリケーションの認証、許可、ユーザー管理を実装できるサービスである
* ID管理
* ユーザー認証
    * フェデレーション
    * MFA(Multi Factor Authentication) - 多要素認証
* アクセスコントロール
    * AWSサービスへのSingle-Sign-Onなど

## サービスコントロールポリシー (SCP)
* 組織内のIAMユーザーとIAMロールが使用できる最大権限を一元管理できる
* アカウントが組織のアクセスコントロールガイドラインに従っていることを確認するのに役立ちます。

## IAM データベース認証（Identity and Access Management）
* 通常データベースへのアクセスはユーザーとパスワードを用いて行うが、ユーザー名とパスワードを管理する必要がある。
* IAMユーザーがAWSのデータベースサービスにアクセスする際の認証サービスを提供する。
* トークンを使用する
* サポートデータベースサービス
    * Aurora MySQL
    * Aurora PostgreSQL 

## STS
* Security Token Service
    * AWS STSを利用したウェブ ID フェデレーション


## SCPとIAMポリシー
* 双方で明示されている権限だけがユーザーに適用される
    * SCPとIAMポリシーの共通部分のみ

## AD Connector
AD ConnectorはIAMとオンプレミス環境のMS Active Directoryとを連携するのに利用します


## AWS Organizations
* Service Control Policy
    * ルートアカウント単位で組織(OU)を管理するためのポリシータイプ
    * 組織単位であるためユーザー単位ではない <-> OU単位
        * ユーザー単位はIAMポリシーによって行う