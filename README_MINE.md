# 自分用メモ・チェックリスト (aituber-kit)

このリポジトリを触るときの自分用のメモです。本番の README は `README.md` を参照。

---

## リポジトリ構成

| リモート | URL | 用途 |
|---------|-----|------|
| **origin** | https://github.com/kaedeee/aituber-kit | 自分の fork（push 先） |
| **upstream** | https://github.com/tegnike/aituber-kit | フォーク元（本家） |

---

## フォーク元の最新を取り込む手順

```bash
git fetch upstream
git merge upstream/main -m "Merge upstream/main: sync with tegnike/aituber-kit"
# コンフリクトが出たら解消してから commit
git push origin main   # 必要なら
```

ローカルに未コミットの変更がある場合は、先に `git stash` してから merge し、あとで `git stash pop`。

---

## よく使うコマンド（開発）

```bash
npm run dev       # 開発サーバー (http://localhost:3000)
npm run build     # 本番ビルド
npm test          # テスト
npm run lint      # ESLint
```

---

## 自分用チェックリスト（作業前・作業後）

- [ ] `npm install` 済み / 依存は最新
- [ ] `.env` を `.env.example` からコピーして必要項目を設定済み
- [ ] フォーク元を触る前に `git fetch upstream` で最新確認
- [ ] 言語ファイルの更新は **日本語（locales/ja/）のみ**（他言語は手動で触らない）

---

## メモ（自由に追記してOK）

- 最終で upstream 同期した日: 2025-02-13（merge upstream/main 済み）
- ローカルで保持している変更: `.gitignore` に `.secretkey` を追加、`.vscode/settings.json` を自分用に変更

---

*このファイルはリポジトリの運用用メモです。本家への PR には含めない想定。*
