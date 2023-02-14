# Mac

Mac についてのノートです。

- 作業環境
    - macOS Ventura 13.2

## SSH
- OpenSSH_9.0p1, LibreSSL 3.3.6

### 認証キー登録
```bash
ssh-add -K ~/.ssh/id_rsa
```

### 認証エージェント
1. .ssh/config に以下を記述する
```bash title=".ssh/config" linenums="1"
Host *
  UseKeychain yes
  AddKeysToAgent yes
```

2. キーロード
```bash
ssh-add --apple-load-keychain
```

## Homebrew インストール
下記コマンドを実行する

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- [参考](https://brew.sh/index_ja)
