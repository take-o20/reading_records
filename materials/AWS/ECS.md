# ECS（Elastic Container Service）
* 完全に管理されたコンテナオーケストレーションサービスである。
* Amazon Elastic Compute Cloud や AWS Fargateで実行できる
    * Amazon ECS Anywhereのオンプレミスインフラストラクチャでも実行できる。


## オートスケーリング
* ECSは使用中サービスのCPUとメモリの平均使用量を含むCloudWatchメトリクスを発行する。
* スケールアウト（実行するタスクを増やす）
* スケールイン（実行するタスクを減らす）
* サポートするオートスケーリング
    * 特定のメトリクスのターゲット値に基づいて、サービスが実行するタスク数を増減させる
    * アラーム超過のサイズに応じて変動する一連のスケーリング調整値 (ステップ調整値) に基づいて、サービスが実行するタスク数を増減させる。
    * 日付と時刻に基づいてサービスが実行するタスクの数を増減させる。

## Amazon ECS クラスターの自動スケーリング
* https://docs.aws.amazon.com/ja_jp/AmazonECS/latest/developerguide/cluster-auto-scaling.html#update-ecs-resources-cas
