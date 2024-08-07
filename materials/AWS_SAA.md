# AWSソリューションアーキテクトアソシエイト

## 試験概要
https://aws.amazon.com/jp/certification/certified-solutions-architect-associate/

## 勉強資料
* awsのドキュメント
    * https://docs.aws.amazon.com/index.html
    * https://docs.aws.amazon.com/ja_jp/index.html
* AWS Black Belt
    * https://www.youtube.com/playlist?list=PLzWGOASvSx6FIwIC2X1nObr1KcMCBBlqY
* ホワイトペーパー
    * AWSホワイトペーパー
        * https://aws.amazon.com/jp/whitepapers/
    * AWS Well-Architectedフレームワーク
        * https://docs.aws.amazon.com/ja_jp/wellarchitected/latest/framework/welcome.html
* ハンズオン
    * https://aws.amazon.com/jp/getting-started/hands-on/
    * https://aws.amazon.com/jp/training/digital/
    * https://aws.amazon.com/jp/events/aws-event-resource/hands-on/

## memo
### 2章 グローバルインフラストラクチャとネットワーク
* gatewayの種類と役割が述べられていた。
* VPNの種類について述べられていた。
    * 外部からVirtual Private Cloudに接続する方法。
* VPC間の通信はGWを介す必要がある。
    * スターネットワーク

### 3章 コンピューティングの関連サービス
* EC2 - Amazon Elastic Compute Cloud (EC2)
    * 仮想サーバーを提供する。
    * IaaS
    * Elastic Load Balancing(ELB)・Auto Scaling
* ECS - Amazon Elastic Container Service (ECS)
    * Dockerコンテナの実行環境
    * Elastic Kubernetes Service
* AWS Lambda
    * サーバーレスアーキテクチャ
    * 使ったことある


### 4章 ストレージサービス
* ストレージとストレージゲートウェイについて
    * ストレージはブロックストレージ、ファイルストレージ、オブジェクトストレージに分類される。
        * ブロックストレージは、EC2上などに存在し、RDB保存用などに使用される。
        * ファイルストレージはどこからでもNFSプロトコルを介してアクセスできる。
        * オブジェクトストレージはメディアファイルや大量なログなどを保存するために使用される。
            * REST APIを有している
    * ゲートウェイはオンプレにあるデータをクラウドストレージに送信する際に使う
        * 利用目的により複数種ある

### 5章 データベースサービス
サービスは以下の4種類に分類できる。
* RDB
* NoSQL
* 時系列
* 台帳

### 6章 ネットワーキングとコンテンツ配信
* CloudFront
    * キャッシュを使うことでCDNとしての役割を果たす
* Route 53
    * DNSの役割を果たす
* Global Accelerator
    * 2地点を高速なネットワークで繋げる仕組みである

### 7章 アイデンティティとガバナンス
* AWSアカウントとAWS Organizations
* IAM と IAMアイデンティティセンター

### 8章 セキュリティサービス
* 鍵管理
    * KMS と CloudHSM
        * Hardware Security Module
        * 前者をよく使う
        * HSMは大規模向けで、VPC内で専用のハードウェアを利用して鍵を管理する
* セキュリティサービス
* p214のコラム - saaの後に取る資格について


### 9章 アプリケーションサービス
* AWSのサーバー上に構築されている。構築・メンテナンスが不要なので、コスト面やセキュリティ面においても自前でつくるより良い
* キューサービスやSNS(Simple Notification Service)など

### 10章 分析サービスとデータ転送サービス
* 分散処理
    * Amazon EMR - Elastic MapReduce
    * 分散処理基盤
    * 分散処理アプリケーション基盤
        * Hadoop
        * Apache Spark
* 分析サービス
    * ETLツール - Elastic Transform Load
    * Kinesis
    * Data Pipeline
    * Athena 対話型分析ツール
    * Amazon QuickSight 視覚化ツール
* データ転送サービス
    * AWS Snowball

### 11章 コスト管理
* EC2/RDSのコスト管理
* コスト管理サービス

### 12章 運用支援サービス

### 13章 AWSのアーキテクチャ設計
* ホワイトペーパー
    * https://aws.amazon.com/jp/whitepapers
* AWS Well-Architectedフレームワーク
    * https://docs.aws.amazon.com/ja_jp/wellarchitected/latest/framework/welcome.html
* セキュアなアーキテクチャ
* 弾力性に優れたアーキテクチャ
* 高パフォーマンスなアーキテクチャ
    * リソースの選択
        * コンピューティングリソース
        * ストレージリソース
        * データベースリソース
        * ネットワークリソース
* コストを最適化したアーキテクチャ
    * AWSから外部への通信にはお金がかかる。
        * インバウンドにはかからないがアウトバウンドにはコストがかかる。
    * インスタンスの選択
        * オンデマンドインスタンス
        * リザーブドインスタンス
        * スポットインスタンス


## 所感.
* 質問に答えるだけで簡単そう。


## サービス
* Amazon EventBridge
    * イベントを使用してアプリケーションコンポーネント同士を接続するサーバレスサービス
* Amazon SageMaker
    * フルマネージド型の機械学習サービス
* AWS SQS - Simple Queue Service
* AWS Direct Connect
* AWS Site-to-Site VPN
* Amazon OpenSearch
    * ログ分析、リアルタイムのアプリケーションモニタリング、クリックストリーム分析などの、完全オープンソースの検索および分析エンジン
* Amazon OpenSearch Service
    * OpenSearchクラスターのすべてのリソースをプロビジョニングして、OpenSearchクラスターを起動する
* Amazon Kinesis Data Analytics
* Amazon Kinesis Data Firehose
* Amazon OpenSearch Service
* Amazon Kinesis Data Streams

### ネットワーキング
* AWS CloudFront
    * コンテンツ配信のルーティングを最適化する
        * html, javascript, 画像 etc..

### ストレージ
* SSE-KMS
    * Server Side Encryption - Key Managed Service

### データベースサービス
* Amazon DynamoDB
    * あらゆる規模で一桁ミリ秒のパフォーマンスを実現する、サーバーレス NoSQL フルマネージドデータベース

    
### 証明書
* AWS Certificate Manager
    * AWS サービスと内部接続リソースで使用するパブリックおよびプライベート SSL/TLS 証明書をプロビジョニング、管理、および展開します。ACM を使用すれば、SSL/TLS 証明書の購入、アップロード、および更新という時間のかかるプロセスを手動で行う必要がなくなります。
        * 自動更新できる証明書はAWSで発行したものに限る。（サードパティ証明書は手動）


### コンテナ
* AWS Fargate
    * コンテナ向けサーバーレスコンピューティング
        * サーバーの管理は不要でアプリケーションの実行ができ、使用したリソースに対し従量課金される。
* AWS ECS(Elastic Container Service)
    * フルマネージドのコンテナオーケストレーションサービスである
* AWS ECR(Elastic Container Registry)
    * ハイパフォーマンスホスティングを提供するフルマネージドコンテナレジストリである。
* Amazon Elastic Kubernetes Service (Amazon EKS)
    * AWS クラウドおよびオンプレミスデータセンターで Kubernetes を実行するためのマネージド Kubernetes サービスです。


### 機械学習サービス
* Amazon Transcribe
    * 音声をテキストに翻訳するサービス
* Amazon Textract
    * 光学文字認識
* Amazon Comprehend
    * 機械学習を使用して、テキストからインサイトや関係性を発見するための自然言語処理 (NLP) サービスです。
* Amazon Rekognition
    * 事前トレーニングされたカスタマイズ可能なコンピュータビジョン (CV) 機能を提供して、画像と動画から情報とインサイトを抽出します。





