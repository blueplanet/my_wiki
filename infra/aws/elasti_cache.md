## フェイルオーバー
- [ElastiCache がフェイルオーバーした際に気をつけるべき redis-rb の利用方法について - Qiita](http://qiita.com/dany1468/items/8946cd5e4c853b48bffd)
  - フェイルオーバーしたら、サーバー側再起動とかで復帰できますが、Rails側は対応が必要
  - 上記記事によると、Sidekiqは大丈夫だが、他の箇所でたとえconnection poolなどを使っている場合は、再起動または特別の対応が必要
  - unicorn などを再起動すれば接続しなおすので、復帰できる
  
