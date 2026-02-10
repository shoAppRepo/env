# パッケージのインストール
```bash
# ウィンドウ分割
brew install zellij yazi

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# PATH通す
vim ~/.zshrc
export PATH="$HOME/.cargo/bin:$PATH"
source ~/.zshrc

# ディレクトリ構成
cargo install filetree

# git tree
cargo install keifu

# claude code
npm install -g @anthropic-ai/claude-code
```

# 通知
## 通知用のパッケージをインストール
osascriptだとうまくいかないことがあるので...
```
brew install terminal-notifier

# 確認
terminal-notifier -message "Test"
通知が来なければ、「システム設定」からterminal-notifierの通知設定を確認してください。
```

## claudeでhooksの登録
### 許可待ち
hooksのnotificationを利用
```
/hooks
```
- notificationを選択
- matcherで「permission_prompt」を入力
- 通知用のコマンドを登録
```
terminal-notifier -title "Claude Code" -subtitle "確認待ち" -message "Claude Codeが許可を求めています" -sound default
```

### 完了
```
/hooks
```
- stopを選択
- 通知用のコマンドを登録
```
terminal-notifier -title "Claude Code" -subtitle "終わったよ" -message "作業完了！！" -sound default```
```
