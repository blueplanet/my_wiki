## Rails 機能
- 一回の「リクエスト -> レスポンス」の処理の中、同じSQLであれば、キャッシュしてくれる
  - [Rails のクエリキャッシュの仕組みを調べた - takatoshiono's blog](http://takatoshiono.hatenablog.com/entry/2015/06/20/005835)
  - [Caching with Rails: An Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/caching_with_rails.html#sql-caching)
- SQL+条件値をキーとしてキャッシュされる
- 疑問　　  
  - [x] どこにキャッシュしている？  
    - [rails/query_cache.rb at 0ce641839aa59d8c8306ec21cfd5f31aaa9b169c · rails/rails](https://github.com/rails/rails/blob/0ce641839aa59d8c8306ec21cfd5f31aaa9b169c/activerecord/lib/active_record/connection_adapters/abstract/query_cache.rb) の `cache_sql` でキャッシュしている    
  - [ ] QueryCacheのインスタンスはいつ、どこで作成される？
  - [x] どうやってレスポンスが終わったら消える？   
    - [rails/query_cache.rb at master · rails/rails](https://github.com/rails/rails/blob/master/activerecord/lib/active_record/query_cache.rb) の `complete` メソッドでクリアしている
    
## 複数DBの場合
- [x] キャッシュは、接続DB単位で分けている？  
　　  - 違う。リクエスト単位でキャッシュする
- [x] connection はどこで新規している？  
 　　 - そのリクエストの中、最初のクエリが発行される時connectionを取得する
  
## 参考リンク
- [[Ruby] 例えば、ActiveRecord の connection_pool を止める - sonots:blog](http://blog.livedoor.jp/sonots/archives/38797925.html)
