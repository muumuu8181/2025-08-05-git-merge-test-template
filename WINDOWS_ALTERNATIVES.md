# 🪟 Windows環境用代替コマンド集

## sedコマンドの代替方法

### Option 1: PowerShellを使用
```powershell
# README.mdの## 概要セクション置換（Device A）
$content = Get-Content README.md -Raw
$newContent = $content -replace '(?s)## 概要.*?(?=\n## )', @"
## 概要
- **作成日**: 2025-08-05
- **目的**: Device-A UI Enhancement - 美しいユーザーインターフェース構築
- **使用技術**: HTML, CSS3, Bootstrap, Animation
- **Device-A改善**: モダンなボタンデザインとヘッダーレイアウト

"@
$newContent | Set-Content README.md
```

### Option 2: 手動編集
1. `README.md` をテキストエディタで開く
2. `## 概要` セクションを見つける
3. 以下の内容に置き換える：

**Device A版**:
```markdown
## 概要
- **作成日**: 2025-08-05
- **目的**: Device-A UI Enhancement - 美しいユーザーインターフェース構築
- **使用技術**: HTML, CSS3, Bootstrap, Animation
- **Device-A改善**: モダンなボタンデザインとヘッダーレイアウト
```

**Device B版**:
```markdown
## 概要
- **作成日**: 2025-08-05
- **目的**: Device-B Feature Enhancement - 高機能ユーティリティシステム
- **使用技術**: JavaScript ES6+, Node.js, Lodash
- **Device-B改善**: 日付処理、ID生成、バリデーション機能
```

**Device C版**:
```markdown
## 概要
- **作成日**: 2025-08-05
- **目的**: Device-C Documentation Enhancement - 包括的ドキュメント管理システム
- **使用技術**: Markdown, JSDoc, GitBook
- **Device-C改善**: API仕様書、設定ガイド、ベストプラクティス
```

### Option 3: Git Bash使用（推奨）
```bash
# Git for Windowsに含まれるGit Bashでsedが使用可能
# Git Bashを起動してから通常のLinuxコマンドを実行
```

## 簡単な実行方法

### より簡単なテスト版
手動編集を多用した簡略版：

1. **各デバイスフォルダでREADME.mdを手動編集**
2. **新規ファイルをテキストエディタで作成**
3. **npm installは通常通り実行**
4. **git操作は通常通り実行**

この方法なら確実にWindows環境で実行可能です。