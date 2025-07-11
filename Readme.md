# Pull Request 体験アプリケーション

## 概要

このアプリケーションは、GitHub の Pull Request（プルリクエスト）のワークフローを体験できる Web アプリケーションです。実際の GitHub インターフェースを模倣し、開発者が Pull Request の流れを理解できるよう設計されています。

**Note**: このアプリケーションは教育目的で作成されており、実際の Git リポジトリには接続されません。

Pull Request の概念と操作方法を学ぶためのシミュレーションツールです。

## 機能

### 📋 主要機能

- **ブランチ作成**: 新しいフィーチャーブランチの作成体験
- **コード編集**: リアルタイムでのコード編集機能
- **コミット**: 変更内容のコミット体験
- **Pull Request 作成**: 実際の GitHub ライクな PR 作成フォーム
- **差分表示**: 変更内容の可視化
- **マージ機能**: Pull Request のマージ体験

### 🎨 UI/UX 特徴

- **GitHub ライクなデザイン**: 実際の GitHub インターフェースを忠実に再現
- **ダークテーマ**: 開発者に親しみやすいダークモード UI
- **アニメーション**: スムーズなトランジションとローディング効果
- **レスポンシブデザイン**: モバイルデバイスでも使用可能

## 技術スタック

- **HTML5**: セマンティックな構造
- **CSS3**: モダンなスタイリング（Grid、Flexbox、アニメーション）
- **JavaScript (ES6+)**: インタラクティブな機能
- **No Dependencies**: 外部ライブラリを使用しない純粋な Web 技術

## 使用方法

### 1. セットアップ

```bash
# リポジトリをクローン
git clone https://github.com/gadgeski/pull-request-experience-app.git

# ディレクトリに移動
cd pull-request-experience-app

# ブラウザでindex.htmlを開く
open index.html
```

### 2. アプリケーションの使用手順

#### Step 1: ブランチ作成

1. 新しいブランチ名を入力（例: `feature/new-function`）
2. 「ブランチを作成」ボタンをクリック

#### Step 2: コード編集

1. コードエディタに新しいコードを記述
2. 「変更を保存」ボタンをクリック

#### Step 3: コミット

1. コミットメッセージを入力（例: `feat: add greeting function`）
2. 「コミット」ボタンをクリック

#### Step 4: Pull Request 作成

1. Pull Request のタイトルを入力
2. 詳細な説明を記述
3. 「Pull Request を作成」ボタンをクリック

#### Step 5: 確認とマージ

1. 作成された Pull Request を確認
2. 変更差分を確認
3. 「Pull Request をマージ」ボタンをクリック

#### Step 6: 完了

- マージ完了メッセージが表示
- 「もう一度試す」でリセット可能

## ファイル構成

```
pull-request-experience-app/
├── index.html          # メインアプリケーション
├── README.md          # このファイル
└── screenshots/       # スクリーンショット（オプション）
```

## 設計思想

### 教育目的

- **段階的学習**: 6 つのステップに分けた構造化されたワークフロー
- **視覚的フィードバック**: 各ステップの進捗状況を明確に表示
- **実践的体験**: 理論だけでなく実際の操作を通じた学習

### 技術的特徴

- **Pure JavaScript**: フレームワークに依存しない実装
- **モジュラー設計**: 各機能が独立して動作
- **エラーハンドリング**: 適切なバリデーションと例外処理

## カスタマイズ

### デザインのカスタマイズ

```css
/* メインカラーの変更 */
:root {
  --primary-color: #58a6ff;
  --success-color: #2ea043;
  --danger-color: #f85149;
}
```

### 機能の拡張

```javascript
// 新しいバリデーション関数の追加
function validateBranchName(branchName) {
  // カスタムバリデーションロジック
  return /^[a-zA-Z0-9-_/]+$/.test(branchName);
}

// 新しいステップの追加
function addCustomStep() {
  // カスタムステップの実装
}
```

