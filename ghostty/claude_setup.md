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