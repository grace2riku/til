* ターミナルのタイトル変更。macOS, iTerm2で確認。

ファイル ~/bin/nameiterm につぎが書いてあるとする。

```
#! /bin/bash
echo -ne "\033]0;$1\007"
```

つぎはターミナルのタイトルを1に変更する例
```
$ bin/nameiterm 1
```

つぎはターミナルのタイトルをNewに変更する例
```
$ bin/nameiterm New Title
```

つぎはターミナルのタイトルをNew Titleに変更する例
```
$ bin/nameiterm "New Title"
```
