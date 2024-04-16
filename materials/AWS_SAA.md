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



## 所感.
* 質問に答えるだけで簡単そう。


