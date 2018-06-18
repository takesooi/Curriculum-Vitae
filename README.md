# 職務経歴書

### 言語
|key|value|
|---|-----|
|C#|7年|
|lua|1年|
|JavaScript|3年|
|TypeScript|1年|
|powershell|3年|
|VB|1年|

### フレームワーク・ライブラリ
- nginx-luajit-ws
- SignalR
- Hangfire
  - バッチサーバーで使用
- Entity Framework Core、Dapper
- REDIS：StackExchange、Booksleeve、ServiceStack
- IIS、SelfHost、Nancy
- Lz4、MessagePack、ZeroFormatter、Jil
- TopSelf
- AWS：AutoScaling、Instance調整、Build、Deploy周り、Lambda
- Unity：NW、Script、UniWebview
- BigQuery(ETW) ログ蓄積
- MYSQL、SQLSERVER

### CI
- Jenkins、AppVeyor

### 強み
- サーバーサイド以外にもインフラ、クライアントの知識があり、またそこの知識を勉強しています。
- 新規コンテンツのチーフを任されることが多かったため、新しいことや問題解決能力に優れている。
- トラブルシューティングでは以下を使用して解析していました。
  - debug diagnostic tool、WinDbgを使用したメモリ解析
  - perfviewを使用したスレッド解析
  - PerformanceCounterの使用

### 興味があるもの
- GCP、AWS、Unity周りをどんどん触っていきたい。フルスタックなエンジニアに興味あり

## 職務経歴

- 2008/04 - : ソフトウェア興業 入社
 - 開発部所属
- 2011/04 - : ソフトウェア興業 退社
 - 開発部所属
- 2011/07 - : 株式会社gloops（グループス）入社  
現在に至る

## 開発経歴
### 株式会社gloops（グループス）（2011/07~現在）
#### [新規]モバイルアプリ開発・運用（2015/04~現在）
- 概要：IOS、Android向けNativeアプリのサーバー開発、リアルタイムバトル
- 役割：チーフエンジニア
- プロジェクト規模：25名
- 業務内容：
  - C# 
    - 機能実装、NW、Websocket、パフォーマンスチューニング
  - Unity
    - NW、Script、UniWebview
  - TypeScript、javascript
    - のちにFullNativeに移行
  - AWS
    - AutoScaling、Instance調整、Build、Deploy周り、Lambda
  - Lua
    - Nginx(コネクションサーバー) → Disque(キューサーバー)の実装
  - MYSQL
    - PerformanceSchemeを使用してプロファイリング
  - BigQuery(ETW) ログ蓄積
  - Kibana、Fluentd
  - トラブルシューティング
    - debug diagnostic tool、WinDbgを使用したメモリ解析
    - perfviewを使用したスレッド解析
    - PerformanceCounterの使用

- テスト
  - MSTest
  - 負荷テスト
    - locust、jmeterを試したが負荷ツール側に状態を保持する必要があり、また大量のオブジェクト作成が必要なため、共通ライブラリ(クライアント-サーバー間インターフェイス)を使用した独自負荷ツールを作成した。結果は短期間でのツール作成と、容易なシナリオ作成を可能とした、ツールのパフォーマンスに問題なし。
    - 機能テスト、シナリオテストを実行でき、ViewにてTPSなど確認可能

- コード自動化
  - MYSQL用のPocoGeneraterの実装
  - T4にて自動化できそうなものは自動化

- サーバー構成
   - API
     - ALB、EC2(api)
   - Websocket
     - ALB、Nginx、Disque、EC2(game、matching、battle)
  - Aurora(Mysql5.7)
  - ElastiCache(redis)
   
- その他
  - デプロイ
    - [Api] CodeDeploy(AWS)
    - [Game]CodeDeploy + RollingDeploy(独自)
       - Onlineデプロイが可能

- 開発思考
  - DDD、コンポーネント思考

#### システム基盤部・運用・保守（2014/04~2015/04）
- 概要：システム基盤(DB担当)
- 役割：メンバー
- プロジェクト規模：10名
- 業務内容：
    - システム設計
    - 保守、トラブルシューティング
    - パフォーマンスチューニング
      - DMVを使用した解析
    - SqlServer2008、2012、2016
    - MYSQL→SqlServerのマイグレーション
    - ログ配布、AlwaysOn
    - re:dash
    - Zabbix、grafana 監視
    - 検証(SQLServer2016、IOPS)

#### [既存]モバイルアプリ開発・運用（2013/04~2014/04）
- 概要：サーカーIP、IOS、Android向けNativeアプリのサーバー開発
- 役割：メンバー
- プロジェクト規模：25名
- 業務内容：
    - C# 
      - イベント実装がメインでトラブルシューティング、自動化の実装
      - スレッドのデッドロックが発生したので非同期実装への改修
    - SQLServer
      - Dapper、Dataset
    - Redis
      - Booksleeve       

#### [新規]モバイルアプリ新規開発・運用（2012/07~2013/04）
- 概要：アニメIP、IOS、Android向けWebアプリのサーバー開発
- 役割：チーフエンジニア
- プロジェクト規模：25名
- 業務内容：
    - C# 
      - 新規開発(6か月)
        - 機能実装、自動化の実装、パフォーマンスチューニング
      - 運用(3か月)
        - イベント実装、トラブルシューティング
    - SQLServer
      - Dapper、Dataset
    - Redis
      - ServiceStack

#### [新規]モバイルアプリ開発・運用（2012/04~2013/04）
- 概要：競馬IP、IOS、Android向けWebアプリのサーバー開発
- 役割：チーフエンジニア
- プロジェクト規模：25名
- 業務内容：
    - C# 
      - 新規開発(5か月)
        - 機能実装、自動化の実装、パフォーマンスチューニング
      - 運用(7か月)
        - イベント実装、トラブルシューティング
    - SQLServer
      - Dataset
    - Redis
      - ServiceStack
- その他
  - 毎月、右肩上がりに売り上げが伸びたコンテンツとして記録

#### モバイルアプリ開発・運用（2011/07~2012/04）
- 概要：野球IP、IOS、Android向けWebアプリのサーバー開発
- 役割：メンバー
- プロジェクト規模：25名
- 業務内容：
    - C# 
      - 新規開発(1か月)
        - 機能実装
      - 運用(8か月)
        - イベント実装、トラブルシューティング
    - SQLServer
      - Dataset
    - Redis
      - ServiceStack
- その他
  - 入社当初のコンテンツ、売り上げ規模は一番のコンテンツでした。

### ソフトウェア興業 SIer（2008/04~2011/04）
#### 自動車部品管理WEBシステム
- フェーズ：基本設計～結合テスト
- java、DB2、struts、JSP
  
#### 銀行システムデーター集計バッチ改修
- フェーズ：基本設計～結合テスト
- Oracle、COBOL、PL/SQL
  
#### 銀行システムWEB開発
- フェーズ：製造～結合テスト
- VB、SQLServer

#### 銀行システム総合テスト
- フェーズ：総合テスト
- シナリオ作成、本番構築、テスト
