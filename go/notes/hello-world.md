# Hello World と Go の基本構造

## 概要
Go の最小プログラムを通じて、Python との違いと Go プロジェクトの基本構造を理解する。

## 学んだこと
- Go の実行可能プログラムは `package main` + `func main()` が必須
- `go mod init <モジュール名>` でプロジェクトを初期化する（Python の `pyproject.toml` に相当）
- `go run main.go` でビルド＋実行、`go build` でバイナリ生成
- 未使用の import や変数はコンパイルエラーになる（Python と違い放置できない）
- `fmt` パッケージが標準出力を担当（Python の `print()` に相当）

## コード例
- [hello/main.go](../code/hello/main.go)

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

## Python との対応表
| 概念 | Python | Go |
|------|--------|-----|
| 実行 | `python main.py` | `go run main.go` |
| プロジェクト管理 | `pyproject.toml` | `go.mod` |
| 標準出力 | `print()` | `fmt.Println()` |
| パッケージ宣言 | 不要 | `package main` |
| 型 | 動的型付け | 静的型付け |

## 疑問・TODO
- [ ] `go build` でバイナリを作って実行してみる
- [ ] 複数ファイルのプロジェクト構成を学ぶ
- [ ] `fmt` パッケージの他の関数（`Printf`, `Sprintf` など）

## 参考リンク
- [A Tour of Go](https://go.dev/tour/)
- [Go Modules Reference](https://go.dev/ref/mod)
