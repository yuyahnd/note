# 複数リポジトリの履歴を保持したまま統合する

root_repo と sub_repo を１つのリポジトリへ統合する。

```bash title="ディレクトリ構成"
root_repo
├─ .git
└─ sub_repo
```

## 手順
1. root_repo に統合用ディレクトリをコミットする。
2. 統合する sub_repo をリモートリポジトリとして追加する。
3. sub_repo を sbutree オプションを使って指定のディレクトリへマージする。

### コマンド

```bash title="統合用ディレクトリをコミット"
$ mkdir sub_repo
$ touch sub_repo/.gitkeep
$ git add -i
$ git commit -m "sub_repo用ディレクトリを作成"
```

```bash title="リモートリポジトリ追加"
$ git remote add -f sub_repo https://github.com/xxxxx/sub_repo.git
```

```bash title="マージ"
$ git merge --allow-unrelated-histories -X subtree=sub_repo/ sub_repo/main
```
