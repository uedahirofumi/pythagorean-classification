# GitHub保存手順（Windows）

## 1. Gitの確認

PowerShellまたはWindows Terminalで:

```powershell
git --version
```

バージョンが出ればGitは導入済みです。

## 2. フォルダをPCへ置く

例:

```text
C:\Users\あなたの名前\Documents\pythagorean_classification_v1
```

移動:

```powershell
cd "C:\Users\あなたの名前\Documents\pythagorean_classification_v1"
```

## 3. 最初のGit履歴を作る

```powershell
git init -b main
git add .
git commit -m "Canonical research record v1 - 2026-10-07"
```

確認:

```powershell
git log --oneline
```

## 4. GitHubで空のリポジトリを作る

GitHubにログインし:

1. 右上の + を押す
2. New repository
3. Repository name: 例 `pythagorean-classification`
4. 最初は Private 推奨
5. README / .gitignore / License は追加しない
6. Create repository

## 5. ローカルとGitHubを接続

GitHubの新規リポジトリ画面に表示されるHTTPS URLをコピー。

例:

```text
https://github.com/YOURNAME/pythagorean-classification.git
```

PowerShell:

```powershell
git remote add origin https://github.com/YOURNAME/pythagorean-classification.git
git remote -v
```

## 6. GitHubへ送る

```powershell
git push -u origin main
```

認証画面が出たらGitHubアカウントで認証します。

## 7. 今回の版にタグを付ける

```powershell
git tag -a v1.0 -m "Nondegenerate classification complete - 2026-10-07"
git push origin v1.0
```

## 8. 今後の更新

大きな変更時は過去の正典を上書きせず、新しい日付ファイルを追加します。

例:

```text
docs/2026-10-20_Pythagorean_classification_v2.md
```

その後:

```powershell
git status
git add .
git commit -m "Prove degenerate branch classification"
git push
```

## 9. 最低限覚えるコマンド

```powershell
git status
git add .
git commit -m "変更内容"
git push
```

履歴確認:

```powershell
git log --oneline
```

## 10. 注意

パスワード、APIキー、秘密鍵、個人情報などはcommit/pushしないでください。

研究の公開優先権や恒久的引用を強くしたい場合、GitHubの履歴に加えて、後でZenodo DOIやarXivを使うのが適切です。
