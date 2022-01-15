# Mac
Macについてのノートです。  
- 作業環境
  - macOS 12.1

## ssh
- OpenSSH_8.6p1, LibreSSL 2.8.3

### 認証キー登録
```
ssh-add -K ~/.ssh/id_rsa
```

### 認証エージェント
1. .ssh/config に以下を記述する
```
Host *
  UseKeychain yes
  AddKeysToAgent yes
```

2. キーロード
```
ssh-add --apple-load-keychain
```
