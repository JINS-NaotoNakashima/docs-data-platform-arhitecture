# データ分析基盤アーキテクチャ構築の記事メモ

内製開発のためのSnowflakeデータアーキテクチャ

内製開発ゆえの開発方針をしめす
  - 関係個所が広く変更の影響を受けやすい
  - その割に定常的な保守が必要
  - コストをかけるべき場所でもない
  ⇒ 外部に依存すると改修コストが青天井・アジリティも損なわれる

主要なファクターに対してそれぞれ3通りのアプローチを示す。

- データモデル
  - 純データレイク
  - ディメンショナルモデリング
  - DataVault + ディメンショナルモデリング
- データ取込
  - 内部ステージ
  - 外部ステージ
  - SnowflakeOpenFlow
- データ変換
  - DynamicTable
  - dbt
  - Snowpark
- ジョブオーケストレーション
  - dbtCloud
  - dbtProject on Snowflake
  - AirFlow
- リソース管理
  - SnowSight
  - Terraform
  - SnowflakeDevOps(SnowflakeCLI, SnowflakePythonAPI)
- データカタログ
  - dbtCloud
  - SnowflakeHrizonCatalog
  - OpenMetadata
- ロール設計
  - 最小構成
  - リテラシー・役割軸
  - 組織・ドメイン軸
- BIツール
  - GoogleSpreadSheet
  - LookerStudio
  - Streamlit

[選択肢がないのでAppendix]
- アラート設計
- テスト手法
