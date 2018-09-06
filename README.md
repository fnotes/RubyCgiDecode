# RubyCgiDecode
Ruby用のCGIデコード。PHP風にデータを扱えるようにします。

    require './CgiDecode.rb'
    q = CgiDecode.new
    # $_GET,$_POST,$_COOKIE,$_FILES が使えるように
---
+ ファイルは一時ファイルとして/tmp/に保存されます
+ $_FILES にはファイル情報のみが入っています
+ ファイルはチェック後、移動してください
---
    $_FILES.each_with_index do |f,i|

        # f['name'] form name
        # f['type'] file type
        # f['up_name'] upload file name
        # f['tmp_name'] /tmp/*****
        new_name = q.move(f,'save_name')
    end

---
さらに詳しくは下記に掲載しています  
https://code-notes.com/lesson/21
---
This software is released under the MIT License, see LICENSE.txt.
