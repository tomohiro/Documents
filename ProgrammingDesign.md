# Programming Design

## MVC

### 1979年の原典

- [Trygve Reenskaug「MODELS - VIEWS - CONTROLLERS」（原文公開日：1979年12月10日）](http://heim.ifi.uio.no/~trygver/1979/mvc-2/1979-12-MVC.pdf)
- [和訳](http://d.hatena.ne.jp/digitalsoul/20100913/1284330448)

> モデルは知識の表象です。モデルは１つのオブジェクトであるかもしれませし（あまり面白くはありませんが）、複数のオブジェクトからなる構造かもしれません。
>
> モデルとその一部には一対一の対応関係がある一方で、モデルとその所有者によって知覚された世界の表象との間にも一対一の対応関係があります。


## アーキテクチャパターン

- [Amazon.co.jp： エンタープライズ アプリケーションアーキテクチャパターン (Object Oriented Selection): マーチン・ファウラー, 長瀬 嘉秀, 株式会社 テクノロジックアート: 本](http://www.amazon.co.jp/%E3%82%A8%E3%83%B3%E3%82%BF%E3%83%BC%E3%83%97%E3%83%A9%E3%82%A4%E3%82%BA-%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%A2%E3%83%BC%E3%82%AD%E3%83%86%E3%82%AF%E3%83%81%E3%83%A3%E3%83%91%E3%82%BF%E3%83%BC%E3%83%B3-Object-Oriented-Selection/dp/4798105538)
- [PofEAA's Wiki - FrontPage](http://capsctrl.que.jp/kdmsnr/wiki/PofEAA/)


## トランザクションスクリプト

- [いまさらきけない「ドメインモデル」と「トランザクションスクリプト」 - ひがやすを blog](http://d.hatena.ne.jp/higayasuo/20080519/1211183826)

> 私は一番最初に「ユースケースと一対一にサービスクラスを設け、ビジネスロジックはサービスクラスに記述する」という主張をしてました。
>
> 記念すべき(?)第一回のダイコン時代の設計法でそういってますね。
>
> http://d.hatena.ne.jp/higayasuo/20040606/1086495806
>
> どうしてそうしたほうが良いかというと、ユーザの要件であるユースケースとその実装であるサービスクラスが一対一に結びついていたほうが、要件の変更が入ったときに、どのクラスを修正すればいいか一目瞭然なので、メンテナンス性が高いと考えたからです。
>
> この方法は、トランザクションスクリプトではないと私は主張しました。手続き分割していくわけではなく、ユースケースごとに最も責任を持つクラスに分割しているし、DIによってオープンクローズの原則(OCP)もきちんと間持ているからです。
>
> http://d.hatena.ne.jp/higayasuo/20050510
>
> オープンクローズの原則の詳細はこちら。
>
> http://www.morijp.com/masarl/homepage3.nifty.com/masarl/article/dp-ocp.html
>
> でも、今から思うとこのやり方は、トランザクションスクリプトですね。PofEAAは注意深く読み直してみると、ユースケース(アクション)中心にオブジェクト(メソッド)を組み立てるのがトランザクションスクリプトで、ドメインオブジェクトを中心にオブジェクトを組み立てるのがドメインモデルだからです。


## メンタルモデルを反映するアーキテクチャパターン

### ドメイン駆動設計 (DDD: Domain Driven Design)

- [Domain Driven Design（ドメイン駆動設計） Quickly 日本語版](http://www.infoq.com/jp/minibooks/domain-driven-design-quickly)
- [ドメイン駆動設計入門 - Digital Romanticism](http://d.hatena.ne.jp/digitalsoul/20101027/1288180208)
- [[ 技術講座 ] Domain-Driven Designのエッセンス 第1回](http://www.ogis-ri.co.jp/otc/hiroba/technical/DDDEssence/chap1.html)
- [[ 技術講座 ] Domain-Driven Designのエッセンス 第2回](http://www.ogis-ri.co.jp/otc/hiroba/technical/DDDEssence/chap2.html)
- [[ 技術講座 ] Domain-Driven Designのエッセンス 第3回](http://www.ogis-ri.co.jp/otc/hiroba/technical/DDDEssence/chap3.html)

#### DDD 実践例

- [ドメイン駆動設計を実践するために - Digital Romanticism](http://d.hatena.ne.jp/digitalsoul/20101223/1293110547)
- [SNSチームでのドメイン駆動設計の実践 | GREE Engineers' Blog](http://labs.gree.jp/blog/2013/12/9330/)
- [Scalaコードでわかった気になるDDD | GREE Engineers' Blog](http://labs.gree.jp/blog/2013/12/9354/)
- [ユビキタス言語とドメインモデル、そしてモデル探索のうずまき - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2013/05/07/domain-model/)
- [シナリオ -> モデル -> コード -> - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2013/05/11/sinario-model-code/)
- [Scala with DDD - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2013/12/02/scala-with-ddd/)
- [ドメインモデルの関連を表現するには - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2013/06/02/ddd-entity-reference/)
- [ServiceとDCIについて ~振る舞いはどこにあるべきか~ - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2014/01/03/dci-service/)


### DCI (Data Context Interaction)

- [DCIアーキテクチャ - Trygve Reenskaug and James O. Coplien - Digital Romanticism](http://d.hatena.ne.jp/digitalsoul/20100131/1264925022)
- [DCIアーキテクチャの実装：ローンシンジケート - Digital Romanticism](http://d.hatena.ne.jp/digitalsoul/20100515/1273925906)
- [Modegramming Style: DCI (Data Context Interaction)](http://modegramming.blogspot.jp/2012/03/dci-data-context-interaction.html)

#### DCI 実装例

- [ServiceとDCIについて ~振る舞いはどこにあるべきか~ - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2014/01/03/dci-service/)
- [ScalaでのDCIの実装を考える - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2013/12/24/dci/)
- [traitで簡単にDCIを実装する - じゅんいち☆かとうの技術日誌](http://j5ik2o.me/blog/2014/01/07/dci-trait/)
