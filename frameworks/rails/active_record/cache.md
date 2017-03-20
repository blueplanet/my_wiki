## Rails 機能
- 一回の「リクエスト -> レスポンス」の処理の中、同じSQLであれば、キャッシュしてくれる
  - [Rails のクエリキャッシュの仕組みを調べた - takatoshiono's blog](http://takatoshiono.hatenablog.com/entry/2015/06/20/005835)
  - [Caching with Rails: An Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/caching_with_rails.html#sql-caching)
- SQL+条件値をキーとしてキャッシュされる
- 疑問
  - [ ] どこのキャッシュしている？
  - [ ] どうやってレスポンスが終わったら消える？
  
## 複数DBの場合
- [x] キャッシュは、接続DB単位で分けている？  
　　  - 違う。リクエスト単位でキャッシュする
- [x] connection はどこで新規している？  
 　　 - そのリクエストの中、最初のクエリが発行される時connectionを取得する
  
## 参考リンク
- [[Ruby] 例えば、ActiveRecord の connection_pool を止める - sonots:blog](http://blog.livedoor.jp/sonots/archives/38797925.html)
