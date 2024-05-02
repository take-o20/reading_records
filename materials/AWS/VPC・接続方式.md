# VPC・接続方式

## AWS Direct Connect
* https://aws.amazon.com/jp/directconnect/
* オンプレスミス環境などからAWSのサービスへ接続する専用回線のこと
* VPNに比べて割高だが、安定性・高速なネットワークを提供する

## AWS Site-to-Site VPN
* https://docs.aws.amazon.com/ja_jp/vpn/latest/s2svpn/VPC_VPN.html
* Amazon VPC内のインスタンスにリモートのユーザーがアクセスできるようにする機能を提供する
* VPCからリモートネットワークへのアクセスを有効にする

## AWS Transit Gateway
* VPC内のネットワークとオンプレスのネットワークを中央ハブで接続する
    * マルチキャストが可能になる

## VPC ピアリング
* 2つのVPCを接続する
    * パブリックインターネットを経由せずに接続が可能である

## NATゲートウェイ（Network Address Translation）
* ネットワークアドレス変換サービスを提供する
* VPCのアウトバウンド通信を許可するサービス
    * プライベートVPC内のインスタンスからインターネットへ接続する場合など
* NATゲートウェイを使用するとプライベートサブネット内のインスタンスはVPC外へのサービスへアクセスできる
    * VPC外のサービスはVPC内のサービスに接続できない
    * 一方通行

## NATインスタンス
* https://docs.aws.amazon.com/ja_jp/vpc/latest/userguide/VPC_NAT_Instance.html
* ネットワークアドレス変換サービスを提供する
* パブリックサブネットに置かれるインスタンス
    * プライベートサブネット内のインスタンスはこのインスタンスを踏み台としてインターネットと接続する。
* 現在はサポート終了している

## Elastic IPアドレス
* 静的なIPv4アドレス
* インターネットからアクセス可能なパブリックIPv4アドレス
* 静的であるため、EC2に設定した場合にEC2を停止してもIPアドレスが変更されない


## VPC
* Virtual Private Cloud
* 論理的に隔離されている定義済みの仮想ネットワーク内でAWSリソースを起動できる
* 1つのリージョン
* https://aws.amazon.com/jp/vpc/
* https://docs.aws.amazon.com/ja_jp/vpc/latest/userguide/what-is-amazon-vpc.html

## インターネットゲートウェイ
* VPCとインターネットとの接続を可能にするコンポーネントである
    * パブリックサブネット内のインスタンスがインターネットと通信可能になる
* IPv4とIPv6をサポートしている

