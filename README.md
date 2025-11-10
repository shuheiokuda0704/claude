# hello world

シンプルなウェルカムページプロジェクト

## 概要

美しいグラデーション背景とフェードインアニメーションを持つ、モダンな「hello world」ページです。

## 特徴

- 🎨 **美しいデザイン**: グラデーション背景とスムーズなアニメーション
- 🔒 **セキュリティ**: CSP、X-Frame-Optionsなどのセキュリティヘッダーを実装
- ♿ **アクセシビリティ**: セマンティックHTML、ARIA属性、アニメーション削減設定への対応
- 📱 **レスポンシブ**: モバイル、タブレット、デスクトップに対応
- ⚡ **パフォーマンス**: CSS変数、will-changeによる最適化

## セットアップ

### 必要条件

- Webブラウザ（Chrome、Firefox、Safari、Edgeなど）

### インストール

1. リポジトリをクローン:
```bash
git clone <repository-url>
cd claude
```

2. Webブラウザで `index.html` を開く:
```bash
open index.html
```

または、ローカルサーバーを起動（推奨）:
```bash
# Pythonを使用する場合
python -m http.server 8000

# Node.jsを使用する場合
npx http-server
```

その後、ブラウザで `http://localhost:8000` にアクセスします。

## ファイル構成

```
.
├── index.html    # メインHTMLファイル
├── styles.css    # スタイルシート
└── README.md     # このファイル
```

## セキュリティ機能

- **Content Security Policy (CSP)**: 外部スクリプトの実行を防止
- **X-Frame-Options**: クリックジャッキング攻撃を防止
- **X-Content-Type-Options**: MIMEタイプスニッフィングを防止
- **Referrer-Policy**: リファラー情報の漏洩を防止
- **HTTPS強制**: 安全な接続を確保

## アクセシビリティ

- セマンティックHTML（`<main>`, `<h1>`）を使用
- ARIA属性（`aria-label`）でスクリーンリーダーをサポート
- `prefers-reduced-motion`メディアクエリでアニメーション削減設定に対応
- 十分なコントラスト比を確保

## カスタマイズ

### 色の変更

`styles.css` の CSS変数を編集してカラースキームを変更できます:

```css
:root {
    --gradient-start: #667eea;  /* グラデーション開始色 */
    --gradient-end: #764ba2;    /* グラデーション終了色 */
    --text-color: white;        /* テキスト色 */
}
```

### アニメーション設定

アニメーションの速度を変更するには:

```css
:root {
    --animation-duration: 2s;  /* アニメーション時間 */
}
```

### フォントサイズ

見出しのサイズを変更するには:

```css
:root {
    --heading-size: 5rem;  /* デスクトップ用 */
}
```

## ブラウザサポート

- Chrome 88+
- Firefox 85+
- Safari 14+
- Edge 88+

## ライセンス

MIT License

## 貢献

プルリクエストを歓迎します。大きな変更を行う場合は、まずissueを開いて変更内容を議論してください。

## 作成者

Created with Claude Code