### 言語サポート

現在は日本語のみサポートしていますが、以下のように多言語対応が可能です：

```javascript
const translations = {
  ja: {
    createBranch: "ブランチを作成",
    saveChanges: "変更を保存",
  },
  en: {
    createBranch: "Create Branch",
    saveChanges: "Save Changes",
  },
};
```

## 学習目標

このアプリケーションを使用することで、以下の概念を理解できます：

### Git 基本概念

- **ブランチ**: 機能開発のための分岐
- **コミット**: 変更内容の記録
- **マージ**: 変更内容の統合

### Pull Request ワークフロー

- **フィーチャーブランチ**: 新機能開発用のブランチ作成
- **コードレビュー**: 変更内容の確認プロセス
- **継続的インテグレーション**: 自動テストとマージ

### チーム開発

- **コラボレーション**: 複数人での開発協力
- **コード品質**: レビューを通じた品質向上
- **プロジェクト管理**: 変更履歴の追跡

## トラブルシューティング

### よくある問題

#### 1. ブランチ名が無効です

**原因**: 無効な文字が含まれている
**解決策**: 英数字、ハイフン、アンダースコア、スラッシュのみ使用

#### 2. コミットメッセージが空です

**原因**: メッセージが入力されていない
**解決策**: 適切なコミットメッセージを入力

#### 3. Pull Request が作成できません

**原因**: 必須フィールドが未入力
**解決策**: タイトルを必ず入力してください

### デバッグ情報

開発者ツールのコンソールでデバッグ情報を確認できます：

```javascript
// 現在のステップ状況を確認
console.log("Current step:", currentStep);
console.log("Branch name:", branchName);
console.log("Code content:", codeContent);
```

## 開発者向け情報

### 開発環境のセットアップ

```bash
# 開発用サーバーの起動（Python）
python -m http.server 8000

# 開発用サーバーの起動（Node.js）
npx serve .
```

### コードスタイル

- **インデント**: 4 スペース
- **命名規則**: camelCase
- **コメント**: 重要な機能には適切なコメント

### 貢献方法

1. フォークを作成
2. フィーチャーブランチを作成
3. 変更を実装
4. テストを実行
5. Pull Request を作成

## パフォーマンス最適化

### 最適化のポイント

- **CSS**: 必要最小限のスタイル定義
- **JavaScript**: 効率的な DOM 操作
- **アニメーション**: GPU 加速の利用

### メモリ使用量

- **軽量設計**: 外部ライブラリなし
- **効率的な状態管理**: 最小限の変数使用
- **イベントリスナー**: 適切なクリーンアップ

## セキュリティ考慮事項

### 入力値の検証

```javascript
function sanitizeInput(input) {
  return input.replace(/[<>]/g, "");
}
```

### XSS 対策

- **HTML エスケープ**: 動的コンテンツの適切な処理
- **入力検証**: 全ての入力値を検証

## 今後の拡張予定

### 機能追加

- [ ] **レビュー機能**: コードレビューの体験
- [ ] **コンフリクト解決**: マージコンフリクトの体験
- [ ] **CI/CD**: 自動テストとデプロイの体験
- [ ] **多言語対応**: 英語、中国語などの追加

### 技術改善

- [ ] **TypeScript**: 型安全性の向上
- [ ] **PWA**: オフライン対応
- [ ] **アクセシビリティ**: WCAG 準拠

## ライセンス

MIT License

## 著者

**gadgeski** - [GitHub Profile](https://github.com/gadgeski)

## 謝辞

このプロジェクトは、Git/GitHub の学習を支援するために作成されました。
GitHub の素晴らしいインターフェースデザインからインスピレーションを得ています。

## 参考資料

- [GitHub Docs - Pull Requests](https://docs.github.com/en/pull-requests)
- [Git Documentation](https://git-scm.com/doc)
- [Web MDN - Web APIs](https://developer.mozilla.org/en-US/docs/Web/API)

---
