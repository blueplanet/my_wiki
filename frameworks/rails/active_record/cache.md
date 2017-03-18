## Rails 機能
- 一回の「リクエスト -> レスポンス」の処理の中、同じSQLであれば、キャッシュしてくれる
  - [Rails のクエリキャッシュの仕組みを調べた - takatoshiono's blog](http://takatoshiono.hatenablog.com/entry/2015/06/20/005835)
  - [Caching with Rails: An Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/caching_with_rails.html#sql-caching)
- SQL+条件値をキーとしてキャッシュされる
- 疑問
  - [ ] どこのキャッシュしている？
  - [ ] どうやってレスポンスが終わったら消える？

  
## 複数DBの場合
- キャッシュは、接続DB単位で分けている？
