# My Profile Site

プロフィール・ポートフォリオサイト

## 🌐 デモ
デプロイ後に公開URLを追加してください

## 🚀 GitHub Pagesへのデプロイ手順

### 1. GitHubリポジトリの作成

1. [GitHub](https://github.com) にログイン
2. 右上の「+」→「New repository」をクリック
3. リポジトリ名: `portfolio` (好きな名前でOK)
4. Public を選択
5. 「Create repository」をクリック

### 2. リモートリポジトリの設定とプッシュ

```bash
cd /Users/eshimayuusuke/workspace/myweb
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
git branch -M main
git push -u origin main
```

**注意:** `YOUR_USERNAME` を自分のGitHubユーザー名に変更してください

### 3. GitHub Pagesの有効化

1. GitHubリポジトリページの「Settings」タブをクリック
2. 左メニューの「Pages」をクリック
3. Source: `Deploy from a branch` を選択
4. Branch: `main` を選択、フォルダ: `/public` を選択
5. 「Save」をクリック

数分後、`https://YOUR_USERNAME.github.io/portfolio/` でサイトが公開されます！

### 4. Formspreeの設定（メール送信機能）

1. [Formspree](https://formspree.io/) にアクセス
2. 無料でサインアップ（GitHubアカウントでログイン可）
3. 「New Form」をクリック
4. フォーム名を入力（例: Portfolio Contact）
5. 作成されたフォームID（`YOUR_FORM_ID`）をコピー
6. [public/index.html](public/index.html) の109行目を編集:
   ```html
   <form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   `YOUR_FORM_ID` を実際のIDに置き換え
7. 変更をコミット&プッシュ:
   ```bash
   git add public/index.html
   git commit -m "Add Formspree form ID"
   git push
   ```

## ✏️ カスタマイズ

### プロフィール情報の変更
[public/index.html](public/index.html) を編集:
- 29行目: 名前
- 44-46行目: プロフィール情報
- 84, 89行目: SNSリンク（Instagram, GitHub）

### デザインの変更
[public/styles.css](public/styles.css) を編集

### 変更の反映
```bash
git add .
git commit -m "Update profile"
git push
```

## 📁 ファイル構成

```
myweb/
├── public/           # 公開用ファイル
│   ├── index.html   # メインHTML
│   ├── styles.css   # スタイル
│   └── app.js       # JavaScript
├── .gitignore       # Git除外設定
└── README.md        # このファイル
```

## 🛠 技術スタック

- HTML5
- CSS3
- JavaScript (ES6+)
- Formspree (メール送信)
- GitHub Pages (ホスティング)

---

© 2026 Yusuke Eshima
