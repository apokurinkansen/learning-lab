# learning-lab

技術学習のメモと練習コードをまとめるリポジトリ。

## 構造

```
learning-lab/
├── <言語・トピック>/
│   ├── notes/    # 学習メモ（Markdown）
│   └── code/     # 練習コード
└── templates/
    └── topic.md  # トピックメモのテンプレート
```

- 言語・トピックごとにトップレベルディレクトリを作成
- `notes/` に Markdown メモ、`code/` に練習コードを配置
- Obsidian で `notes/` ディレクトリを参照する前提の構成

## 使い方

### 新しいトピックのメモを作成

```bash
cp templates/topic.md go/notes/goroutine.md
```

### 新しい言語・トピックを追加

```bash
mkdir -p <言語名>/{notes,code}
```

## 現在のトピック

- `go/` - Go 言語
