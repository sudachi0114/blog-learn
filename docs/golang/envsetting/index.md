---
id: golang-envsetting
title: "[Go] 環境構築"
sidebar_label: "[Go] 環境構築"
hide_table_of_contents: false
keywords:
  - go
  - mac
  - 環境構築
---

## Go 環境構築

Go 言語の開発環境を (macOS 上に) 構築するときの覚え書きと、
その中で得た知見のメモ。

### Install

いろいろ方法がある..

* brew 
* goenv
* 

* 一番単純なのは `brew` で入れちゃうのだと思う

```shell
$ brew install go

$ go version
go version go1.15.2 darwin/amd64
```

## Go に関する環境変数などの確認

```shell
$ go env
GO111MODULE=""
GOARCH="amd64"
...
```

### この中から大事そうなやつを厳選

たぶんこの辺りだと思う..
(詳細は後々書く..TODO:)

* `GO111MODULE=""`

* `GOBIN=""`

* `GOPATH="/Users/sudachi/go"`
  特にこれについてはいろいろ書きたい..(気がする)

* `GOROOT="/Users/sudachi/.goenv/versions/1.15.2"`


## Go の開発をする場所 (ディレクトリ)

`$GOPATH` のしたじゃないと..とかよく言われてるけど

`go mod init {{ここ}}` 
で頑張れば、基本どこでも OK そう。


##　パッケージについて

パッケージ管理ツールとかいろいろあるけど、
最近だと `go mod tidy` が最強だと思う..

### パッケージ分割について

最近のだと相対パスでのインポートはできないよ (たぶん 1.11 系以降はできない)

-> package module という単位で管理する、という話


## 参考
* [The Go Programming Language](https://golang.org/)
* [A Tour of Go](https://go-tour-jp.appspot.com/welcome/1)