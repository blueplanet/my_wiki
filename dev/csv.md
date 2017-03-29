## CSV解析
- セル内改行
  - セル内改行がある場合だけ、row_sep: "\r\n"を設定する
    - Windowsで作成した場合、セル内改行は"\n"になる
    - MacOSで作成した場合、セル内改行は"\r"になる
  - セル内改行がない場合は、row_sepオプションを設定しないこと
- gitにテスト用ファイルとか、特にWindowsで作成したCSVファイルコミットする時は、`autocrlf`オプションを`false`にしないと変換されてしまうので、不整合が発生してしまう
  - [git での改行コード - Qiita](http://qiita.com/shuhei/items/2da839de8803cb335f86)
