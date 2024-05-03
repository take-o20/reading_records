# ELB
3種類のロードバランサー(ALB, NLB, CLB)の総称である。


## 機能
* ヘルスチェック
    * Ec2インスタンスの正常／異常を確認し、利用するEC2の振り分けを行う。
* クロスゾーン負荷分散
    * EC2の負荷に応じて複数のAZに跨るEc2インスタンスに負荷分散を行う
* 暗号化通信
* スティッキーセッション
    * 同一セッションでは同じEC2インスタンスを使う
* Connection Draining
    * 
* ログ取得
    * S3バケットにログ収集する

## CLB
* Classic Load Balancerの略
* 旧タイプのロードバランサー
* レイヤー4と7で動作する

## NLB
* Network Load Balancer
* レイヤー4で動作する

## ALB
* Application Load Balancer
* HTTP(S)のトラフィックを負荷分散する


## word
* draining
    * 排出させる、はかせる
* レイヤー4負荷分散
    * IPアドレスやポート番号で負荷分散する
* レイヤー7負荷分散
    * HTTP(S)プロトコル、URLタイプ、クッキーデータで負荷分散する
