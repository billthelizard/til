## データレイク

さまざまなデータを**オリジナルのデータ形式のまま**格納した場所.
構造化されていなくても良い.

### 類似の用語:

* エンタープライズデータウェアハウス (EDW): 企業全体向けサービスを提供するデータウェアハウス。
* データマート: 個々の部門によって利用されユーザが現在必要としているデータをより最適化された形で利用。
* データスワンプ: 失敗したデータレイクの揶揄。なんでも入るからと、計画性のないデータ蓄積を行うとレイク（湖）は、すぐに使いにくいスワンプ（沼）となる。

参考:
https://blogs.oracle.com/bigdata-dataintegration-jp/data-lake-database-data-warehouse-difference_jp

## ETL (Extract/Transform/Load)

データウェアハウスに格納されるまでのデータ処理の過程のこと:

* Extract - 抽出
* Transform - 変換
* Load - ロード

参考:
https://ja.wikipedia.org/wiki/Extract/Transform/Load

## AWS Lake Formation

AWSが提供しているデータレイクのマネージドサービス.

* Security & Access Control
  * Data encryption
  * Access Control with IAM
  * Logging with CloudTrail
* Pre-processing
  * Cleaning
  * Partitioning
  * Indexing
* Storage: S3

![aws-lake-formation](https://i.imgur.com/ZAV13l7.png)

> データソースに Lake Formation をポイントするだけで、Lake Formation はソースをクロールし、
> 新しく作成した Amazon S3 データレイクにデータを移動します。
> Lake Formation は S3 内のデータを頻繁に使用されるクエリ用語で整理し、適切なサイズにまとめ、効率性を向上します。

参考:
https://aws.amazon.com/jp/lake-formation/

詳細な説明: Re:Invent Speech by Rahul Pathak - GM, Amazon Athena & Amazon EMR
- [ANT396 - Intro to AWS Lake Formation - Build a secure data lake](https://www.youtube.com/watch?v=nsiLMqg654s)

## Schema on read vs. schema on write

![data-lake-vs-data-warehouse](https://i.imgur.com/AcMgqdc.png)

https://aws.amazon.com/jp/big-data/datalakes-and-analytics/what-is-a-data-lake/

## Data lineage (データ系統)

> Data lineage includes the data's origins, what happens to it and where it moves over time. Data lineage gives visibility while greatly simplifying the ability to trace errors back to the root cause in a data analytics process.

https://en.wikipedia.org/wiki/Data_lineage
