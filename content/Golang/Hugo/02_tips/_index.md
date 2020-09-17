---
title: "[メモ] 役に立ちそうなこと"
date: 2020-09-17T18:41:34+09:00
draft: false
weight: 2
---

## 記事を書くときに役に立ちそうなこと

### chapter に関する tips
* 新しい Chapter を作る
```sh
hugo new --kind chapter content/{chapter-name}
```


#### chapter の header要素
* chapter の header要素 (例)
```
---
title: "Golang"
date: 2020-09-16T18:26:35+09:00
draft: false
chapter: true
pre: "<b>1. </b>"

(ここから chapter の中身)
---
```


* chapter の header の意味
```
---
title: "Golang"                          # <= (string) chapter の名称, 右のスクロール部分にタイトルとして出る"
date: (date?) 2020-09-16T18:26:35+09:00  # <= (date?) chapter を作成した日時, hugo new で作成すると自動的に埋め込まれる
draft: false                             # <= (boolean) 公開するかどうか / この chapter が下書き (準備中) かどうか (false にしないと公開されない, ローカル (サーバ) でも公開されないので注意)
chapter: true                            # <= (boolean) この _index.md が chapter であることを宣言
pre: "<b>1. </b>"                        # <= (string/html) chapter の通し番号 (tex みたいに自動生成にならないかなあ...ちょっと難しそう)
---

(ここから chapter の中身)
```


### エントリに関する tips
* 新しい記事 (エントリ) を作る
```sh
hugo new content/{path/to/entory}/_index.md
```

例: この記事
```sh
hugo new content/Golang/Hugo/02_tips/_index.md
```

#### エントリの header要素
* エントリの header要素 (例: この記事)
```
---
title: "[メモ] 役に立ちそうなこと"
date: 2020-09-17T18:41:34+09:00
draft: false
weight: 2
---

(ここから記事の内容)
```


* エントリの header の意味
```
---
title: "[メモ] 役に立ちそうなこと"   # <= (string) この記事のタイトル
date: 2020-09-17T18:41:34+09:00  # <= (date?) エントリを作成した日時, hugo new で作成すると自動的に埋め込まれる
draft: false                     # <= (boolean) 公開するかどうか / このエントリが下書き (準備中) かどうか (false にしないと公開されない, ローカル (サーバ) でも公開されないので注意)
weight: 2                        # <= chapter 中のエントリたちのうち、何番目に表示するか
---

(ここから記事の内容)
```