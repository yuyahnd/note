# note
Miscellaneous note.

## Installation
github から clone します。

```bash
$ git clone https://github.com/yuyahnd/note.git
```

### 環境構築
mkdocs をインストールします。

```bash
$ pip install mkdocs
$ pip install mkdocs-material
```

### ドキュメントプロジェクト作成

```bash
$ mkdocs new .
```

以下のようなディレクトリが作成されます。

```
.
├─ docs/
│  └─ index.md
└─ mkdocs.yml
```

### ローカルサーバー起動
```bash
$ mkdocs serve
```

### build
```bash
$ mkdocs build
```

### Github Pages deploy
```bash
$ mkdocs gh-deploy
```


## License
This repository is licensed under the MIT license. See LICENSE for details.

&copy; 2023 Yuya Honda
