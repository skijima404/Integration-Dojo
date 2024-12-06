# 参考資料

Integration Dojo 受講後、自己学習をしたい場合に備えて参考資料を共有します。

## インテグレーションを使ったデザインパターン

### Enterprise Integration Patterns (英語)
[Webページへのリンク](https://www.enterpriseintegrationpatterns.com/)
[本で読みたい場合はこちら](https://amzn.asia/d/dPe4grj)

CamelやMuleSoftといったインテグレーション基盤はEnterprise Integration Patternsのパターンを組みわせて簡単に実装できるツールとして利用できるようになっています。

### Microservices.io
[Webページへのリンク](https://microservices.io/)
[本で読みたい場合はこちら](https://amzn.asia/d/21EvC3q)

マイクロサービスアーキテクチャのデザインパターンの紹介です。
質問が多いものはこちら
- [Saga: 長いトランザクションの実装方法](https://microservices.io/patterns/data/saga.html)
- [ACID特性](https://microservices.io/articles/dark-energy-dark-matter/dark-matter/prefer-acid-over-base.html)

[Dark Energy and Dark Matter](https://microservices.io/tags/dark%20energy%20and%20dark%20matter) シリーズは、インテグレーションには特化してはいないものの、インテグレーションの設計以前の考慮事項からの指針が記述されています。

## 要素技術の解説

### API Gateway

API Gatewayはなぜ必要かを解説したものは、製品概要がわかりやすいです。
[API Gateway概要 (日本語)](https://www.redhat.com/ja/topics/api/what-does-an-api-gateway-do)

API Gatewayとはそもそも何かという解説。

### インテグレーション基盤

そもそもなぜこのような基盤が必要なのかは、CamelやMuleSoftの解説がわかりやすいです。

[Apache Camel超入門 (日本語)](https://rheb.hatenablog.com/entry/2022/05/27/191550)
[システム連携基盤サービス：MuleSoft (日本語)](https://www.tis.jp/service_solution/mulesoft/)

書籍ではMuleSoftのガイドブックの1章で詳しく解説されています。ハンズオン部分で具体的なユースケースも読めるため、わかりやすいです。
[MuleSoftで学ぶAPIシステム連携ガイドブック (日本語)](https://amzn.asia/d/9bUxKXc)

### イベント連携基盤

[Apache Kafka Performance](https://developer.confluent.io/learn/kafka-performance/)
イベント連携のレイテンシーが気になる方が多いですが、Confluent社のベンチマークによると99％は5ms以内に連携されているという結果が出ています。

[Apache Kafka is NOT Hard Real Time BUT Used Everywhere in Automotive and Industrial IoT](https://www.kai-waehner.de/blog/2021/01/04/apache-kafka-is-not-hard-real-time-industrial-iot-embedded-connected-vehicles-automotive/)
ハードリアルタイムでは利用できないものの、ほとんどの「リアルタイム」要件はソフトリアルタイムあるいはニアリアルタイムのため、Kafkaはほとんどのユースケースで利用できることを解説したもの。

### サービスメッシュ

[サービスメッシュについて理解する (日本語)](https://dev.classmethod.jp/articles/servicemesh/)
サービスメッシュの概要や仕組みを解説している記事。