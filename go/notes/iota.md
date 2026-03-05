# iota

## 概要
Go で連続した定数を定義するための仕組み。他の言語の `enum` に相当する。読み方は「イオタ」（ギリシャ文字 ι 由来）。

## 学んだこと
- `const` ブロック内で 0 から始まり、1行ごとに +1 される
- 2行目以降は `= iota` を省略できる（前の行のパターンが繰り返される）
- `const` ブロックごとに 0 にリセットされる
- `_` で特定の値をスキップできる
- 式と組み合わせられる（`1 << iota` でビットフラグなど）

### Go に enum がない理由
- Go の設計方針「既存の仕組みの組み合わせで十分なら、専用の構文は作らない」
- `const + iota + 型定義` で enum と同等のことができる
- ただし `Weekday(999)` のような不正な値もコンパイルエラーにならない弱点がある

## コード例

```go
// 基本
const (
    Red   = iota // 0
    Green        // 1
    Blue         // 2
)

// 型定義と組み合わせる
type Weekday int

const (
    Sunday Weekday = iota
    Monday
    Tuesday
)

// ビットフラグ
const (
    Read    = 1 << iota // 1
    Write               // 2
    Execute             // 4
)
```

## 疑問・TODO
- [ ] enum を追加する提案（Go の issue）を読んでみる

## 参考リンク
- [Go Spec - Iota](https://go.dev/ref/spec#Iota)
